There is stm411re and FreeRTOS project. Firstly we create a new project and when we create .ioc file,
in the menu choose FREERTOS and then create 3 diferent Task in FreeRTOS menu, with diferent priorities.
Set the GPIO which will be use. I used PB0->for 'default task', which have priority 'Above the normal',
then PC1 -> for 'myTask02' which have priority 'Normal', and PC0 for 'myTask03' which priority is 
'Below Normal. Then I just write code(3 lines)to everyone task, that it toggle the different GPIO_pin 
and set differnt time of 'osDelay'(I use it, because it allows sheduler to run when other tasks are doing
when we are waiting) and we see in the video below, that diferent task are doing in the same time.

https://github.com/user-attachments/assets/f457d0fa-f7b7-4d48-96af-7c6f5cfe0ba2

Photos below show steps:
![freertos_photo_1](https://github.com/user-attachments/assets/1de6961e-cfb5-42fb-a792-8fed7ea64b30)
![freertos_photo_2](https://github.com/user-attachments/assets/7caa7bbf-23de-46f0-8535-76ae99947156)
When we want to save, programs gives us a warning, with steps what have to do.
![freertos_photo_3](https://github.com/user-attachments/assets/1326d71e-aee7-4470-b2ec-466040652193)
Then we select timer which are asking and enebling "USE_NEWLIB_REENTRANT".
![freertos_photo_4](https://github.com/user-attachments/assets/db49368f-c1b3-4e02-9934-5f2ddca5f8ae)
![freertos_photo_5](https://github.com/user-attachments/assets/8a714c95-1e66-4eb8-a041-398d51312078)
And dot forget GPIO:
![freertos_photo_6](https://github.com/user-attachments/assets/0582a61d-bada-4a57-aece-6b6b9cd8c6fe)
So, when we do everything, we see that all tasks 'LED' are blink at the same time. 
Thats all.
