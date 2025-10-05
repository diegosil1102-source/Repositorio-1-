# Repositorio-1-
Inteligencia artificial 
# Neurona McCulloch-Pitts - Operación OR

# Entradas posibles de la compuerta OR
entradas = [
    (0, 0),
    (0, 1),
    (1, 0),
    (1, 1)
]

# Pesos de la neurona (uno por cada entrada)
w1 = 1
w2 = 1

# Umbral (θ)
theta = 1

# Función de activación (función escalón)
def activacion(suma):
    if suma >= theta:
        return 1
    else:
        return 0

print("x1 | x2 | Salida")
print("-----------------")

# Calcular la salida para cada combinación
for x1, x2 in entradas:
    suma = w1*x1 + w2*x2
    salida = activacion(suma)
    print(f" {x1} |  {x2} |   {salida}")


# Esta neurona simula la operación lógica OR, que da como resultado 1 cuando al menos una de las entradas es 1.
# Los pesos (w1 y w2) indican la importancia de cada entrada.
# Si la suma de las entradas ponderadas alcanza o supera el umbral (θ), la neurona “se activa” (salida = 1).
# En caso contrario, la salida es 0.
