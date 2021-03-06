﻿/***********************************************************************************************************************
* 

* Copyright [2019] Renesas Electronics Corporation and/or its affiliates.  All Rights Reserved.


* This software is supplied by Renesas Electronics America Inc. and may only be used with products of Renesas Electronics Corp.


* and its affiliates (“Renesas”).  No other uses are authorized.  This software is protected under all applicable laws, including copyright laws.


* Renesas reserves the right to change or discontinue this software.


* THE SOFTWARE IS DELIVERED TO YOU “AS IS,” AND RENESAS MAKES NO REPRESENTATIONS OR WARRANTIES, AND TO THE FULLEST EXTENT PERMISSIBLE


* UNDER APPLICABLE LAW,DISCLAIMS ALL WARRANTIES, WHETHER EXPLICITLY OR IMPLICITLY, INCLUDING WARRANTIES OF MERCHANTABILITY, FITNESS FOR A


* PARTICULAR PURPOSE, AND NONINFRINGEMENT, WITH RESPECT TO THE SOFTWARE.  TO THE MAXIMUM EXTENT PERMITTED BY LAW, IN NO EVENT WILL RENESAS


* BE LIABLE TO YOU IN CONNECTION WITH THE SOFTWARE (OR ANY PERSON OR ENTITY CLAIMING RIGHTS DERIVED FROM YOU) FOR ANY LOSS, DAMAGES,


* OR CLAIMS WHATSOEVER, INCLUDING, WITHOUT LIMITATION, ANY DIRECT, CONSEQUENTIAL, SPECIAL, INDIRECT, PUNITIVE, OR INCIDENTAL DAMAGES;


* ANY LOST PROFITS, OTHER ECONOMIC DAMAGE, PROPERTY DAMAGE, OR PERSONAL INJURY; AND EVEN IF RENESAS HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH LOSS,


* DAMAGES, CLAIMS OR COSTS.


************************************************************************************************************************/




1. Project Overview:


	The example project demonstrates the typical use of the IIC slave HAL module APIs.

	The project initializes IIC slave and IIC master module 
with standard rate and is made interfaced with loopback mechanism.
	
On power up, after establishing SDA-SCL connection, user is requested to
 press the on-board push button to trigger the
	data transfer
 On push button pressing IIC transaction is performed and Once the transfer is 
completed, 

	received data is compared with the transmitted data.
Output is displayed on the RTT viewer and the on-board LED state indicates

	the success of data transfer.
	
	




LED output Status on slave TX and RX data mismatch(failure) and data match(success)
	

a) Failure  - Led is set as ON


	b) Success  - Led blinks for each transaction.





Note:


* For any event or API failure appropriate messages is displayed on RTT viewer.


* Slave write operation and read operation affirmative occurrence order can vary on extreme rapid "push button pressings" event





2. Hardware Settings:
 


	
	
Two jumper wires are required to establish loop back connection along IIC lines within the board with pins as mentioned below.



	

	RA6M3_EK
 /RA6M3G_EK
	
	--------
    

	Channel 0 has been used by IIC slave and channel 2 been used by IIC master.

    

	1) Slave IIC pins
        

	IIC0 P401  ----> SDA 
        

	IIC0 P408  ----> SCL 

    
	

	
	2) Master IIC pins
        
	
	IIC2 P511  ----> SDA 
     
   
	IIC2 P512  ----> SCL 
		


    

	RA6M2_EK
    
	
	--------
    
	
	Channel 0 has been used by IIC slave and channel 1 been used by IIC master.

    
	
	1) Slave IIC pins
        

	IIC0 P401  ----> SDA 
    
    
	IIC0 P400  ----> SCL 

    



	2) Master IIC pins
        

	IIC1 P206  ----> SDA 
     
   
	IIC1 P100  ----> SCL 

    



	RA6M1_EK
    

	--------
	Channel 0 has been used by IIC slave and channel 1 been used by IIC master.

    
	
	1) Slave IIC pins
        

	IIC0 P401  ----> SDA 
     
   
	IIC0 P400  ----> SCL 

    
	


	2) Master IIC pins
        

	IIC1 P101  ----> SDA 
     
   
	IIC1 P100  ----> SCL 

    



	RA4M1_EK
   

	--------
    

	Channel 0 has been used by IIC slave and channel 1 been used by IIC master.

  
  
	1) Slave IIC pins
       
 
	IIC0 P401  ----> SDA 
        

	IIC0 P400  ----> SCL 

    
	


	2) Master IIC pins
        

	IIC1 P206  ----> SDA 
      
  
	IIC1 P100  ----> SCL 

    



	RA2A1_EK
    

	--------
    
	
	Channel 0 has been used by IIC slave and channel 1 been used by IIC master.

 
  
	1) Slave IIC pins
        

	IIC0 P401  ----> SDA 
      
  
	IIC0 P000  ----> SCL 

    



	2) Master IIC pins
       
 
	IIC1 P400  ----> SDA 
      
 
	IIC1 P109  ----> SCL 
		
		





Note - For the functioning of IIC Slave on all the boards except for EK-RA6M3, external pull up resistors of value 3.9 or 4.7k ohms are required
 
       to be connected on I2C(SDA/SCL) lines.
  
