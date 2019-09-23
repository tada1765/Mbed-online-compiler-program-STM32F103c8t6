# Mbed-online-compiler-program-STM32F103c8t6
Objective:
----------------
- To program STM32F103c8t6 MCU with Mbed online compiler.

Software & Hardware:
-----------------------------
- Software :
 - ST-LINK Utility, [download here](https://www.st.com/en/development-tools/stsw-link004.html)
 - google chrome or any internet browser that able to reach Mbed website, [website here](https://www.mbed.com/en/).

- Hardware :
 - STM32F103c8t6 blue-pill or black pill, [references](https://shopee.com.my/product/119159849/1952461096)
 -  Or stm32f103 smart v2.0, [references](https://shopee.com.my/STM32F103C8T6-ARM-STM32-Minimum-System-Development-Board-STM32-Core-Board-i.119159849.1948146478)
 - Or NUCLEO-F103RB, [references](https://www.st.com/en/evaluation-tools/nucleo-f103rb.html)

Circuit Diagram on my circuit:
---------------------------------
This circuit diagram is using two STM32F103C8T6 MCU, STM32 Blue-Pill as ST-link,  STM32 Black-Pill as target. For more detail can refer to my "STM32F103c8t6 as ST linker with LED Blinky program" project.

OR you can use NUCLEO-F103RB so you can skip the wiring on this circuit connection.

- Two stm32f103c8t6 MCU Connection:
![ST-Link and target](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/3f563d7f5efcb2f3bb6b5f674d108215/image.png)

ignore the blue bracket mark(for STM8) construct the red bracket mark(for stm32) circuit.
*NOTE: connect 3.3V together for both MCU (target and ST-link), do not use 5V.

 - The snip shot on my circuit connection:
![MY](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/7d17e0517a6c6b626fd93480f10e4bac/image.png)

Procedure:
------------
This procedure is step by step to program a STM32 Blue-Pill or STM32 Black-Pill MCU by using Mbed online compiler. 

1. Open Mbed website, [website here](https://www.mbed.com/en/) and register an account.
![mbed](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/ff0ff5a714c52d8041d1a010a421a027/image.png)

2. login and click the work "compiler"show in the red mark bracket diagram below:
![login](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/a1680e1ca5d3f61eacda8e1487126c94/image.png)

3. now you are in the Mbed compiler interface click the red mark bracket to select platform.
![platform](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/c268408e12a0ffb355fddf719347d5d9/image.png)

4. Then click "add Board".
![addBoard](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/0d15b388dce2586d56f4df8abbfcee75/image.png)

5. Tick the box for Cortex-M3 then select NUCLEO-F103RB.
![NUCLEO](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/16228398ec9d039a8f5491ae8beb1b26/image.png)

6. Make sure you select the right platform at the top right corner is show "NUCLEO-F103RB".
![NUCLEO2](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/01f4afaf1de7c3c179a70379994df7b2/image.png)

7. Now go to this website here, [website here](https://os.mbed.com/users/hudakz/code/STM32F103C8T6_USBSerial/) from  hudakz then click the red mark bracket "import to compiler".
![hudakz ](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/2d83b04c37e7255c7329b0f516fb3a96/image.png)

8. At your Mbed compiler interface double click "main.ccp" and make sure in the program have import "stm32f103c8t6.h" and mbed.h".
![main](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/0938468707764e3486e3b8dedbb6df86/image.png)

9. Then connect your board to PC through USB cable then click "compile". after that a bin file will start downloading.
![compile](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/460cbf34c758c4b576a7b4b12e36e302/image.png)
  
10. Open " ST-LINK Utility" software and click the red mark bracket connect to the target. 
![stlink](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/64b09c6b689bd9fd32db540060a12d8a/image.png)

11. under "target" select "Program".
![program](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/562d9020c8f54c1ad122de14dc4c0313/image.png)

12. Click "Browse" and select the downloaded bin file then click Start.
![bin](https://trello-attachments.s3.amazonaws.com/5cee4774d8fcdd32c2d51358/5d87175e696aed11f95e01e1/51c20f576ca286251f03c5263c67ea33/image.png)

13. Now observe the response on your MCU, a LED will start blinking. the program already flash into the MCU memory, so you can disconnect the software and power off the MCU then power up again, You will see the LED blink again.   

Summery:
-----------
- This example able to function a simple LED Blinky program when using Mbed online compiler for a STM32F103c8t6 micro controller.
- Some file is necessary to have in the Mbed program for example "mbed-STM32F103C8T6.lib" to program STM32F103c8t6 without any error. 
- They are still many function needed to be try and test in the future to ensure the board able to work with Mbed online compiler completely.  

References:
--------------
1. from hudakz, [link: https://os.mbed.com/users/hudakz/code/STM32F103C8T6_USBSerial/]
2. Mbed website, [link: https://www.mbed.com/en/]


