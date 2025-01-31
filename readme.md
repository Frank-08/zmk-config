# No Arrows Keyboard

## Change what a key does

1. Open zmk-config/boards/shields/no_arrows/no_arrows.keymap
2. Kayout matches the physical layout
3. Keycodes can be found here: https://zmk.dev/docs/keymaps/list-of-keycodes
4. Commit and Push to repo
5. Firmware wiil be created through github action
6. Once compiled, downlaod firmware.uf2 file
7. Power on Keyboard with boot button pressed
8. Copy firmware.ue2 file to the drive that was mounted
9. keybaord will unmount and boot into new firmware

## STL Generator for case

### Generator is a python script stolen from [jeffminton on github](https://github.com/jeffminton/keyboard_stl_generator)

1. Run `pip install -r requirements.txt`
2. Update parameters.json in zmk-config/case-files/keyboard_stl_generator if neded
3. Run `Python keyboard_stl_generator.py -i zmk-config/dad-no-arrows.json -a -p parameters.json`
4. Files are in zmk-config/dad-no-arrows
