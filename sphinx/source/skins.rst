.. _skins:

=====
Skins
=====

Ren'Py supports skinning the launcher – changing what the launcher
looks like. To do this, follow the following steps:

Skins are specific to the Ren'Py version in use, and can't be
expected to be forward or backwards compatible.

1. Open the launcher in the launcher. This can be done from the
   preferences screen.

2. Create the skin.rpy script file.

3. Copy the following into skin.rpy::

    init -2 python:
        # The color of non-interactive text.
        custom_text = "#545454"

        # Colors for buttons in various states.
        custom_idle = "#42637b"
        custom_hover = "#d86b45"
        custom_disable = "#808080"

        # Colors for reversed text buttons (selected list entries).
        custom_reverse_idle = "#78a5c5"
        reverse_hover = "#d86b45"
        custom_reverse_text = "#ffffff"

        # Colors for the scrollbar thumb.
        custom_scrollbar_idle = "#dfdfdf"
        custom_scrollbar_hover = "#d86b45"
        # An image used as a separator pattern.
        custom_pattern = "images/pattern.png"

        # A displayable used for the background of everything.
        custom_background = "images/background.png"

        # A displayable used for the background of the projects list.
        custom_projects_window = Null()

        # A displayable used the background of information boxes.
        custom_info_window = "#f9f9f9c0"

        # Colors for the titles of information boxes.
        custom_error_color = "#d15353"
        custom_info_color = "#545454"
        custom_interaction_color = "#d19753"
        custom_question_color = "#d19753"

        # The color of input text.
        custom_input_color = "#d86b45"

        # A displayable used for the background of windows
        # containing commands, preferences, and navigation info.
        custom_window = Frame(Fixed(Solid(custom_reverse_idle, xsize=4, xalign=0), Solid(custom_info_window, xsize=794, xalign=1.0), xsize=800, ysize=600), 0, 0, tile=True)

4. Modify skin.rpy to skin the launcher. Place the image files you use
   into the launcher's game directory. Recommended size for background
   800x600 pixels.

5. Select Custom theme in preferences.

An incorrect skin.rpy file could prevent the launcher from
starting. To fix it, you'll need to remove skin.rpy and skin.rpyc from the launcher's game directory, start the launcher, and then put them back.
