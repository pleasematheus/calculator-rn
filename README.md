# Calculadora React Native
Este é um projeto simples de uma calculadora feita em React Native.

## Como executar
Para executar este projeto, basta clonar este repositório e executar os seguintes comandos:

## Instalar as dependências
Com o terminal aberto e no diretório da aplicação digite:
```
npx install react-native
```

## Executar a aplicação
```
npx react-native run-android
```
ou
```
npx react-native run-ios
```

# Componentes
## Botão
O componente `Botão` é responsável por renderizar um botão na tela da calculadora. Ele recebe os seguintes parâmetros:

- label: O texto que será exibido no botão;
- double (opcional): Um valor booleano que indica se o botão deve ter o dobro do tamanho padrão;
- triple (opcional): Um valor booleano que indica se o botão deve ter o triplo do tamanho padrão;
- operation (opcional): Um valor booleano que indica se o botão é uma operação (como +, -, * e /).

# Display
O componente `Display` é responsável por renderizar o visor da calculadora. Ele recebe um único parâmetro:

value: O valor que será exibido no visor.

# App
O componente `App` é o componente principal da aplicação. Ele renderiza os componentes Display e Botão, e implementa a lógica da calculadora.

## Estado inicial
O estado inicial da calculadora é definido pela constante `initialState` e tem a seguinte estrutura:

```
const initialState = {
  displayValue: '0',
  clearDisplay: false,
  operation: null,
  values: [0, 0],
  current: 0
}
```
# Métodos
O componente `App` define três métodos:

- addDigit(n): Adiciona um dígito ao valor exibido no visor. Se o dígito for um ponto e já houver um ponto no valor, nada é feito. Se o valor atual for 0, o visor é limpo antes de adicionar o dígito.
- clearMemory(): Limpa a memória da calculadora, restaurando o estado inicial.
- setOperation(operation): Define a operação a ser executada e atualiza o estado da calculadora de acordo com a operação selecionada.

# #Renderização
O componente `App` renderiza os componentes `Display` e `Botão` de acordo com o estado atual da calculadora. Os botões são organizados em uma grade com 4 colunas e várias linhas, usando o estilo definido no objeto `style`.
