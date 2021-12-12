# Group1_microp

Milestone #1

Groups Member

1. Muhaimin bin Mohd Hashim (MKE211014)
2. Muhammad Salehuddin bin Bakarudin (MKE211021)
3. Ooi Tze Kian (MKE191085 )

How to setup Blinky on Nucleo-F466RE board.
1.	Open any Integrated Development Environment (IDE)/compiler that is available. For this task, we are using STM32CubeIDE compiler.
2.	Connect the Nucleo board to your computer.
3.	From the compiler interface, select File > New > STM32 Project to start a new project. A new interface will pop-out. From here, we select our board by searching Nucleo-F466RE board.
4.	Set the name of the project to Blinky and finish. 
5.	After that, at the left side, you will see a list of files associated with the board configuration. 
6.	The only things we care about is main.c file. To open this file, on the left side, double click Src > main.c.
7.	In this main.c file, we need to edit the while(1) function.
8.	Before editing this main.c file, we need to check the pin configuration for LED so that to make sure, we are assigning a correct pin.
9.	To do so, we need to download/see the board configuration either download or open .ioc file which is located at the left side of the interface.
10.	After confirming our LED pin configuration, in this case our Nucleo-F466RE board is GPIOA PIN 5, we go back to main.c file and edit it.
11.	Go to while(1) function and add this line:

    HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5);
    HAL_Delay (1000);

12.	After adding those two lines, go to the Project > Build Project to compile the code. 
13.	Go to Run > Debug As > STM32 MCU C/C++ Application.
14.	An interface will pop-out, just leave it as default and click OK.
15.	Confirmation windows will pop-out be asked to change perspective. Click switch to open a new windows perspective, where a new toolbar at the top can be seen.
16.	At the toolbar, you can see a play button. Click the play button to start running your Blinky application on your Nucleo board.
17.	You can see your GREEN LED labelled LD2 turn on and off. To change the timing of the on and off the the LD2, you can edit the HAL_DELAY(TIME) according to your preference.
