# 1. Actualizar valores en diccionarios y listas
matriz = [ [10, 15, 20], [6, 7, 14] ]
cantantes = [
    {"nombre": "Enrique Martin Morales", "país": "Puerto Rico"},
    {"nombre": "Chayanne", "país": "Puerto Rico"}
]

ciudades = {
    "México": ["Ciudad de México", "Guadalajara", "Monterrey"],
    "Chile": ["Santiago", "Concepción", "Viña del Mar"]
}

coordenadas = [
    {"latitud": 9.9355431, "longitud": -84.9399704}
]

# 2. Iterar a través de una lista de diccionarios
def iterarDiccionario(lista):
    for d in lista:
        salida = []
        for clave, valor in d.items():
            salida.append(f"{clave} - {valor}")
        print(", ".join(salida))

cantantes = [
    {"nombre": "Shakira", "país": "Colombia"},
    {"nombre": "Chappell Roan", "país": "Estados Unidos"},
    {"nombre": "Rosalía", "país": "España"},
    {"nombre": "Aurora", "país": "Noruega"}
]
iterarDiccionario(cantantes)

# 3. Obtener valores de una lista de diccionarios
def iterarDiccionario2(llave, lista):
    for d in lista:
        if llave in d:
            print(d[llave])

cantantes = [
    {"nombre": "Shakira", "país": "Colombia"},
    {"nombre": "Chappell Roan", "país": "Estados Unidos"},
    {"nombre": "Rosalía", "país": "España"},
    {"nombre": "Aurora", "país": "Noruega"}
]
iterarDiccionario2("nombre", cantantes)

iterarDiccionario2("país", cantantes)

# 4. Iterar a través de un diccionario con valores de lista
def imprimirInformacion(diccionario):
    for clave, lista in diccionario.items():
        print(f"{len(lista)} {clave.upper()}")
        for item in lista:
            print(item)
        print()

Japón = {
    "ciudades": ["Tokio", "Kioto", "Osaka", "Hiroshima"],
    "comidas": ["Sushi", "Ramen", "Takoyaki", "Okonomiyaki", "Tempura"]
}
imprimirInformacion(Japón)
