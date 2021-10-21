# 🚀 Front-End React Native do NLW-07 HEAT - RocketSeat 🚀

## 👨‍💻 Tecnologias utilizadas 👩‍💻

- Javascript (Linguagem programação)
- Typescript (Tipagem para Javascript)
- React Native (Biblioteca Javascript para desenvolver aplicativos para Android e iOS de forma nativa)
- Expo (Framework para React Native, para aumentar produtividade)
- REST (Arquitetura)
- Oauth2 (Autenticação)
- Socket.IO Client (Web socket - Comunicação em tempo-real)

### 🗃️ Bibliotecas utilizadas 📚

- @expo-google-fonts/roboto : adiciona fonte Roboto
- @react-native-async-storage/async-storage : adiciona métodos de storage
- axios : HTTP client
- expo : framework para aumentar produtividade
- expo-app-loading : mantém a splash screen visível enquanto AppLoading está montado
- expo-auth-session : adiciona autenticação baseada em navegador web
- expo-font : permite carregar e usar fontes da web
- expo-linear-gradient : adiciona métodos para aplicar gradiente linear
- expo-random : criar bytes aleatórios fortes necessário para expo-auth-session
- expo-status-bar : para configuração da barra de status dos dispositivos
- moti : pacote de animação universal para React Native
- react : biblioteca criação de interfaces
- react-dom : extensão do ReactJs para manipulação do DOM
- react-native : biblioteca JS para desenvolver aplicativos para Android e iOS de forma nativa
- react-native-iphone-x-helper : adiciona métodos para acertar a altura do status bar e footer nos dispositivos com tela notched
- react-native-reanimated : simplifica a criação de animações, necessária para moti com expo
- react-native-svg : permite utilizar SVG no React Native
- react-native-web : componentes React Native e APIs para a Web
- socket.io-client : cliente do Socket IO para comunicação em tempo-real
- react-native-svg-transformer (dev) : transforma imagens SVG importadas em componentes React para o React Native
- typescript (dev) : adiciona tipagem para javascript

## 🔐 Resumo do fluxo de autenticação Oauth 🚫

- Solicitar login ao github ao clicar no botão de Login com github
- Entra no fluxo de autenticação com navegador web usando a url do github: https://github.com/login/oauth/authorize?scope=escopo_tipo&client_id=id_do_client e as Homepage URL e callback URL fornecidos pelo Expo (https://auth.expo.io/@nome_do_usuario/nome_do_aplicativo)
- Autorizar o acesso as informações do usuário do github e inserir as credenciais do github quando for solicitado.
- Recebe a resposta do github pelo Expo com o código do github para efetuar o login (resposta.params.code)
- Enviar uma solicitação de login ao back-end enviando o código do github no corpo da requisição (code)
- Como resposta da requisição recebe-se um token para acesso aos recursos e as informações do usuário
- Inserir o token de acesso no cabeçalho das requisições
- Guardar o token no AsyncStorage
- Guardar as informações do usuário no AsyncStorage
- Guardar as informações do usuário em um estado (do React)

## 🖇️ Utilização resumida do Socket IO client no app 🔗

- criar um web socket client para um determinado servidor web (método io())
- criar escuta para uma determinada ação emitida pelo servidor (método on())
- a escuta executa uma ação no app:
  - no caso guarda a informação emitida em uma variável
  - de tempo em tempo a aplicação verifica esta variável por novas informações
  - se há novas informações exibe na lista de mensagens recentes as informações

## 🖼️ Imagens do projeto 👀

<img src="https://raw.githubusercontent.com/rodolfoHOk/portfolio-img/main/images/nlw-heat-mobile-01.jpg" alt="NLW HEAT Img1" width="450"/>

<img src="https://raw.githubusercontent.com/rodolfoHOk/portfolio-img/main/images/nlw-heat-mobile-02.jpg" alt="NLW HEAT Img2" width="450"/>

<img src="https://raw.githubusercontent.com/rodolfoHOk/portfolio-img/main/images/nlw-heat-mobile-03.jpg" alt="NLW HEAT Img2" width="450"/>

## ⚙️ Link para o projeto do Back-End no Github 🗄️

https://github.com/rodolfoHOk/nlw-heat-node

## ⚙️ Link para o projeto do Front-End Web no Github 🖥️

https://github.com/rodolfoHOk/nlw-heat-web
