# ✖️ Multiplicacao

Gerador de tabuada interativa de 1 a 20 com HTML, CSS e JavaScript.

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## 📑 Sumário

- [Sobre](#sobre)
- [Funcionalidades](#funcionalidades)
- [Tecnologias](#tecnologias)
- [Como executar](#como-executar)
- [Estrutura](#estrutura)
- [Como funciona o código](#como-funciona-o-código)
- [Licença](#licença)

## 📖 Sobre

Aplicação web simples: o usuário digita um número e gera a tabuada correspondente, renderizada dinamicamente via DOM.

## ✨ Funcionalidades

- Campo numérico com validação básica
- Botão "Gerar Tabela"
- Tabela de 1 a 20 com estilo responsivo

## 🛠️ Tecnologias

- HTML5
- CSS3 (centralizado, cards, responsivo)
- JavaScript (criação dinâmica de `<table>`)

## 🚀 Como executar

```bash
git clone https://github.com/VictorHFL/Multiplicacao.git
cd Multiplicacao
# abra index.html no navegador
```

## 📁 Estrutura

```text
Multiplicacao/
├── index.html
├── style.css
└── README.md
```

## ⚙️ Como funciona o código

```javascript
function gerarTabela() {
  const numero = document.getElementById('numero').value;
  const tabela = document.createElement('table');

  for (let i = 1; i <= 20; i++) {
    const linha = tabela.insertRow();
    const coluna = linha.insertCell(0);
    coluna.textContent = `${numero} x ${i} = ${numero * i}`;
  }

  const divTabela = document.getElementById('tabela');
  divTabela.innerHTML = '';
  divTabela.appendChild(tabela);
}
```

> [!NOTE]
> O CSS está embutido no `<style>` do `index.html`; `style.css` é um extra opcional.

## 📄 Licença

Distribuído sob a licença MIT. Veja [LICENSE](LICENSE) para detalhes.

