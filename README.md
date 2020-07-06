# Pac_DesarrolloInterfaces
Práctica Desarrollo de Interfaces.

Ilerna Games es una empresa de diseño de videojuegos y ha contactado con nosotros.
Nos comentan que su programador se ha puesto de baja y necesitan acabar urgentemente un juego. Consiste en realizar un tres en raya, y por suerte, tenemos la parte de diseño y la estructura del juego montada. Únicamente faltan rellenar los métodos y la parte lógica del juego.

Podremos observar que está dividido en dos partes:
• La parte gráfica Juego.java
• La parte funcional LogicaJuego.java

Utilizando el programa NetBeans finalizaremos este juego, os encontraréis que tenéis los métodos detallados con las funcionalidades que se esperan comentados dentro del proyecto, de todas formas, se van a explicar a continuación:

En la clase Juego.java
• Están declaradas de forma global la matriz y la clase LogicaJuego.
• iniciarJuego(): Es el método que inicializará una nueva partida, tendremos que llamar al método iniciarPartida de la clase LogicaJuego.java y vaciar los botones.
• clearButtons(): Vacía todos los botones para poder empezar una nueva partida.

Clase LógicaJuego.java
• De forma global están declaradas las variables turno, pX, pO
o Turno: Turno de cada jugador (0 o 1)
o pX: Turno de las “X”
o pO: Turno de las “O”
• getTurno(): Método que nos permite obtener el turno actual.
• cambioTurno(): Llamaremos a este método para cambiar de turno, es decir, si nos encontramos en el turno 1, que pase al turno 0 y viceversa.
• comprobarJuego(): Es una de las partes más importantes del juego, ya que sin este método no gana nadie. Aquí comprobaremos si alguno de los jugadores ha conseguido 3 en raya, se tendrá que comprobar de forma horizontal, vertical y diagonal.
• pintarFicha(): Pinta la ficha en el botón de juego visual, si nos encontramos en el turno 0, se tendrá que poner un fondo al texto de color rojo (Color.red) y el texto X, por otro lado, el turno 1 se pintará de color azul (Color.blue) y se insertará el texto O.
• ponerFicha(): Inserta la ficha en la matriz y llama al método adecuado para pintar la ficha en el botón.
• tiradaJugador(): En este método, deshabilitaremos el botón seleccionado para evitar que se vuelva a tirar en esa misma casilla, insertaremos la ficha en la matriz llamando al método adecuado y comprobaremos el ganador. Si existe ganador, se llamará al método adecuado para que nos incremente la puntuación de cada jugador y deshabilitará el tablero en caso de haber ganador. En caso contrario, cambiará de turno.
• ganador(): Método que actualizará la puntuación de cada jugador, y cambiará de turno para que la siguiente partida empiece el otro jugador.
• habilitarTrablero(): Habilitará o deshabilitará todos los botones dependiendo de la variable habilitado (setEnabled.(habilitado)), es decir, todos los componentes del Jpanel que recibirá por parámetro.
• iniciarPartida(): Inicializa una nueva partida, reinicia la matriz (Tablero de juego) y habilita el tablero.
