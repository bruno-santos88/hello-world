# Exercício 1 - Programa em Phython que calcule o IMC
peso = float(input('qual seu peso? '))
altura = float(input('qual sua altura? '))

imc = peso / (altura**2)

print (f"Seu imc é: {imc}")

# Exercício 2 - Criar lista para inserção de 5 itens

lista = []

lista.append(int(input("num 1:")))
lista.append(int(input("num 2:")))
lista.append(int(input("num 3:")))
lista.append(int(input("num 4:")))
lista.append(int(input("num 5:")))

lista

# Alerta com notification.notify()

from plyer import notification


def alerta(nivel,
           base,
           etapa):
    nivel_do_alerta = ""
    if nivel == 1:
        nivel_do_alerta = "Alerta Baixo"
    elif nivel == 2:
        nivel_do_alerta = "Alerta Médio"
    elif nivel == 3:
        nivel_do_alerta = "Alerta Alto"
    else:
        nivel_do_alerta = "N/A"


    titulo = nivel_do_alerta
    data_atual = datetime.datetime.now().strftime("%d/%m/%Y %H:%M:%S")

    notification.notify(
        title=titulo,
        message=f"Falha no carregamento da base {base} na etapa {etapa} " + data_atual)


alerta(nivel=3, base="CLIENTES", etapa="EXTRACAO")
