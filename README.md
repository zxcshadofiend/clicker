from tkinter import *
import pygame, time, threading, random, json

pygame.init()
window = Tk()
window.geometry('600x600')
window.title('Кликер')
window['bg'] = '#F5DEB3'
window.resizable(width=False, height=False)

#логика проекта
click = 0

def clicker():
    global click
    click += 1
    label_click.config(text = str(click))

#создание виджетов
but_click = Button(window,
                   text = 'Нажми',
                   width = 15,
                   height = 3,
                   bg = '#FF0000',
                   fg = '#00FFFF',
                   font = 'Arial 14',
                   command = clicker)

label_click = Label(window,
                   text = '0',
                   width = 15,
                   height = 3,
                   bg = '#FF69B4',
                   fg = '#8B0000',
                   font = 'Arial 14')

label_click.place(x =212, y =20)
but_click.place(x = 210, y = 100)
mainloop()
