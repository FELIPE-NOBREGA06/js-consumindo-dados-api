# Alura Books - Formulário de Cadastro

Um formulário de cadastro responsivo desenvolvido com HTML, CSS e JavaScript, integrado com a API ViaCEP para preenchimento automático de endereços.

![Alura Books](./img/Logo.svg)

## 📋 Descrição

Este projeto é uma página de cadastro para a plataforma Alura Books. Ele permite que usuários preencham seus dados pessoais e endereço de forma intuitiva, com validação de campos e busca automática de endereço através do CEP.

## ✨ Funcionalidades

- **Formulário responsivo** - Adaptável para diferentes tamanhos de tela
- **Busca automática de CEP** - Integração com API ViaCEP para preenchimento automático de endereço
- **Validação de campos** - Campos obrigatórios marcados com `required`
- **Menu responsivo** - Menu hambúrguer para dispositivos móveis
- **Página de sucesso** - Confirmação após envio do formulário
- **Design moderno** - Utiliza fonte Poppins do Google Fonts

## 🛠️ Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilização e responsividade
- **JavaScript (ES6+)** - Funcionalidades interativas
- **API ViaCEP** - Busca de endereços por CEP
- **Google Fonts** - Tipografia

## 📁 Estrutura do Projeto

```
.
├── index.html                 # Página principal do formulário
├── cadastro-finalizado.html   # Página de sucesso
├── script.js                  # Lógica JavaScript
├── styles/
│   ├── reset.css             # Reset de estilos padrão
│   ├── styles.css            # Estilos principais
│   ├── header.css            # Estilos do cabeçalho
│   ├── banner.css            # Estilos do banner
│   ├── formulario.css        # Estilos do formulário
│   ├── cadastro.css          # Estilos da página de sucesso
│   └── rodape.css            # Estilos do rodapé
└── img/                       # Imagens e ícones do projeto
```

## 🚀 Como Usar

1. Clone ou baixe o repositório
2. Abra o arquivo `index.html` em um navegador web
3. Preencha o formulário com seus dados
4. O campo de CEP preencherá automaticamente os campos de endereço
5. Clique em "Enviar formulário" para finalizar o cadastro

## 📝 Campos do Formulário

### Dados Pessoais
- Nome Completo (obrigatório)
- Data de Nascimento (obrigatório)
- Telefone (obrigatório)
- E-mail (obrigatório)

### Endereço
- CEP (obrigatório) - Dispara busca automática
- Endereço (obrigatório)
- Número (obrigatório)
- Complemento (opcional)
- Bairro (obrigatório)
- Cidade (obrigatório)
- Estado/UF (obrigatório)

## 🔌 Integração com API ViaCEP

O JavaScript utiliza a API ViaCEP para buscar informações de endereço baseado no CEP inserido:

```javascript
async function buscaEndereco(cep) {
  const consultaCEP = await fetch(`https://viacep.com.br/ws/${cep}/json/`);
  const consultaCEPConvertida = await consultaCEP.json();
  // Preenche os campos automaticamente
}
```

