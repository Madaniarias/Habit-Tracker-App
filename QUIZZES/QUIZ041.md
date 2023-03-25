# QUIZ041

## INSTRUCTIONS
![Screen Shot 2023-02-28 at 9 42 40](https://user-images.githubusercontent.com/111761417/221722596-9aee9b01-63ff-4196-8c27-627898dce29a.png)

## CODE

### PYTHON CODE
# quiz 41

from kivymd.app import MDApp


class quiz41(MDApp):

    def __init__(self, **kwargs):
        super().__init__(**kwargs)

    def build(self):
        return

    turn = "x"

    def change_turn(self, click):
        if self.turn == "x":
            click.text = "x"
            click.disabled = True
            click.md_bg_color_disabled = "F9E79F"
            self.root.ids.turn_text.text = "It is o's Turn"
            self.turn = "o"

        else:
            click.text = "o"
            click.disabled = True
            click.md_bg_color_disabled = "D5F5E3"
            self.root.ids.turn_text.text = "It is x's Turn!"
            self.turn = "x"


test = quiz41()
test.run()

### KIVY CODE

Screen:
    size: 500,500
    MDBoxLayout:
        id: main box
        orientation: "vertical"
        size_hint: 1,1
        pos_hint: {"center_x":.5, "center_y":.5}
        spacing: dp(10)
        padding: dp(10)

        MDBoxLayout:
            id: name_box
            orientation: "vertical"
            pos_hint: {"center_x":.5, "center_y":.5}
            size_hint: 1, .15
            md_bg_color: "#2980B9"

            MDLabel:
                id: name_text
                text: "Tic Tac Toe by Maria"
                font_style: "H3"
                halign: "center"
                font_size: "27pt"

        MDBoxLayout:
            id: turn_box
            orientation: "vertical"
            pos_hint: {"center_x":.5, "center_y":.5}
            size_hint: 1, .15
            md_bg_color: "#3498DB"

            MDLabel:
                id: turn_text
                text: "It is x's Turn!"
                font_style: "H3"
                halign: "center"
                font_size: "27pt"

        MDBoxLayout:
            orientation: "vertical"
            size_hint: 1,1
            pos_hint: {"center_x":.5, "center_y":.5}

            MDBoxLayout:#row1
                orientation: "horizontal"
                size_hint: .7,.8
                pos_hint: {"center_x":.5, "center_y":.5}
                md_bg_color: "D35400"
                spacing: dp(10)
                padding: dp(10)

                MDRaisedButton:
                    id: square1_1
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square1_1)

                MDRaisedButton:
                    id: square1_2
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square1_2)

                MDRaisedButton:
                    id: square1_3
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square1_3)

            MDBoxLayout:#row2
                orientation: "horizontal"
                size_hint: .7,.8
                pos_hint: {"center_x":.5, "center_y":.5}
                md_bg_color: "D35400"
                spacing: dp(10)
                padding: dp(10)

                MDRaisedButton:
                    id: square2_1
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square2_1)

                MDRaisedButton:
                    id: square2_2
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square2_2)

                MDRaisedButton:
                    id: square2_3
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square2_3)

            MDBoxLayout:#row3
                orientation: "horizontal"
                size_hint: .7,.8
                pos_hint: {"center_x":.5, "center_y":.5}
                md_bg_color: "D35400"
                spacing: dp(10)
                padding: dp(10)

                MDRaisedButton:
                    id: square3_1
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square3_1)

                MDRaisedButton:
                    id: square3_2
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square3_2)

                MDRaisedButton:
                    id: square3_3
                    size_hint: 1,1
                    pos_hint: {"center_x":.5, "center_y":.5}
                    md_bg_color:"b9ff9c"
                    font_size: "65pt"
                    on_release: app.change_turn(square3_3)

## TEST

https://user-images.githubusercontent.com/111761417/227700083-030c1da2-066e-409e-9fe6-d74a9630f240.mov


