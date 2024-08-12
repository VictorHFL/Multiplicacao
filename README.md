# Gerador de Tabela de Multiplicação

Este projeto é uma aplicação web simples que permite ao usuário gerar uma tabela de multiplicação para qualquer número escolhido. A aplicação utiliza HTML, CSS e JavaScript para gerar e estilizar a tabela de forma moderna e responsiva.

## ⚙️ Funcionalidades

- O usuário pode inserir um número no campo de entrada.
- Ao clicar no botão "Gerar Tabela", uma tabela de multiplicação para o número inserido é gerada.
- A tabela exibe os resultados de 1 até 20.

## 🖥️ Tecnologias Utilizadas

- **HTML**: Estrutura básica da página.
- **CSS**: Estilização da página com foco em design moderno e responsivo.
- **JavaScript**: Lógica para geração dinâmica da tabela de multiplicação.

## 📋 Estrutura do Código

### HTML

O HTML define a estrutura básica da aplicação:

- **`<div class="container">`**: Contêiner principal que contém todo o conteúdo da página, centralizado com bordas arredondadas e sombra.
- **`<input type="number" id="numero" placeholder="Digite um número">`**: Campo de entrada onde o usuário insere o número.
- **`<button onclick="gerarTabela()">Gerar Tabela</button>`**: Botão que aciona a geração da tabela.
- **`<div id="tabela"></div>`**: Div onde a tabela de multiplicação será gerada dinamicamente.

### CSS

O CSS é utilizado para aplicar estilos modernos e responsivos:

- **Body**: Centraliza o conteúdo e aplica um fundo claro.
- **Container**: Define um layout com bordas arredondadas e sombra para destacar o conteúdo.
- **Tabela**: Estiliza a tabela para uma aparência limpa, com células centralizadas e separação clara entre linhas.
- **Input e Button**: Ambos são estilizados para serem responsivos, com transições suaves e bordas arredondadas.

### JavaScript

O JavaScript controla a geração dinâmica da tabela:

```javascript
function gerarTabela() {
    const numero = document.getElementById('numero').value;
    const tabela = document.createElement('table');

    for (let i = 1; i <= 20; i++) {
        const linha = tabela.insertRow();
        const coluna = linha.insertCell(0);
        coluna.innerHTML = `${numero} x ${i} = ${numero * i}`;
    }

    const divTabela = document.getElementById('tabela');
    divTabela.innerHTML = '';
    divTabela.appendChild(tabela);
}