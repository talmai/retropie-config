Files needed to update a RetroPie allowing it to be connected to 2 wii-motes (w/classic adapter). YMMV and you will definitely need to update to the specific ID of your bluetooth controllers. 

# Install wminput (and deps)

```
> sudo apt-get install vim bluetooth vorbis-tools python-cwiid wminput
```

# Copy the following files

```
/etc/udev/rules.d/wiimote.rules
/etc/cwiid/wminput/wii_controller1
/etc/cwiid/wminput/wii_controller2
/opt/retropie/configs/all/retroarch-joypads/NintendoWiimote.cfg
/etc/rc.local
```

Note that rc.local is where you would need to update your IDs

# Restart udev

```
sudo service udev restart
```

# Check bluetooth status

```
/etc/init.d/bluetooth status
```

# Update retroarch.cfg

Finally update /opt/retropie/emulators/retroarch/retroarch.cfg with...

```
# PLAYER 1
input_player1_joypad_index = "0"
input_player1_a_btn = "0"
input_player1_b_btn = "1"
input_player1_x_btn = "2"
input_player1_y_btn = "3"
input_player1_l_btn = "4"
input_player1_r_btn = "5"
input_player1_l2_btn = "6"
input_player1_r2_btn = "7"
input_player1_select_btn = "8"
input_player1_start_btn = "9"
input_player1_up_axis = "+1"
input_player1_down_axis = "-1"
input_player1_left_axis = "-0"
input_player1_right_axis = "+0"
input_player1_l_x_plus_axis = "+2"
input_player1_l_x_minus_axis = "-2"
input_player1_l_y_plus_axis = "-3"
input_player1_l_y_minus_axis = "+3"
input_player1_r_x_plus_axis = "+4"
input_player1_r_x_minus_axis = "-4"
input_player1_r_y_plus_axis = "-5"
input_player1_r_y_minus_axis = "+5"
# PLAYER 2
input_player2_joypad_index = "1"
input_player2_a_btn = "0"
input_player2_b_btn = "1"
input_player2_x_btn = "2"
input_player2_y_btn = "3"
input_player2_l_btn = "4"
input_player2_r_btn = "5"
input_player2_l2_btn = "6"
input_player2_r2_btn = "7"
input_player2_select_btn = "8"
input_player2_start_btn = "9"
input_player2_up_axis = "+1"
input_player2_down_axis = "-1"
input_player2_left_axis = "-0"
input_player2_right_axis = "+0"
input_player2_l_x_plus_axis = "+2"
input_player2_l_x_minus_axis = "-2"
input_player2_l_y_plus_axis = "-3"
input_player2_l_y_minus_axis = "+3"
input_player2_r_x_plus_axis = "+4"
input_player2_r_x_minus_axis = "-4"
input_player2_r_y_plus_axis = "-5"
input_player2_r_y_minus_axis = "+5"
```
