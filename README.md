def sumar(x, y):
    return x + y

def restar(x, y):
    return x - y

def multiplicar(x, y):
    return x * y

def dividir(x, y):
    if y == 0:
        return "Error: División por cero"
    return x / y

def calculadora():
    print("Bienvenido a la Calculadora en Python")
    print("Seleccione la operación:")
    print("1. Sumar")
    print("2. Restar")
    print("3. Multiplicar")
    print("4. Dividir")
    print("5. Salir")
    
    while True:
        try:
            opcion = int(input("Ingrese el número de la operación que desea realizar (1/2/3/4/5): "))

            if opcion == 5:
                print("Saliendo de la calculadora. ¡Hasta luego!")
                break

            if opcion not in [1, 2, 3, 4]:
                print("Opción inválida. Por favor, seleccione una opción válida.")
                continue

            # Solicitar números al usuario
            num1 = float(input("Ingrese el primer número: "))
            num2 = float(input("Ingrese el segundo número: "))

            # Realizar la operación seleccionada
            if opcion == 1:
                resultado = sumar(num1, num2)
                print(f"Resultado de la suma: {num1} + {num2} = {resultado}")
            elif opcion == 2:
                resultado = restar(num1, num2)
                print(f"Resultado de la resta: {num1} - {num2} = {resultado}")
            elif opcion == 3:
                resultado = multiplicar(num1, num2)
                print(f"Resultado de la multiplicación: {num1} * {num2} = {resultado}")
            elif opcion == 4:
                resultado = dividir(num1, num2)
                print(f"Resultado de la división: {num1} / {num2} = {resultado}")
        
        except ValueError:
            print("Entrada inválida. Por favor, ingrese números válidos.")
            
# Iniciar la calculadora
calculadora()
