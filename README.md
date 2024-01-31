# Calculadora Web
html, css, javascript

![image](https://user-images.githubusercontent.com/81652916/222916745-c7f6a04c-38e3-4db5-b477-dcd73358c913.png)


## Visão Geral

Este repositório contém o código-fonte para uma aplicação web de calculadora simples. A calculadora é implementada usando HTML, CSS e JavaScript, proporcionando operações aritméticas básicas como adição, subtração, multiplicação e divisão.

## Estilos Gerais

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'cursiva', sans-serif;
}

body {   
    background-color: #2ab3ac; 
}
```

## Funcionalidades

1. **Função de Inserção:** Permite aos usuários inserir valores numéricos e operadores ao clicar nos botões correspondentes.

    ```javascript
    function insert(valor) {
        resultado.innerHTML += valor;
    }
    ```

2. **Função de Limpeza:** Limpa a tela da calculadora.

    ```javascript
    function clean(){
        resultado.innerHTML = ' ';
    }
    ```

3. **Função de Retrocesso:** Remove o último caractere inserido.

    ```javascript
    function backspace() {
        if(resultado.textContent) {
            let result = document.getElementById("resultado").innerHTML
            resultado.innerHTML = result.substring(0, result.length -1);
        }
    }
    ```

4. **Função de Confirmação:** Avalia e exibe o resultado da expressão matemática.

    ```javascript
    function confirma() {
        if(resultado.textContent != 'Erro') {
            document.getElementById("resultado").innerHTML = eval(resultado.innerHTML);
        }
    }
    ```

## Estilos Específicos

```css
.calculator {
    width: 250px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 15px;
    padding: 10px;
    background-color: #000807;
}

table td {
    display: inline-block;
}

.btn {
    margin: 3px;
    width: 50px;
    height: 40px;
    cursor: pointer;
    background-color: #0c1a21;
    color: #dfdfdf;
    font-size: 16px;
    transition: all 500ms ease-in-out;
}

.btn:hover {
    background-color: #162f3b;
}

.ac {
    background-color: #1b7269;
}

.ac:hover {
    background-color: #228f84;
}

.especial {
    background-color: #228f84;
}

.especial:hover {
    background-color: #18646b;
}

.igual {
    background-color: #1b7269;
}

.igual:hover {
    background-color:  #228f84;
}

.result {
    height: 100px;
    color: #dfdfdf;
    text-align: right;
    font-size: 35px;
    word-wrap: break-word;
    border-bottom: 1px solid #25968a;
}
```

## Uso

1. Clone o repositório:

    ```bash
    git clone https://github.com/seu-usuario/nome-do-repositorio.git
    ```

2. Abra o arquivo `index.html` no seu navegador web.

3. Utilize a interface da calculadora para realizar operações aritméticas básicas.

