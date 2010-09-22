The zip file contains x-loader and u-boot compiled with ITBOK test suits, copy MLO from x-load, u-boot.bin from u-boot on boot partition of SD card, (MLO first). You can boot any kernel uImage with this, just copy the uIage file along with MLO and u-boot.bin. 
Available tests
==============
currently, only touch screen test is running properly, at boot press any key to stop autoboot process and do the following:
 # diag ts test
Place the stylus on lcd panel and press ENTER
Type 'q' to abort the test
[x y] = [ 0x71 0x2c]
[x y] = [ 0x16 0x2c]
[x y] = [ 0xce 0x106]
[x y] = [ 0x75 0x10d]
[x y] = [ 0x14 0x10d]
[x y] = [ 0x77 0x9d]
Touchscreen Test Aboterd by user...


to see other tests, do:
#itbok

1. Run All Tests (Options 2 to 18)
 2. Run Memory Test
 3. Run NAND Test
 4. Run Audio Headset detection Test
 5. Run Audio Test
 6. Run Keypad Test
 7. Run Touchscreen Test
 8. Run LCD Backlight Test
 9. Run LCD Test
10. Run Battery Test
11. Run TV-out Test
12. Run S-Video
13. Run RTC Test
14. Run Ethernet Test
15. Run MMC Test
16. Run Camera Test
17. Run OTG Host Test
18. Run OTG Gadget Test
19. Run UART Test
20. EXIT

Unfortunately these tests dont run successfully yet.

For LCD, try this:
# diag lcd fillclr red (not working for me)
