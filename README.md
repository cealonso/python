# Ejercicios de Python

Realizar un programa de logística que permita almacenar:

- Cantidad total de vehículos disponibles (buses).
- Total de asientos disponibles por micro (space_in_a_bus)

 y luego a través de estas variables calcule la cantidad total de personas que pueden transportar(count_persons_seats). 
 
 Finalmente se solicita mostrar dicho valor por pantalla.

    buses=100
    space_in_a_bus=20
    count_persons_seats=buses*space_in_a_bus
    print(" Cantidad total de personas por micro es:", count_persons_seats)

Analice la siguiente situación: Se lleno por error el vaso de Nicolás con gaseosa Coca-Cola mientras que el vaso de Juliana se llena tambien por error con la gaseosa Fanta Naranja. El problema es que a Juliana le gusta la gaseosa Coca-Cola y a Nicolás la gaseosa Fanta Naranja. Cada uno no quiere tomar el vaso del otro. ¿Cómo haría para que en el vaso de Nicolás tenga Fanta Naranja y en el vaso de juliana tenga Coca-Cola sin tirar ambas gaseosas y volver a llenar los vasos?.

    vaso_juliana="Fanta"
    vaso_nico="Coca-cola"
    temp=vaso_juliana # paso fanta a temp el vaso de juliana esta vacio
    vaso_juliana=vaso_nico # paso a juliana la coca de nico
    vaso_nico=temp   # paso a nico lo que habia en temp o sea fanta
    print("El vaso de Nico tiene: ", vaso_nico)
    print("El vaso de Juliana tiene: ", vaso_juliana)

Realizar una calcular que permita sumar dos números dados por teclado:

    value1 = int(input('Enter first number: '))
    value2 = int(input('Enter second number: '))
    result = value1 + value2
    print(value1, value2, sep='+', end='=')
    print(result)
