# EjerciciosDeOfertaLaboral
Ejercicio dado en una oferta laboral


Ejercicio de una oferta laboral: 

Una computadora comienza imprimiendo los números 2023, 2024 y 2025. Luego continúa imprimiendo sin parar la suma de los últimos 3 números que imprimió: 6072, 10121, 18218, … ¿Cuáles son los últimos 4 dígitos del número impreso en la posición 2023202320232023? Por ejemplo, en la posición 50, está impreso el número 8188013234823360 que termina en 3360. Por favor no olvides comentarnos cuál fue tu razonamiento para llegar al resultado.







def calcular_digitos(posicion):

    modulo = 10**4 #guardar 4 digitos finales

    

    a, b, c = 2023, 2024, 2025 #comienzo segun enunciado

    

    if posicion == 1:

        return a % modulo

    elif posicion == 2:

        return b % modulo

    elif posicion == 3:

        return c % modulo

    

    for _ in range(4, posicion + 1): #posicion 4

        proximo = (a + b + c) % modulo

        a, b, c = b, c, proximo

    

    return c



posicion = 2023202320232023  #posicion pedida

resultado = calcular_digitos(posicion)

print(f"Los últimos 4 dígitos en la posición {posicion} son: {resultado}")







Lo que usé fue el bucle for, la operación modulo y condicionales.-
