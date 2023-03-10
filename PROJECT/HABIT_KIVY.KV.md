# KIVY FILE FOR THE HABIT TRACKER APPLICATION

```.py

#habit_kivi.kv

ScreenManager:
    LoginScreen:
        name: "LoginScreen"

    RegistrationScreen:
        name: "RegistrationScreen"

    MainScreen:
        name: "MainScreen"

    HistoryScreen:
        name: "HistoryScreen"


<LoginScreen>:
    FitImage:
        source:"background.jpeg"
    MDCard:
        size_hint: .6,.8
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"


        MDLabel:
            size_hint: 1,.2
            font_style: "H3"
            font_size: "40pt"
            text: "WELCOME TO HABIT TRACKER!"
            halign: "center"
            color: 183/255, 110/255, 121/255, 1

        MDLabel:
            size_hint: 1,.02

        MDTextField:
            id: email
            mode: "fill"
            hint_text: "enter email"
            size_hint: .6, .06
            pos_hint: {"center_x":.5}

        MDLabel:
            size_hint: 1,.02

        MDTextField:
            id: passwd
            mode: "fill"
            hint_text: "enter password"
            password: True
            size_hint:.6, .06
            pos_hint: {"center_x":.5}

        MDLabel:
            size_hint: 1,.04

        MDBoxLayout:
            size_hint: 1,.2
            orientation: "vertical"

            MDRaisedButton:
                id: login
                text: "login"
                md_bg_color: 183/255, 110/255, 121/255, 1
                on_press: root.try_login()
                size_hint: .53,.05
                pos_hint: {"center_x":.5}

            MDLabel:
                size_hint: 1,.01

            MDRaisedButton:
                text: "register"
                md_bg_color: 183/255, 110/255, 121/255, 1
                on_press: root.parent.current = "RegistrationScreen"
                size_hint: .53,.05
                pos_hint: {"center_x":.5}

            MDLabel:
                size_hint: 1,.06

<RegistrationScreen>:
    FitImage:
        source:"background.jpeg"
    MDCard:
        size_hint: .6,.8
        pos_hint: {"center_x":.5, "center_y":.5}
        orientation: "vertical"

        MDLabel:
            size_hint: 1,.1
            font_style: "H3"
            text: "REGISTER"
            halign: "center"
            color: 183/255, 110/255, 121/255, 1

        MDTextField:
            id: uname
            hint_text: "enter username"
            mode: "fill"
            size_hint: .8, .07
            pos_hint: {"center_x":.5}

        MDLabel:
            size_hint: 1,.03

        MDTextField:
            id: email
            hint_text: "enter email"
            mode: "fill"
            size_hint: .8, .07
            pos_hint: {"center_x":.5}

        MDLabel:
            size_hint: 1,.03

        MDTextField:
            id: passwd
            hint_text: "enter password"
            mode: "fill"
            password: True
            size_hint: .8, .07
            pos_hint: {"center_x":.5}

        MDLabel:
            size_hint: 1,.03

        MDTextField:
            id: passwd_check
            hint_text: "re-enter password"
            mode: "fill"
            password: True
            size_hint: .8, .07
            pos_hint: {"center_x":.5}

        MDLabel:
            size_hint: 1,.03

        MDBoxLayout:
            size_hint: 1,.2
            orientation: "vertical"

            MDRaisedButton:
                id: login_back
                text: "Back"
                md_bg_color: 183/255, 110/255, 121/255, 1
                on_press: root.parent.current = "LoginScreen"
                size_hint: .53,.05
                pos_hint: {"center_x":.5}

            MDLabel:
                size_hint: 1,.01

            MDRaisedButton:
                text: "Register"
                md_bg_color: 183/255, 110/255, 121/255, 1
                on_press: root.try_register()
                size_hint: .53,.05
                pos_hint: {"center_x":.5}

            MDLabel:
                size_hint: 1,.02


<MainScreen>:

    MDBoxLayout:
        orientation: "horizontal"
        pos_hint: {"center_x":.5, "center_y":0.95}
        size_hint: 1,0.1
        MDLabel:
            id:profile_label
            size_hint:.03,1
            md_bg_color: 183/255, 110/255, 121/255, 1

        MDLabel:
            id: welcome_label
            size_hint: .95, 1
            font_style: "H3"
            text: "WELCOME BACK!"
            font_size: "25pt"
            color: "white"
            md_bg_color: 183/255, 110/255, 121/255, 1

    MDBoxLayout:
        orientation: "horizontal"
        pos_hint: {"center_x":.5, "center_y":.85}
        size_hint: 1,0.1

        MDLabel:
            id:space_label
            size_hint:.03,1
            md_bg_color: 231/255, 206/255, 210/255, 1

        MDLabel:
            id: welcome2_label
            size_hint: .95, 1
            font_style: "H3"
            text: "CHECK YOUR HABITS FOR THE DAY AND LOOK AT YOUR PROGRESS!"
            font_size: "19pt"
            md_bg_color: 231/255, 206/255, 210/255, 1

    MDBoxLayout:
        orientation: "horizontal"
        pos_hint: {"center_x":.5, "center_y":.4}
        size_hint: 1,0.8
        md_bg_color: 231/255, 206/255, 210/255, 1

        MDBoxLayout:
            id: checkboxes
            orientation: "vertical"
            size_hint:.35,1

            MDGridLayout:
                id: switches
                cols: 2
                rows: 5
                md_bg_color: 248/255, 240/255, 241/255, 1

                MDLabel:
                    id: habit1
                    text: "Study Math"
                    font_size: "13pt"
                    halign: 'center'
                    valign: 'center'
                    md_bg_color: 242/255, 227/255, 229/255, 1
                    size_hint: .5,.5


                MDCheckbox:
                    on_active: root.checkbox_click(self.active,1)
                    inactive_color: "grey"
                    color_active: "pink"
                    widget_style: "ios"
                    pos: .5,.5
                    md_bg_color: 242/255, 227/255, 229/255, 1

                MDLabel:
                    id: habit2
                    text: "Go to gym"
                    font_size: "13pt"
                    halign: 'center'
                    valign: 'center'
                    md_bg_color: 234/255, 213/255, 210/255, 1

                MDCheckbox:
                    on_active: root.checkbox_click(self.active,2)
                    inactive_color: "grey"
                    color_active: "pink"
                    widget_style: "ios"
                    pos: .5,.5
                    md_bg_color: 234/255, 213/255, 210/255, 1
                MDLabel:
                    id: habit3
                    text: "Study CS"
                    font_size: "13pt"
                    halign: 'center'
                    valign: 'center'
                    md_bg_color: 242/255, 227/255, 229/255, 1
                MDCheckbox:
                    on_active: root.checkbox_click(self.active,3)
                    inactive_color: "grey"
                    color_active: "pink"
                    widget_style: "ios"
                    pos: .5,.5
                    md_bg_color: 242/255, 227/255, 229/255, 1
                MDLabel:
                    id: habit4
                    text: "Sleep 8 hours"
                    font_size: "13pt"
                    halign: 'center'
                    valign: 'center'
                    md_bg_color: 234/255, 213/255, 210/255, 1
                MDCheckbox:
                    on_active: root.checkbox_click(self.active,4)
                    inactive_color: "grey"
                    color_active: "pink"
                    widget_style: "ios"
                    pos: .5,.5
                    md_bg_color: 234/255, 213/255, 210/255, 1
                MDLabel:
                    id: habit5
                    text: "Make bed"
                    font_size: "13pt"
                    halign: 'center'
                    valign: 'center'
                    md_bg_color: 242/255, 227/255, 229/255, 1
                MDCheckbox:
                    on_active: root.checkbox_click(self.active,5)
                    inactive_color: "grey"
                    color_active: "pink"
                    widget_style: "ios"
                    pos: .5,.5
                    md_bg_color: 242/255, 227/255, 229/255, 1

        MDBoxLayout:
            orientation: "vertical"
            size_hint:.45,1
            md_bg_color: 246/255, 238/255, 237/255, 1

            MDLabel:
                size_hint: 1,.3
                id: Progress_label
                text: "Progress-O-Meter"
                font_size: "26pt"
                halign: 'center'
                valign: 'center'

            MDRaisedButton:
                id:progress_date
                text: "select date"
                text_pos_hint: {"center_x":1}
                md_bg_color: "white"
                text_color: "grey"
                size_hint: .8, .05
                pos_hint: {"center_x":.5}
                on_press: root.date()

            MDBoxLayout:
                orientation: "vertical"
                MDLabel:
                    size_hint: 1, .4
                MDProgressBar:
                    id: progressbar
                    value:0
                    min: 0
                    max: 100
                    pos_hint: {"x": .1}
                    size_hint_x: .8
                    color: 'green'
                MDLabel:
                    id: percent_label
                    size_hint: 1, .8
                    text: "0%"
                    font_size:"22pt"
                    halign: 'center'
                    valign: 'center'
                MDLabel:
                    id:error_text
                    size_hint:1,.2
                    text:""
                    font_size:10
                    halign: 'center'
                MDRaisedButton:
                    id: save_button
                    text: "Save"
                    on_press: root.save()
                    md_bg_color: 185/255, 107/255, 114/255, 1
                    size_hint: 1,.3
                    font_size:"20pt"
                    pos_hint: {"center_x":.5}

        MDBoxLayout:
            id: main_buttons
            orientation: "vertical"
            md_bg_color: 231/255, 206/255, 210/255, 1
            size_hint:.2,1

            MDRaisedButton:
                id: stats_screen
                text: "History"
                md_bg_color: 183/255, 110/255, 121/255, 1
                on_press: root.parent.current = "HistoryScreen"
                size_hint: .53,.05
                pos_hint: {"center_x":.5}
                font_size: "14pt"

            MDLabel:
                size_hint: 1,.01


            MDRaisedButton:
                id: close_screen
                text: "Log out"
                md_bg_color: 183/255, 110/255, 121/255, 1
                size_hint: .53,.05
                pos_hint: {"center_x":.5}
                font_size: "14pt"
                on_press: root.back_login

            MDLabel:
                size_hint: 1,.01

<HistoryScreen>
    MDBoxLayout:
        orientation: "horizontal"
        pos_hint: {"center_x":.5, "center_y":0.95}
        size_hint: 1,0.1

        MDLabel:
            id:space2_label
            size_hint:.03,1
            md_bg_color: 183/255, 110/255, 121/255, 1

        MDLabel:
            id: history_label
            size_hint: .95, 1
            font_style: "H3"
            text: "HISTORY"
            font_size: "25pt"
            color: "white"
            md_bg_color: 183/255, 110/255, 121/255, 1

    MDBoxLayout:
        orientation: "horizontal"
        pos_hint: {"center_x":.5, "center_y":.85}
        size_hint: 1,0.1

        MDLabel:
            id:space_label
            size_hint:.03,1
            md_bg_color: 231/255, 206/255, 210/255, 1

        MDLabel:
            id: welcome2_label
            size_hint: .95, 1
            font_style: "H3"
            text: "CHECK YOUR PROGRESS HISTORY"
            font_size: "19pt"
            md_bg_color: 231/255, 206/255, 210/255, 1

    MDRaisedButton
        id: delete
        text: "DELETE"
        on_press:root.delete()
        md_bg_color: 183/255, 110/255, 121/255, 1
        pos_hint: {"center_x":.4,"center_y":.2}

    MDRaisedButton
        id: back
        text: "BACK"
        on_press:root.parent.current = "MainScreen"
        md_bg_color: 183/255, 110/255, 121/255, 1
        pos_hint: {"center_x":.6,"center_y":.2}
```
