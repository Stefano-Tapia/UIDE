import turtle

# 1. Configuración de la pantalla de juego
ventana = turtle.Screen()
ventana.title("Atari Pong")
ventana.bgcolor("black")
ventana.setup(width=800, height=600)
ventana.tracer(0) # Esto hace que el juego corra más fluido

# 2. Creación de la Paleta Izquierda (Jugador A)
paleta_a = turtle.Turtle()
paleta_a.speed(0)
paleta_a.shape("square")
paleta_a.color("white")
paleta_a.shapesize(stretch_wid=5, stretch_len=1) # Le damos forma de rectángulo
paleta_a.penup() # Evita que dibuje una línea al moverse
paleta_a.goto(-350, 0) # Posición en el lado izquierdo

# 3. Creación de la Paleta Derecha (Jugador B)
paleta_b = turtle.Turtle()
paleta_b.speed(0)
paleta_b.shape("square")
paleta_b.color("white")
paleta_b.shapesize(stretch_wid=5, stretch_len=1)
paleta_b.penup()
paleta_b.goto(350, 0) # Posición en el lado derecho

# 4. Creación de la Pelota
pelota = turtle.Turtle()
pelota.speed(0)
pelota.shape("square") # El Pong original usaba cuadrados
pelota.color("white")
pelota.penup()
pelota.goto(0, 0) # Empieza en el centro

# 5. Funciones para mover la paleta izquierda
def paleta_a_arriba():
    y = paleta_a.ycor() # Obtenemos la posición 'y' actual
    if y < 250:         # Límite para que no se salga de la pantalla
        paleta_a.sety(y + 20) # Sumamos 20 píxeles hacia arriba

def paleta_a_abajo():
    y = paleta_a.ycor()
    if y > -250:
        paleta_a.sety(y - 20) # Restamos 20 píxeles hacia abajo

# 6. Conectar el teclado con las funciones
ventana.listen()
ventana.onkeypress(paleta_a_arriba, "w")
ventana.onkeypress(paleta_a_abajo, "s")

# 7. Bucle principal del juego (Mantiene la ventana abierta)
while True:
    ventana.update() # Actualiza los gráficos en cada vuelta
