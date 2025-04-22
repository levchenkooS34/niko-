<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Генерация кругов на Python</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
        }
        pre {
            background: #222;
            color: #0f0;
            padding: 15px;
            overflow-x: auto;
        }
        a {
            display: inline-block;
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Пример генерации кругов на Python с использованием tkinter</h1>
    <p>Вот пример кода, который рисует случайные круги на экране:</p>
    <pre>
from random import *
from tkinter import *

size = 600
root = Tk()
canvas = Canvas(root, width=size, height=size)
canvas.pack()
diapason = 0

while True:
    colors = choice(['aqua', 'blue', 'fuchsia', 'green', 'maroon', 'orange',
                     'pink', 'purple', 'red', 'yellow', 'violet', 'indigo',
                     'chartreuse', 'lime'])
    x0 = randint(0, size)
    y0 = randint(0, size)
    d = randint(0, size//5)
    canvas.create_oval(x0, y0, x0+d, y0+d, fill=colors)
    root.update()
    </pre>
    <a href="circle_generator.py" download>Скачать Python файл</a>
</body>
</html>
