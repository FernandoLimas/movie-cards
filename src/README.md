# Boas vindas ao repositório do projeto Movie Cards Library!

# Habilidades

  Nesse projeto, utilizei:
  - Gerenciador de pacotes
  - Inicializei um projeto em **React**
  - Utilizei JSX no **React**
  - Utilizei o **ReactDOM.render** para renderizar elementos numa página web
  - Utilizei o `import` para usar código externo junto ao seu
  - Criei componentes **React**
  - Fiz uso de `props`
  - Fiz composição de componentes
  - Criei múltiplos componentes dinamicamente
  - Utilizei **PropTypes** para checar o tipo de uma prop no uso de um componente
  - Utilizei **PropTypes** para garantir a presença de props obrigatórias no uso de um componente
  - Utilizei **PropTypes** para checar que uma prop é um objeto de formato específico
  - Utilizei **PropTypes** para garantir que uma prop é um array com elementos de um determinado tipo

## O que desenvolvi?

Uma biblioteca de cartões de filmes utilizando React. A biblioteca possui um cabeçalho e uma lista de cartões. Cada cartão representa um filme e possui uma imagem, título, subtítulo, sinopse e avaliação. A biblioteca na imagem abaixo.

![image](preview.png)

## Iniciar o projeto:

Instalar as dependências do projeto com o comando:
  ```bash
npm install
```

## Testes
Os testes para cada requisitos estão na pasta `src/tests`. Leia os arquivos para entender como os testes estão organizados.

Para executar os testes localmente, digite no terminal o comando `npm test`. Inicialmente, seus testes estarão assim:

![image](failing-tests.png)

A primeira parte da saída mostra um sumário de cada teste e seu status. Um ❌ representa um teste falhando, enquanto um ✅ representa um teste correto. Naturalmente, no início todos os testes estarão falhando.

Abaixo do sumário, para cada teste falhando, há uma mensagem explicativa sobre o motivo que causou a falha do teste, assim como a linha em que a falha ocorreu. Na imagem, vemos que o teste falha porque o componente `<Header />`, utilizado na linha 38, não está definido.

Se fizermos uma implementação simples do componente `<Header />`, que não renderiza nada:

```jsx
import React from 'react';

class Header extends React.Component {
  render() {
  }
}

export default Header;
```

Veremos que o primeiro teste agora passa:

![image](first-green-test.png)

Quando seu projeto estiver terminado, todos os testes deverão estar passando:

![image](all-green.png)

---

## Linter

Para garantir a qualidade do código, utilizei neste projeto os linters `ESLint` e `StyleLint`.
Assim o código estará alinhado com as boas práticas de desenvolvimento, sendo mais legível
e de fácil manutenção! Para rodá-los localmente no projeto, execute os comandos abaixo:

  ```bash
npm run lint
npm run lint:styles
```

## Dica: desativando testes

 Pode desabilitar temporariamente um teste utilizando a função `skip` junto à função `it`. Como o nome indica, esta função "pula" um teste:

```js
it.skip('it includes the text `Movie Cards Library` inside a h1 tag', () => {
  wrapper = shallow(<Header />);

  expect(wrapper.find('header h1').text()).toBe('Movie Cards Library');
});
```

Na saída da execução dos testes, você verá um <img src="orange-circle.png" width="15px"> indicando que o teste está sendo pulado:

![image](skipped-test.png)

Uma estratégia é pular todos os testes no início e ir implementando um teste de cada vez, removendo dele a função `skip`.

## Dica: watch mode

Ao executar os testes localmente, [Jest](https://jestjs.io/), a ferramenta que executa os testes, entra em _watch mode_. Nesse modo, a cada vez que um arquivo é salvo, os testes são executados novamente. Isso pode aumentar sua produtividade removendo a necessidade de executar os testes manualmente o tempo todo. Você pode abrir uma aba no seu terminal ou no terminal do _VSCode_ e deixar o _Jest_ rodando nesse modo.

---
