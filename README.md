# Cacho

## Reglamento oficial Titiribí

**Cacho** es un juego de dados de 4 jugadores(3CPU, 1 Humano) donde se toman turnos y cada jugador hace **suposiciones** de las cantidades de valores de dados que hay en total sabiendo solo el valor de sus 5 dados iniciales.

El juego comienza con cada jugador lanzando sus dados y usando esta **'mano'** para su beneficio.

El jugador que perdió el juego anterior empieza con su suposicion , el primer juego lo comienza Humano.

La **suposicion** consiste de una cantidad(Desde 1 hasta el total de dados en juego) y un valor(1,2,3,4,5,6, que son los valores de las caras de un dado).

Ej: Hay 4 3 en la mesa. Esto quiere decir que el jugador esta suponiendo que hay 4 dados con el valor 3 en todos los dados de la mesa.

Si el siguiente jugador  cree que la suposicion podria ser verdad debe hacerle una suposicion al jugador siguiente aumentado minimo por 1 la cantidad de dados o el valor y esto dara por terminado el turno actual. De no creer en esa suposicion actual el jugador debe decir *cacho* y se hacen visibles todos los dados en juego y el jugador que esta equivocado pierde un dado. Esto hara que comience una nueva ronda.


<!-- corrección sección comodínes -->
**Comodín**

El valor **1** es un comodín. Esto quiere decir que un dado que tenga el valor **1** toma el valor de la suposicion. En ocasiones nos conviene cambiar la suposicion de un valor regular(2,3,4,5,6) a comodines por nuestros dados. Para realizar esto debemos tener en cuenta:

* Convertir de Comodín a numeros:

    *Se multiplica la cantidad de comodines *2 de la suposicion + 1.*

    Ej: CPU3 4 1
        HUM  9 5
    
    En este caso el Humano multiplicó la cantidad dada por CPU3 por 2 y le sumó 1((4 * 2) + 1 = 9). Luego le asigno el valor de 5. Este valor puede ser cualquier valor regular(2,3,4,5,6).

* Numeros a comodin:

    *Se divide la cantidad de comodines /2 de la suposicion + 1.*

    Ej: CPU2 6 3
        HUM  4 1

    En este caso el Humano dividió la cantidad dada por CPU2 en 2 y le sumó 1((6 / 2) + 1 = 4). Luego le asigno el valor de 1, que es el valor de comodín.  

*nota: En caso tal que la cantidad no sea divisible por 2 en numeros enteros, se redondea hacia arriba(ceil).*

## Flujo e interfaz

1. Escribir `cacho` en la terminal

2. Se muestra la mano del jugador y el numero total de dados en juego.

    Estas jugando cacho con 3 oponentes CPU tus dados son:
    HUMANO  3 4 4 4 2 
    
    Hay 20 dados en al mesa.

    CPU1 * * * * * 5 dados
    CPU2 * * * * * 5 dados
    CPU3 * * * * * 5 dados

3. El humano comienza con su suposicion.

    * Escribe una suposicion el primer numero indica la cantidad de dados y el segundo numero su valor. 

    Ej: 4 3
    

4. Cuando alguien escribe `cacho` se deben mostrar todos los dados, mostrar quien pierde un dado y el nuevo total.

    *  CPU1 3 4 5
       CPU2 4 5 5 2 3
       CPU3 4 5
       HUM 3 4 4

       CPU3 -1

       Ahora quedan 19 dados.
       Se lanzan los dados nuevamente.
    

5. Regresar al paso #2 hasta que Humano pierda sus 5 dados o gane, cerrar el programa.

## Pseudocódigo

<!-- Siga con el main para llamar las funciones, todavia no ir a escribir las funciones, despues de que me de cuenta de como tienen que ser ahi si las escribo  -->


int main () {
     imprimirMsjInicio();
     contadorDados();
     generarValoresDados();

     

     controlarTurnos();
        leerSuposicion();
        generarSuposicion();

     revisarCacho();

     nuevaRonda();
     
     Ejecutar hasta que Humano pierda.
}














void imprimirMsjInicio (numOponentes) {
    std::string msj = "Estas jugando cacho con  numOponentes CPU tus dados son:";
    cout << msj;  


    <!-- HUMANO  3 4 4 4 2 
    
    Hay 20 dados en al mesa.

    CPU1 * * * * * 5 dados
    CPU2 * * * * * 5 dados
    CPU3 * * * * * 5 dados -->
    
}


Class jugador
    Constructor

    Destructor

    Propiedades
        string Humano o CPU
        int diceNum
        vector int valores
    

vector int function generarValores (diceNum) {
    vector int valores
    random(diceNum)
    push a valores
    return valores
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


<!-- Code formatter
Post del mouse
Verbos
Funciones brutas, puras
Variables globales
Anecdota -->











<!-- 1) Escribir bien las reglas
-> Manual de juegos de mesa
2) Describir como el gameplay, el flujo y la interfaz que leo, que veo, en que momento escribo
3) Diseñar el programa en pseudocodigo, en ingles, lo que sea

4.1) Escribir tests. TDD.
4.2) Escribir el codigo. -->





