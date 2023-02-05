# QUIZ039

## INSTRUCTIONS
![Screen Shot 2023-02-06 at 1 48 31](https://user-images.githubusercontent.com/111761417/216832643-80f93122-da65-49e7-a864-286f9aba56f3.png)

## CODE
```.py
#QUIZ039.py

from kivymd.app import MDApp

#Create class quiz039
class quiz039(MDApp):
    #initialize
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0

    #Create a method to build the screen
    def build(self):
        return
    #Create a method that sums one to the count every time the button is pressed.
    def change(self, name:str):
        if 'up' in name:
            self.count += 1

        self.root.ids.label.text = f"Count {self.count}"

#Run
demo_class = quiz039()
demo_class.run()
```

## KIVI FILE

```.py
#QUIZ039.kv

Screen:
    id: 500,500

    MDBoxLayout:
        id: main_box
        orientation: "horizontal"
        size_hint: .7, .3
        pos_hint: {"center_x":.5, "center_y":.5}
        md_bg_color: "#FFFFFF"

        MDLabel:
            id: label
            text: "Count"
            halign: "center"
            font_size: '34pt'
            size_hint: .5, 1

        MDRaisedButton:
            text: "+1"
            size_hint: .5, 1
            font_size: "34pt"
            md_bg_color: "#f07167"
            pos_hint: {"center_x":0.5}
            on_press: app.change("up")

```
## TEST
https://user-images.githubusercontent.com/111761417/216833460-986bc99d-5bcf-4ad3-99ee-3d45c5a58586.mov


