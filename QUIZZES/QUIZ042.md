# QUIZ042

## INSTRCUTIONS
![Screen Shot 2023-02-28 at 9 46 03](https://user-images.githubusercontent.com/111761417/221722984-b480c145-cd4f-438c-9d76-ba7374c50fe0.png)

## CODE

### PYTHON CODE
```.py
# quiz42

from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen


class MysteryPageA(MDScreen):
    def message1(self):
        self.ids.A_box.text = "This is mystery page A you pressed the button"
        print(f"This is mystery page A you pressed the button")


class MysteryPageB(MDScreen):
    def message2(self):
        print("This is mystery page B you pressed the button")
        self.ids.B_box.text = "This is mystery page B you pressed the button"


class quiz42(MDApp):
    def build(self):
        return


quiz_test = quiz42()
quiz_test.run()
```
### KIVY CODE
```.py
#quiz42

ScreenManager:
    MysteryPageA:
        name: "MysteryPageA"

    MysteryPageB:
        name: "MysteryPageB"

<MysteryPageA>:
    name: "MysteryPageA"
    MDBoxLayout:
        size_hint: 1,1
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"
        spacing: dp(10)
        padding: dp(10)
        md_bg_color: "7FB3D5"

        MDBoxLayout:
            size_hint: 1,.8
            pos_hint: {"center_x":.5, "center_y":.5}

            MDLabel:
                id: A_box
                text: "Press the button"
                size_hint: 1,1
                halign: "center"
                valign: "center"
                font_size: "55pt"

        MDRaisedButton:
            size_hint: 1,.2
            text: "Go to Page B"
            font_size: "30pt"
            md_bg_color: "A569BD"
            pos_hint: {"center_x":.5, "center_y":.5}
            on_press: root.message1()
            on_press: app.root.current = "MysteryPageB"



<MysteryPageB>:
    name: "MysteryPageB"
    MDBoxLayout:
        size_hint: 1,1
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"
        spacing: dp(10)
        padding: dp(10)
        md_bg_color: "73C6B6"

        MDBoxLayout:
            size_hint: 1,.8
            pos_hint: {"center_x":.5, "center_y":.5}

            MDLabel:
                id: B_box
                text: "This is mystery page B you pressed the button"
                size_hint: 1,1
                font_size: "55pt"
                halign: "center"
                valign: "center"

        MDRaisedButton:
            size_hint: 1,.2
            text: "Go to Page A"
            font_size: "30pt"
            md_bg_color: "A569BD"
            pos_hint: {"center_x":.5, "center_y":.5}
            on_press: root.message2()
            on_press: app.root.current = "MysteryPageA"
```
## TEST

https://user-images.githubusercontent.com/111761417/227700958-c351e155-3db5-4c80-a5d4-7dc968ed336a.mov


