# writeup-three

Primeiro vamos começar com a enumeração, como sempre.


alvo: 10.129.254.11

Primeiro, vamos começar com a enumeração, como sempre, iremos fazer um scan para verificar portas abertas.

![image](https://github.com/user-attachments/assets/8bc8f8f3-219a-4938-9238-bb72414e86b5)

encontramos duas portas abertas, a porta 22, padrão para ssh e a porta 80, http.

Vamos ver oq tem rodando na porta 80

![image](https://github.com/user-attachments/assets/0f3528d2-ee1b-427d-a64e-1bf0c59be563)

Ao analisar, vemos que é uma página estática que apresenta uma seção de reserva de ingressos para shows, mas ão está funcional. O código fonte da página revela que o formulário "Contato" envia solicitações para uma página php, /action_page.php, indicando que obackend do servidor para essa aplicação é em php

![image](https://github.com/user-attachments/assets/7e84e956-e84d-4a80-9653-b862a0f5b5f1)

na seção de contato, tem um email com o thetoppers.htb

![image](https://github.com/user-attachments/assets/fe4d2007-055e-4fa2-8580-869499186be5)

Se acionarmos no /etc/host junto com o ip podemos acessar. O arquivo /etc/hosts é usado para mapear nomes de domínio para endereços ip. Por padrão, esse arquivo é consultado antes do servidor DNS para resolver nomes

![image](https://github.com/user-attachments/assets/30c8d250-177c-4da5-bb21-9e1cbb6037dd)

