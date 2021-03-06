/***********************************************************************************************************************
* Copyright [2019] Renesas Electronics Corporation and/or its affiliates.  All Rights Reserved.
*
* This software is supplied by Renesas Electronics America Inc. and may only be used with products of Renesas Electronics Corp.
* and its affiliates (“Renesas”).  No other uses are authorized.  This software is protected under all applicable laws, 
* including copyright laws.
* Renesas reserves the right to change or discontinue this software.
* THE SOFTWARE IS DELIVERED TO YOU “AS IS,” AND RENESAS MAKES NO REPRESENTATIONS OR WARRANTIES, AND TO THE FULLEST EXTENT 
* PERMISSIBLE UNDER APPLICABLE LAW,DISCLAIMS ALL WARRANTIES, WHETHER EXPLICITLY OR IMPLICITLY, INCLUDING WARRANTIES OF 
* MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT, WITH RESPECT TO THE SOFTWARE.  TO THE MAXIMUM 
* EXTENT PERMITTED BY LAW, IN NO EVENT WILL RENESAS BE LIABLE TO YOU IN CONNECTION WITH THE SOFTWARE (OR ANY PERSON 
* OR ENTITY CLAIMING RIGHTS DERIVED FROM YOU) FOR ANY LOSS, DAMAGES, OR CLAIMS WHATSOEVER, INCLUDING, WITHOUT LIMITATION, 
* ANY DIRECT, CONSEQUENTIAL, SPECIAL, INDIRECT, PUNITIVE, OR INCIDENTAL DAMAGES;
* ANY LOST PROFITS, OTHER ECONOMIC DAMAGE, PROPERTY DAMAGE, OR PERSONAL INJURY; AND EVEN IF RENESAS HAS BEEN ADVISED OF 
* THE POSSIBILITY OF SUCH LOSS,DAMAGES, CLAIMS OR COSTS.
* **********************************************************************************************************************/



1. Project Overview:

     
     The example project demonstrates the typical use of the ELC HAL module APIs.


     IOPORT, GPT0 and GPT1 events are linked using ELC. The start source for GPT0 and GPT1 is IOPORT event and
     the stop source for GPT1 is GPT0 counter overflow. GPT1 runs in PWM mode and GPT0 runs in one-shot mode.
     On pressing the user push button, an IOPORT event is triggered which starts blinking the LED.
     LED stops blinking after 5 sec when GPT0 expires.




2. Hardware settings for the project:


        Hardware connections:
        Pin Connection for EK-RA6M3 and EK-RA6M3G:
        Connect P009 to P101.

NOTE:
1. Use Switch S1 (push button) on RA6M3 and RA6M3G.
2. On EK_RA2A1 board, LED glows for 5 seconds. Because PWM timer used is 16-bit and maximum delay is generated in microseconds,
   LED blinking cannot be recognised.