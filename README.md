import turtle
from turtle import *

# Mensaje inicial
message = "Te amo más que nadie y todo va a estar bien"

# Configuración inicial de Turtle para el mensaje
turtle.bgcolor("white")
pen = turtle.Turtle()
pen.color("black")
pen.penup()
pen.goto(-150, 0)
pen.write(message, font=("Arial", 14, "normal"))
pen.hideturtle()

# Pausa para que se vea el mensaje antes de la rosa
turtle.delay(2000)  # Espera 2 segundos

# Limpiar la pantalla
turtle.clear()

# Configuración para dibujar la rosa
turtle.bgcolor("white")
pen = turtle.Turtle()
pen.speed(2)
pen.color("red")

# Función para dibujar una pétalo de rosa
def draw_petal():
    pen.circle(50, 60)
    pen.left(120)
    pen.circle(50, 60)
    pen.left(120)

# Dibujar una rosa con varios pétalos
for _ in range(6):
    draw_petal()

# Mover la pluma fuera de la rosa
pen.penup()
pen.goto(0, -200)
pen.pendown()

# Dibujar el tallo de la rosa
pen.color("green")
pen.pensize(5)
pen.right(90)
pen.forward(200)

# Mensaje final
pen.penup()
pen.goto(-150, -250)
pen.color("black")
pen.write("Espero que te haya gustado la rosa. ¡Te amo!", font=("Arial", 12, "normal"))
pen.hideturtle()

# Mostrar la ventana
turtle.done()

