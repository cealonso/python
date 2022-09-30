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

Realizar una calculadora que permita sumar dos números dados por teclado. Al finalizar el proceso imprimir el resultado de dicha suma.

    value1 = int(input('Enter first number: '))
    value2 = int(input('Enter second number: '))
    result = value1 + value2
    print(value1, value2, sep='+', end='=')
    print(result)


Programar un to-do list (Lista de cosas para hacer) que permita agregar tareas a una lista y a un archivo simuláaneamente. La cantidad de eventos a cargar se solicitará al usuario antes de proceder a la carga de la información. Por cada nuevo evento se debe cargar su descripción y se deberá almacenar en una nueva linea del archivo. Toda la información debe ser almacenada en un archivo denominado todo.txt almacenado en el mismo lugar donde se encuentra la aplicación.

    tasks=[]
    count=int(input("La cantidad de Eventos que quiero agendar : "))
    file=open("tareas.txt","w",encoding="utf8")
    for i in range(count):
        new_element=input("Que querés agendar? : ") #Se repite las count veces
        tasks.append(new_element)
        file.write(new_element+'\n')
    print(tasks)
    file.close()
    
Programar un to-do list (Lista de cosas para hacer) que permita agregar tareas a una lista y a un archivo simultáneamente. La cantidad de eventos a cargar se solicitará al usuario antes de proceder a la carga de la información. La aplicación debe mostrar su número de versión al ejecutarse por primera vez. Por cada nuevo evento se debe cargar su descripción, un color dependiendo de su prioridad (Rojo: Importante, Amarillo: Prioridad intermedia, Verde: Baja Prioridad). En el momento de cargar la prioridad se debe informar por pantalla los colores que puede completar el usuario para que ingrese correctamente la prioridad. La información sobre la prioridad no se debe agregar a la lista. Se debe generar un Id único correlativo para cada evento (ese id debe comenzar con el numero 1). También se debe almacenar la fecha de comienzo de la tarea y la fecha de finalización. La información sobre el id debe ser agregada al comienzo de la lista (Ejemplo: “1 Desayunar”), las fechas de comienzo y finalización no se deben agregar a la lista. Toda la información debe ser almacenada en un archivo denominado todo.txt almacenado en el mismo lugar donde se encuentra la app.  Cada información ingresada debe separarse en el archivo mediante una tabulación para mejorar la visualización cuando deba ser leído. 


    tasks=[]
    print ("Software TO-DO LIST v1.0")
    count=int(input("La cantidad de Eventos que quiero agendar : "))
    file=open("todo.txt","w",encoding="utf8")
    aux=0
    for i in range(count):
        aux=aux+1
        new_element=input("Que querés agendar? : ") #Se repite las count veces
        priority=input("Deme la prioridad (Rojo: Importante, Amarillo: Prioridad intermedia, Verde: Baja Prioridad)")
        date_start=input("Fecha de Comienzo")
        date_end=input("Fecha de Finalización")
        tasks.append(str(aux)+" "+new_element)
        file.write(str(aux)+"\t"+new_element+"\t"+priority+"\t"+date_start+"\t"+date_end+"\t"+'\n')
    print(tasks)
    file.close()

Realizar un ejercicio que indique si una persona tiene o no fiebre basado en su temperatura corporal.

    degree=float(input("Decime la temperatura : "))
    if degree>=37:
        print ("Tenés fiebre")
    else:
        print ("No pasa nada quédate tranquilo")
