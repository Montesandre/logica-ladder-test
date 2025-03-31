class Motor:
    def __init__(self):
        self.ligado = False

    def atualizar_estado(self, sensor1, sensor2):
        """
        Atualiza o estado do motor com base nos sensores.
        O motor só liga se ambos os sensores estiverem ativados.
        """
        self.ligado = sensor1 and sensor2

    def status(self):
        return "Ligado" if self.ligado else "Desligado"


def exibir_estado(sensor1, sensor2, motor):
    """Exibe o estado atual dos sensores e do motor."""
    estado_motor = motor.status()
    print(f"📡 Sensor 1: {'Ativado' if sensor1 else 'Desativado'} | "
          f"📡 Sensor 2: {'Ativado' if sensor2 else 'Desativado'} | "
          f"🚀 Motor: {estado_motor}")


# Criando o motor
motor = Motor()

# Cenários de teste
cenarios = [
    (False, False),  # Ambos desligados
    (True, False),   # Apenas um ligado
    (False, True),   # Apenas um ligado
    (True, True),    # Ambos ligados
    (True, False),   # Um desligando após ligado
]

print("Simulação do Motor com Sensores:\n")
for s1, s2 in cenarios:
    motor.atualizar_estado(s1, s2)
    exibir_estado(s1, s2, motor)
    print("-")
