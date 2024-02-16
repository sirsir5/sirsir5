import math
import turtle

# Функции для расчета координат
def xt(t):
    return 16 * math.sin(t) ** 3

def yt(t):
    return 13 * math.cos(t) - 5 * math.cos(2 * t) - 2 * math.cos(3 * t) - math.cos(4 * t)

# Настройка окна и черепахи
turtle.colormode(255)
screen = turtle.Screen()
screen.bgcolor("black")
t = turtle.Turtle()
t.speed(0)  # Максимальная скорость

# Настройка цвета линии 
t.color("purple")

# Подготовка к рисованию
t.penup()
t.goto(xt(0) * 20, yt(0) * 20)
t.pendown()

# Рисование фигуры
for i in range(0, 2550, 1):
    t.goto(xt(i) * 20, yt(i) * 20)

t.hideturtle()  # Скрываем черепашку

turtle.done()  # Настройки закрытия окна
(No Title)
