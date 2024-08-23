# VSD-Workshop-RTL-to-GDS
#Open lane Directory and pdk Directory 
![Screenshot from 2024-08-22 23-13-16](https://github.com/user-attachments/assets/06e32aab-7a97-4e47-8c03-bca809d30513)
![Screenshot from 2024-08-22 23-17-02](https://github.com/user-attachments/assets/c5cebadb-a709-43c0-b6bf-9cc7ddc57d59)

![Screenshot from 2024-08-22 23-22-10](https://github.com/user-attachments/assets/6ed474a1-c265-44b5-ae87-3c75fb08e85c)
![Screenshot from 2024-08-22 23-42-05](https://github.com/user-attachments/assets/477cff83-9f55-4dd7-93e3-1020e2e1c55c)

Preparation has been done using prep design 
![Screenshot from 2024-08-22 23-44-53](https://github.com/user-attachments/assets/6019d655-934f-46ca-8131-dcbf5ece7237)
Synthesis
Command run_synthesis
![Screenshot from 2024-08-22 23-53-35](https://github.com/user-attachments/assets/5dbcf253-e898-49ea-9383-006b4a806fc0)
#synthesis Results 

![Screenshot from 2024-08-23 00-02-39](https://github.com/user-attachments/assets/c5016512-e1d9-41f2-be60-9fa4a1463f4c)
![Screenshot from 2024-08-23 00-02-49](https://github.com/user-attachments/assets/07175763-2960-4336-a06d-53e11161b7e0)

THE FLOP RATIO = Number of FLops/ Total Cells 
 = 1613/14876 =0.108428969 = 10.84%

# sta report after synthesis
![Screenshot from 2024-08-23 00-17-46](https://github.com/user-attachments/assets/15913833-4b1f-43d2-902b-a5b9df66b659)


 **DAY 2**  **FLOOR PLAN**

 Floor Plan .tcl 
 ![Screenshot from 2024-08-23 00-26-27](https://github.com/user-attachments/assets/5558a557-3745-4740-be53-02b0d5bb091c)
 init_floor plan
 ![Screenshot from 2024-08-23 00-54-17](https://github.com/user-attachments/assets/a80cdee3-7e91-4151-b8b5-cf6a028bf1a6)
place_io
![Screenshot from 2024-08-23 00-54-50](https://github.com/user-attachments/assets/c39435a7-2726-466f-865c-4ffdd64c452c)
Decap Cells Inserted 
tap_decap 
![Screenshot from 2024-08-23 00-56-52](https://github.com/user-attachments/assets/aa900841-b3a0-4081-8355-5f2aecf6cf0b)

Floorplan.def File Created in the Results
![Screenshot from 2024-08-23 01-03-59](https://github.com/user-attachments/assets/c9a06ea7-8940-4cec-b9e1-684ec5564123)
# DEF FILE 
it Has the Die Area 
![Screenshot from 2024-08-23 01-05-19](https://github.com/user-attachments/assets/2f87f7fa-0d23-41b0-8fcc-8ce7128db3c8)

We can calculate the area using the def file  the unit is 1000 microns
DIEAREA ( 0 0 ) ( 660685 671405 )   This is from the def file and the values are the boundaries of the die 
Area of the die can be calculated  as 6600685 /1000  * 671405/1000 = 4431732.912425 microns^2

# Magic 
Reading the LEF and DEF FIles using command 
# magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def 
![Screenshot from 2024-08-23 23-37-38](https://github.com/user-attachments/assets/9fbea1a0-f9fc-408e-960e-1e1ea8f7a4a4)

![Screenshot from 2024-08-23 23-46-17](https://github.com/user-attachments/assets/d75e62e7-f06a-49c4-9a96-98f62852f1fb)
![Screenshot from 2024-08-23 23-45-55](https://github.com/user-attachments/assets/04980f08-4467-46cd-a8bf-f127802b5235)
![Screenshot from 2024-08-23 23-45-49](https://github.com/user-attachments/assets/0758dc39-8ed5-4fb1-9e02-15d369e6f462)







 



