# Android Crypyo-Monitor
Aplicativo Android criado com Kotlin durante as aulas de desenvolvimento mobile. O projeto tem como propósito principal exibir ao usuário a cotação atualizada do Bitcoin em tempo real, por meio de uma requisição feita a uma API pública de criptomoedas.
# 🏠 Tela inicial do aplicativo
![image](https://github.com/user-attachments/assets/ed7a2ea2-d87e-484c-99aa-f636383115f5)

# Depois de clicar no botão "ATUALIZAR"
![image](https://github.com/user-attachments/assets/79a94589-bbcd-487a-a2f3-4201c9b17b16)

# ❓ Sobre o aplicativo
O android-cryptomonitor é um aplicativo Android desenvolvido para exibir a cotação do Bitcoin em tempo real. Ao tocar no botão "Atualizar", o app recupera e exibe instantaneamente o valor mais recente do Bitcoin, além de mostrar a data e o horário da última atualização. Dessa forma, o usuário tem sempre acesso à cotação atualizada e sabe exatamente quando a informação foi consultada pela última vez.

O aplicativo utiliza a API do Mercado Bitcoin para obter a cotação atual da criptomoeda.

As respostas no formato JSON são convertidas em objetos Kotlin utilizando o Gson, uma biblioteca desenvolvida pelo Google para manipulação eficiente de dados JSON.

# 🔄 Lógica de Funcionamento
1. Inicialização
Na inicialização (onCreate), o app configura a Toolbar e o botão de atualização.

2. Atualização de Dados

 Quando o botão "Atualizar" é clicado, o método makeRestCall() é chamado:

- Realiza uma chamada assíncrona à API https://www.mercadobitcoin.net/api/BTC/ticker/ usando Retrofit.

- Extrai o valor atual (last) e a data (date) do Bitcoin.

- Formata o valor com NumberFormat para a moeda brasileira (R$).

- Exibe mensagens de erro caso a chamada falhe ou retorne códigos HTTP conhecidos.

3. Interface Retrofit

![image](https://github.com/user-attachments/assets/b4cbc1eb-1586-4949-9e54-9ce9a7f4d556)


- A interface define o endpoint utilizado para buscar os dados do BTC.

# 📌 Possíveis Melhorias Futuras
Exibir mais informações como volume, high/low, etc.

Gráfico de histórico de preços.

Suporte a múltiplas criptomoedas.

