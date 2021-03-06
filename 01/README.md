# JS

* Interpretada

* String API
    * toLowerCase (minuscula)
    * trim (remove espaço)
    * match (retorna array resultante da busca com RegEx)

* Math API
    * Metodos comuns para tratar numeros

* Prototype
    * Representa um objeto no JS
    * Injeta funções nele e pode usar em outros lugares
    * Object
        * Atributos não privados

* Functions
    * primeira classe
        * atribuir uma função para uma variavel

        * antes do código ser carregado

    * Expression
    * carregada durante a interpretação do código
    ```js
        var a = function() {
            return 'f';
        }

        a();
    ```


    * Declaration

    ```js
        function a () {
            return 'f';
        }

        a();
    ```

    * Named Function Expression
    ```js
        var nome = function nome() {
            return "hello world";
        }
    ```

    * Maneiras de chamar uma função
        * Escolpo global
        * Função por meio de um objeto
            * Fabrica
                * retorna um objeto
                ```js
                    var pessoa = function (nome, idade) {
                        return {
                            nome = nome;
                            idade = idade;
                        }
                    }

                    joao = pessoa("joao",18);
                ```
            * Construtora
                * novo objeto, passa o this
                    ```js
                        function pessoa (nome, idade) {
                            this.nome = nome;
                            this.nome = idade;
                        }

                        joao = new pessoa("joao",18);
                    ```
        * Por meio de Call e Apply
        ```js
            var pessoa = function() {
                console.log(arguments)
                return 'joao';
            }

            pessoa.call(this , 1,2,3,4,5);
            pessoa.apply(this , [1,2,3,4,5])
        ```

* Array API
    * concat (juntar dois arrays)
    * every (todoso elementos são iguais a algo)
    * filter (filtra o array)
    * join ("toString")
    * indexOf - lastIndexOf
    * map (transforma os elementos de um array)
    * unshift (add elemento no inicio de um array)
    * slice (retorna uma parte de um array)

* RegEx

    [Exercicios](https://github.com/workshopper/regex-adventure)

    * \ - antes de caracteres especiais
    * ^ - inicia com
    * $ - acaba com
    * [abc] - char dentro desse grupo
        * [0-9]
    * [^abc] - não esta nesse grupo
        * [^0-9]
    * {n} - quantificar

    * Metacaracteres
        * . - qq caracteres
        * \w - conjunto [a-zA-z0-9]
        * \W - conjunto [^a-zA-z0-9]
        * \d - [0-9]
        * \D - [^0-9]
        * \s - espaço em branco
        * \S - nega espaço em branco
        * \n - quebra de linha
        * \t - tab

    * Modificadores
        * i - Case-insensitive
        * g - global matching
        * m - multline matching
