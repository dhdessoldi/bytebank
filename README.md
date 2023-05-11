# Bytebank

ByteBank é uma plataforma de banco digital, desenvolvida em uma única página com as funcionalidades de realizar depósitos e transferências, modificando o saldo do usuário. 
Este projeto foi desenvolvido para praticar testes de front-end utilizando o Jest e o React Testing Library. Foram realizados os seguintes testes:

- Teste de componente react para verificar se o nome do usuário logado está renderizado utilizando **getByText()**, que busca o texto informado no documento renderizado, e **expect(...).toBeInTheDocument()**, que retorna se o texto está ou não no documento;

- Verificar se o link para a home está renderizado utilizando **getByText()**, que busca o link informado no documento renderizado, e **expect(...).toBeInTheDocument()**, que retorna se o link está ou não no documento;

- Verificar se uma lista de links está renderizada utilizando **getAllByRole()**, que busca todos os elementos com a mesma role e retorna um array, e **expect(...).toHaveLenght(...)**, que verifica se o array buscado possui o tamanho informado;

* Verificar se o link para o Extrato não está renderizado utilizando **queryByText()**, que retorna 1 ou nulo, e **expect(..).not.toBeInTheDocument()**, que passa no teste caso o retorno seja nulo;

* **findBy() e findAllBy()** não estão no projeto, mas são utilizados para elementos assíncronos que ainda vão ser carregados na página, ou seja, espera esse elemento ser carregado, retorna uma _promise_;

* Verificando os estilos de um array retornado por **getAllByRole()**, utilizando **forEach()** para percorrer o array e utilizar o **expect(..).toHaveClass(...)** para checar se os elementos do array estão com a classe correta;

* Tirar um _snapshot_ do código utilizando **expect().toMatchSnapshot()** no mesmo teste citado acima;

* Utilizar o **userEvent()** para simular o comportamento de pessoas usuárias interagindo com a página;

* Utilizar o **describe()** para melhor semântica de testes;

* Testar componentes que recebem props, passando as props na renderização do componente e simulando props;

* Utilizar o **rerender** para atualizar o componente dado nova atribuição de props;

* Mockar um comportamento utilizando **just.fn()**. Neste caso foi selecionado um botão utilizando **getByRole('button')** e mockado um evento de clique com **userEvent.click()**, para testar quantas vezes a função mockada foi chamada com **expect().toHaveBeenCalledTimes()**;

Introdução à **TDD (test driven development)**, que é uma metodologia para desenvolvimento e escrita de códigos que funciona da seguinte maneira:

- Escrevemos um teste unitário que inicialmente irá falhar, já que o código testado ainda não foi implementado;
- Criamos o código que faça o teste passar, ou seja, a implementação da funcionalidade testada. Esse código deve satisfazer imediatamente a asserção que colocamos no nosso teste;
- Quando o código estiver implementado e o teste satisfeito podemos refatorar o código. E agora que a funcionalidade está criada, ela deve passar sem que seja necessário reescrever o teste.

Boas práticas no desenvolvimento de testes:

- Utilização de it() em vez de test() para o código ficar mais semântico em inglês;

- Realizar testes unitários curtos e com poucas e exceções;

- Corrigir todos os problemas rapidamente para garantir que os testes passem em 100% das vezes que for testado.

### Tecnologias utilizadas

* React com JavaScript;
* CSS modules;

Para rodar a aplicação será necessário instalar:

* [Visual Studio Code](https://code.visualstudio.com/) ou algum outro editor de código;
* [Node.js](https://nodejs.org/en);
* [Git](https://git-scm.com/downloads);

Após baixar instalar os programas acima e baixar o código, abra a pasta da aplicação pelo Visual Studio Code, com ela aberta siga os seguintes passos:

* Pressiona **Ctrl + '** para abrir o terminal;
* Digite **npm install** para instalar as dependências do projeto;
* Digite **npm start** para rodar a aplicação e abri-la em seu navegador.
  
  
  ### ScreenShots
![Captura de tela da página do ByteBank](https://github.com/dhdessoldi/bytebank/assets/110476564/797dcbbd-c02d-4a44-8127-c454cca45e87)

