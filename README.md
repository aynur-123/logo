# logo
kivy ile instagram logosu çizimi 
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.button import Button
import turtle

def degistir(nesne):
    nesne.text = "logo çizildi kapatın."
    turtle.bgcolor('medium violet red')

    turtle.pencolor('white')
    turtle.width(23)
    turtle.penup()
    turtle.goto(160, -100)
    turtle.pendown()
    turtle.left(90)
    turtle.end_fill()
    for i in range(4):
        turtle.forward(250)
        turtle.circle(34, 90)
    turtle.penup()
    turtle.goto(85, 30)
    turtle.pendown()
    turtle.circle(80, 360)
    turtle.penup()
    turtle.goto(110, 130)
    turtle.pendown()
    turtle.circle(7, 360)





class Uygulama(App):
    def build(self):
        self.title = "İNSTAGRAM LOGO"
        dugme=Button(text="BAŞLAMAK İÇİN DOKUN!")
        dugme.bind(on_press=degistir)
        dugme.background_color = "blue"


        return dugme

Uygulama().run()
