# GUI Building Tasks

## Instrutions

1. Create a file inside your repository called "gui_task.md"
2. Reproduce the Examples inside the slide
3. Solve the Task 1 if you are SL and Task1 and Task 2 if you are HL

## Reproducing examples

## Example 1

### Python file

'''.py
from kivymd.app import MDApp

class example1(MDApp):
    def build(self):
        return

test = example1()
test.run()
'''

### Kivy file

'''.py

Screen:
    size: 500, 500

    MDLabel:
        text: "Hello World"
        halign: "center"
        font_size: "34pt"
'''

