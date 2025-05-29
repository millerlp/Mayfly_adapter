# Mayfly_adapter
A circuit board for interfacing 8 analog sensors with an EnviroDIY Mayfly v1.1 data logger. 
This can be used to monitor multiple simple analog voltage inputs. Using the software library
linked below, the user can cycle through 8 inputs of an analog multiplexer (TMUX1208PWR, Texas Instruments) and send the chosen
voltage signal to the analog-to-digital convertor of the Mayfly data logger. The board also has
an 8-channel port expander (PCA9557PWR) that can be used to toggle the SLEEP pin of an attached analog
sensor like the Allegro A1395 Hall effect sensor that this board is designed for. 


As of 2025, the RevB hardware files are functional and in use. These can be used to 
produce a printed circuit board that can be populated with the parts listed in the
file Mayfly_adapter_v1p1_revB_parts.xlsx. 

While the circuit board contains circuits for reading 8 multiplexed analog inputs and
8 multiplexed I2C lines, only the analog input lines are implemented in the associated
library found at [https://github.com/millerlp/Allegro_A139x_8channel_mux](https://github.com/millerlp/Allegro_A139x_8channel_mux). 

Note that this 8-Channel library also relies on a modified library for the PCA9557 library 
found here: [https://github.com/millerlp/pca9557](https://github.com/millerlp/pca9557)

![Image of a Mayfly adapter circuit board attached to an EnviroDIY Mayfly v1.1 data logger](/Pictures/_MG_1317-2.jpg)


On the bottom of the Mayfly data logger board, some of the solder jumpers should be 
modified: 

On solder jumper 19 (SJ19), move the solder blob from 12 to 13. 
On solder jumper 16 (SJ16), place a blob of solder (activates modem power LED - white)
On solder jumper 17 (SJ17), place a blob of solder (activates modem network indicator LED - blue)

![Image of the bottom of a Mayfly data logger with solder jumpers circled](/Pictures/Mayfly_jumper_modifications_20230206.JPG)


Developed by Luke Miller
