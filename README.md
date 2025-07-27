# Cifra de Vernam

Este repositório contém a implementação de um site simples para demonstrar o funcionamento da Cifra de Vernam, um dos métodos criptográficos mais seguros conhecidos.

## Sobre a Cifra de Vernam

A Cifra de Vernam, também conhecida como "One-Time Pad" (OTP), é um algoritmo de criptografia que garante segurança incondicional, ou seja, é matematicamente impossível de ser quebrado se algumas condições essenciais forem seguidas:

1.  **Chave Aleatória:** A chave (pad) utilizada deve ser verdadeiramente aleatória.
2.  **Chave Única:** A chave deve ser usada apenas uma única vez para uma única mensagem.
3.  **Chave Secreta:** A chave deve ser mantida em segredo absoluto entre o remetente e o destinatário.
4.  **Chave do Mesmo Tamanho da Mensagem:** A chave deve ter o mesmo comprimento da mensagem a ser criptografada.

O processo de criptografia e descriptografia da Cifra de Vernam envolve a operação lógica XOR (OU Exclusivo) entre a representação binária da mensagem e a chave.

### Como Funciona

* **Criptografia:** Cada bit da mensagem original é combinado com o bit correspondente da chave usando a operação XOR. O resultado é o bit da mensagem cifrada.
    * `Mensagem XOR Chave = Mensagem Cifrada`
* **Descriptografia:** O mesmo processo é aplicado à mensagem cifrada usando a *mesma chave*. A operação XOR tem a propriedade de ser sua própria inversa, o que significa que aplicar XOR duas vezes com a mesma chave retorna ao valor original.
    * `Mensagem Cifrada XOR Chave = Mensagem Original`

A segurança incondicional da Cifra de Vernam deriva do fato de que, se a chave for verdadeiramente aleatória, do mesmo tamanho da mensagem e usada apenas uma vez, cada possível mensagem decifrada é igualmente provável, tornando impossível para um atacante determinar qual é a mensagem original sem a chave.

## Estrutura do Site

O site é composto por três páginas principais:

* **`index.html`**: Página inicial que apresenta a Cifra de Vernam e as opções para criptografar ou descriptografar.
* **`criptografar.html`**: Permite ao usuário inserir uma mensagem e gerar sua versão cifrada em binário, juntamente com a chave binária aleatória utilizada.
* **`descriptografar.html`**: Permite ao usuário inserir uma mensagem cifrada binária e a chave binária correspondente para revelar a mensagem original.

## Projeto de

Este projeto foi desenvolvido como parte de um trabalho acadêmico pela aluna **Vanessa da Rocha Taufer**, sob a orientação do professor **Amarildo de Vicente**.
