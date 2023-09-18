# TFT
TFT codes to copy in STM32cubeide
STM32_HAL_ILI9341
ILI9341 Library for STM32 HAL

Tutorial https://blog.naver.com/eziya76/221579262995

References

https://github.com/martnak/STM32-ILI9341
https://os.mbed.com/users/dreschpe/code/SPI_TFT_ILI9341/
https://www.mikroe.com/glcd-font-creator
Most of codes are originated from martnak's library.
https://github.com/martnak/STM32-ILI9341

I wanted to make it support diverse fonts so I adopted character functions from SPI_TFT_ILI9341 library.
As it supports C font array created by GLCD Font Creator by MikroElektronika.
https://www.mikroe.com/glcd-font-creator

Please refer to the following link to get more details about fonts.
https://os.mbed.com/users/dreschpe/code/SPI_TFT_ILI9341/

[Modification]

Modified DrawText & DrawChar functions to make them support diverse bitmap fonts.
Rearrange SPI functions
Removed TIM1 related test.
[ How to add new fonts ]

Run GLCD Font Creator
Click File-New Font-Import An Existing System Font
Select font, style and size from font dialog.
GLCD Font Cretor makes Bitmap fonts
Click Export for GLCD menu
Select mikroC tab.
Copy generated code to fonts.c file
Modify data type from unsigned short to uint8_t
Add optional bytes (offset, width, height, bpl) to the array !!! IMPORTANT !!!
Add extern declaration to fonts.h file
![pinout](https://github.com/robot78p/TFT/assets/106536316/5d4f4ecd-bff2-4630-82c5-743411736008)

