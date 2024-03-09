# Sistema_Conta_Bancaria_POO
# Documentação Técnica

## Classe Cliente

A classe `Cliente` representa um cliente no sistema bancário. Ela possui dois atributos:

- `nome`: uma string que representa o nome do cliente.
- `cpf`: uma string que representa o CPF do cliente.

## Classe Conta

A classe `Conta` representa uma conta bancária genérica. Ela possui três atributos:

- `cliente`: um objeto da classe `Cliente` que representa o dono da conta.
- `numero`: um número que representa o número da conta.
- `saldo`: um número que representa o saldo atual da conta.

A classe `Conta` também possui os seguintes métodos:

- `sacar(valorSaque)`: este método tenta sacar um determinado valor da conta. Se o saldo for suficiente e o valor do saque for maior que zero, o saque é realizado e o método retorna `true`. Caso contrário, o método retorna `false`.
- `depositar(valorDeposito)`: este método tenta depositar um determinado valor na conta. Se o valor do depósito for maior que zero, o depósito é realizado e o método retorna `true`. Caso contrário, o método retorna `false`.
- `transferir(valorTransferencia, contaDestino)`: este método tenta transferir um determinado valor para outra conta. Se a transferência for bem-sucedida, o método retorna `true`. Caso contrário, o método retorna `false`.

## Classe ContaCorrente

A classe `ContaCorrente` é uma subclasse de `Conta` que representa uma conta corrente. Ela possui um atributo adicional:

- `limiteChequeEspecial`: um número que representa o limite do cheque especial para a conta.

A classe `ContaCorrente` também sobrescreve o método `sacar(valorSaque)` da classe `Conta`. Neste caso, o saque é permitido se o valor do saque for menor ou igual ao saldo mais o limite do cheque especial.

## Classe ContaPoupanca

A classe `ContaPoupanca` é uma subclasse de `Conta` que representa uma conta poupança. Ela possui um atributo adicional:

- `taxaRendimento`: um número que representa a taxa de rendimento da conta.

A classe `ContaPoupanca` também possui um método adicional:

- `aplicarRendimento()`: este método aplica o rendimento ao saldo da conta, de acordo com a taxa de rendimento.

## Funções Auxiliares

O código também inclui várias funções auxiliares para manipular clientes e contas, como `cadastrarCliente()`, `exibirClientes()`, `atualizarSeletorClientes()` e `cadastrarConta()`.
