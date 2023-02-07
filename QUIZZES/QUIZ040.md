# QUIZ040

## INSTRUCTIONS

![Screen Shot 2023-02-07 at 2 46 23](https://user-images.githubusercontent.com/111761417/217046416-2a0a803b-17bc-4cdf-9ebb-ab432a772cf2.png)

## CODE
```.py
from kivymd.app import MDApp


class dark_light_mode(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)

    def build(self):
        return

    def change(self, mode):
        if mode == "light":
            self.root.ids.btn.text = "Dark Mode"
            self.root.ids.word.color = "#000000"
            self.root.ids.main_box.md_bg_color = "#FFFFFF"
            self.root.ids.btn.md_bg_color = "#73c5ff"

        elif mode == "dark":
            self.root.ids.btn.text = "Light Mode"
            self.root.ids.word.color = "#FFFFFF"
            self.root.ids.main_box.md_bg_color = "#000000"
            self.root.ids.btn.md_bg_color = "#00FF00"


demo_mode = dark_light_mode()
demo_mode.run()
```

## KIVY FILE

```.py
#dark_light_mode.kv

MDScreen:
    id: screen
    size: 500, 500

    MDBoxLayout:
        id: main_box
        size_hint: 1,1
        halign: "center"
        md_bg_color: "#FFFFFF"

        MDLabel:
            id: word
            font_style: "H2"
            text: "Maria Arias"
            color: "#000000"
            halign: "center"
            font_size: "60pt"

        MDRaisedButton:
            id: btn
            text: "Dark Mode"
            md_bg_color: "#73c5ff"
            pos_hint: {"center_x":0.5}
            on_press: app.change("dark")
```

## TEST


https://user-images.githubusercontent.com/111761417/217118514-d8d320d4-349a-4a05-b4b6-4b297c5afade.mov


