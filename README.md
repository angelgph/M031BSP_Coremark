# M031BSP_Coremark
 M031BSP_Coremark

Download coremark source code from GitHub as below , 

https://www.eembc.org/coremark/download.php

Porting step : 

- 1. Create folder named "CoreMark" in project , and put below file into folder : 

core_list_join.c , core_main.c , core_matrix.c , core_state.c  , core_util.c , coremark.h 

- 2. Put below file in project : core_portme.c , core_portme.h 

- 3. check comment between //porting Nuvoton start , //porting Nuvoton end in core_portme.c and core_portme.h

- 4. exclude main.c in project , and follow step #3 modification in core_portme.c and core_portme.h

-------------------------------------------------------------
in KEIL setting , 

- Options for Target > C/C++ , add define MAIN_HAS_NOARGC

- Options for Target > C/C++ , select Optimization > Level 3(-O3) , checked Optimization

- Options for Target > C/C++ > Include Paths  , add directories \Coremark , and \Template


in IAR setting , 

- General Options > Library Options 1 > Prinfer formattter , select Auto

- C/C++ Compiler > Preprocessor > Optimizations > Level , select High and Speed , checked No size constraints

- C/C++ Compiler > Preprocessor > add define MAIN_HAS_NOARGC

- C/C++ Compiler > Preprocessor > add directories \Coremark , and \Template

-------------------------------------------------------------
Below is test result / score in NuMaker-M032SE , 


![image](https://github.com/released/M031BSP_Coremark/blob/main/result.jpg)




