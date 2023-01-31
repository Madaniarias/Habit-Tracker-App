# GUI Building Tasks

## Instrutions

1. Create a file inside your repository called "gui_task.md"
2. Reproduce the Examples inside the slide
3. Solve the Task 1 if you are SL and Task1 and Task 2 if you are HL

## Reproducing examples

## Example 1

### Python file

```.py
from kivymd.app import MDApp

class example1(MDApp):
    def build(self):
        return

test = example1()
test.run()
```

### Kivy file

```.py

Screen:
    size: 500, 500

    MDLabel:
        text: "Hello World"
        halign: "center"
        font_size: "34pt"
```

### Test 

![Screen Shot 2023-01-31 at 16 37 46](https://user-images.githubusercontent.com/111761417/215696231-9c8838d4-067e-45f5-bf4b-69ebdf06ad30.png)

## Example 2

### Python file

```.py

from kivymd.app import MDApp

class example2(MDApp):
    def build(self):
        return
    def close(self):
        exit()

test = example2()
test.run()

```

### Kivy file

```.py
Screen:
    size: 500,500
    MDBoxLayout:
        pos_hint: {"center_x":0.5}
        size_hint: .7,.7
        md_bg_color: "#fdfcdc"
        orientation: "vertical"

        MDLabel:
            text: "Hello World"
            halign: "center"
            font_size: "34pt"

        MDRaisedButton:
            text: "Close"
            size_hint: .5, 1
            font_size: "34pt"
            md_bg_color: "#f07167"
            pos_hint: {"center_x":0.5}
            on_press:
                app.close()

```

### Test

![Screen Shot 2023-01-31 at 16 42 02](https://user-images.githubusercontent.com/111761417/215697117-085bfc70-e336-457b-b245-c7eebb459bc4.png)

## Example 3

### Python file

```.py
from kivymd.app import MDApp

class example3(MDApp):
    def build(self):
        return
    def change_author(self,name):
        self.root.ids.title.text = f"Author{name}"

test = example3()
test.run()
```

### Kivy file

```.py
Screen:
    size: 500, 500
    MDLabel:
        id: title
        text: ""
        font_style: "H1"
        pos_hint: {"center_y":.8}
        halign: "center"

    MDBoxLayout:
        pos_hint: {"center_x":.5,"center_y":.5}
        size_hint: .7, .2
        orientation: "horizontal"

        MDChip:
            text: "Author A"
            pos_hint: {"center_y": .5}
            icon_right: "close-circle-outline"
            md_bg_color: "#003049"
            text_color: "#FFFFFF"
            on_press: app.change_author("A")

        MDChip:
            text: "Author B"
            pos_hint: {"center_y": .5}
            icon_right: "close-circle-outline"
            md_bg_color: "#D62828"
            on_press: app.change_author("B")

        MDChip:
            text: "Author C"
            pos_hint: {"center_y":.5}
            icon_right: "close-circle-outline"
            md_bg_color: "#F77F00"
            on_press: app.change_author("C")

        MDChip:
            text: "Author D"
            pos_hint: {"center_y":.5}
            icon_right: "close-circle-outline"
            md_bg_color: "#FCBF49"
            on_press: app.change_author("D")

        MDChip:
            text: "Author E"
            pos_hint: {"center_y":.5}
            icon_right: "close-circle-outline"
            md_bg_color: "#EAE2B7"
            on_press: app.change_author("E")

```

### Test

![Screen Shot 2023-01-31 at 16 40 07](https://user-images.githubusercontent.com/111761417/215697095-1f9e0f50-403e-4163-b739-ab7a0b1d3e55.png)



