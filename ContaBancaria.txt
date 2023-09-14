class ContaBancaria:
    def __init__(self, numero, titular, saldo, limite):
        self.numero = numero
        self.titular = titular
        self.saldo = saldo
        self.limite = limite

    def deposita(self, valor):
        self.saldo += valor

    def saca(self, valor):
        if valor <= self.saldo:
            self.saldo -= valor
        else:
            print("Saldo insuficiente!")

    def extrato(self):
        print("Número da conta:", self.numero)
        print("Saldo:", self.saldo)

# Exemplo de uso da classe:

minha_conta = ContaBancaria(305012, 'ADRIELE', 3050.0, 6100.0)
minha_conta.extrato()
minha_conta.deposita(400.0)
minha_conta.extrato()
minha_conta.saca(210.0)
minha_conta.extrato()
minha_conta.saca(500.0)
