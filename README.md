# Cacho

## Reglamento oficial Titiribí

**Cacho** es un juego de dados de 4 jugadores(3CPU, 1 Humano) donde se toman turnos haciendo **suposiciones** de las cantidades de valores de dados que hay en total sabiendo solo el valor de sus 5 dados iniciales.

El juego comienza con cada jugador lanzando us dados y usando esta **'mano'** para su beneficio.

El jugador que perdió el juego anterior empieza con su suposicion , el primer juego lo comienza HUM.

La **suposicion** consiste de una cantidad(Desde 1 hasta el total de dados en juego) y un valor(1,2,3,4,5,6, que son los valores de las caras de un dado).
Si el siguiente jugador  cree que la suposicion podria ser verdad debe hacerle una suposicion al jugador de su derecha aumentado minimo por 1 la cantidad de dados o el valor y esto dara por terminado el turno actual. De no creer en esa suposicion actual, se hacen visibles todos los dados en juego y el jugador que esta equivocado pierde un dado. Esto hara que comience una nueva ronda.

El **#1** es un comodín.

* Comodín a numeros:
    *Se multiplica la cantidad de comodines *2 de la suposicion + 1.*

* Numeros a comodin:
    *Se divide la cantidad de comodines /2 de la suposicion + 1.*


## Flujo e interfaz

1. Escribir *'cacho'* en la terminal

2. Se muestra la mano del jugador y el numero total de dados en juego.

    * 
    20

    CPU1 * * * * *
    CPU2 * * * * * 
    CPU3 * * * * *
    HUM  3 4 4 4 2 

3. Se espera el turno para recibir una suposicion o si se comienza se hace una suposicion.

    *  CPU2 3 4
       CPU3 3 5
       Escribe una suposicion(cantidad, valor dado) o si crees que la ultima suposicion es poco probable escribe cacho para revelar las manos de todos.

    * Escribe una suposicion(cantidad, valor dado)

4. Cuando alguien escribe cacho se deben mostrar todos los dados, mostrar quien pierde un dado y el nuevo total.

    *  CPU1 3 4 5
       CPU2 4 5 5 2 3
       CPU3 4 5
       HUM 3 4 4

       CPU3 -1

       12 Dados

5. Regresar al paso #2 hasta que HUM pierda sus 5 dados o eventualmente gane, cerrar el programa.

## Pseudocódigo

* Crear las 4 manos de los jugadores en una funcion que utilice un generador
aleatorio los valores de los dados de los jugadores. Inicialmente 5. Debe haber
una variable que almacene las cantidades de los dados de los jugadores mientras
el juego va cambiando.

En la primer ventana se debe mostrar los 4 jugadores y el total de dados en juego.



vector turn
vector hand
int totalDice

Class jugador
    Constructor

    Destructor

    Propiedades
        Humano o CPU
        diceNum
        hand
    

funcion hand (diceNum) {
    random(diceNum)
    push a hand
}

funcion play () {
    prompt cant y valor
    checkear que si cumplan las condiciones
        int, que esten en el rango de dados disponibles, 1-6
    CPU de acuerdo a su logica genera una suposicion

}

function aceChecker () {
    if ace -> num then (quantity * 2) + 1
    if num -> ace then (quantity / 2) + 1
}



**Logica CPU**

Estadistica de probabilidad?
Intentar reconocer patrones de los demas
Como nada es verdad puede quee esta ultima pueda ser inutil
pasado cierto valor siempre decir cacho
irse por un valor o ir cambiando por diferentes valores













<!-- 1) Escribir bien las reglas
-> Manual de juegos de mesa
2) Describir como el gameplay, el flujo y la interfaz que leo, que veo, en que momento escribo
3) Diseñar el programa en pseudocodigo, en ingles, lo que sea

4.1) Escribir tests. TDD.
4.2) Escribir el codigo. -->





