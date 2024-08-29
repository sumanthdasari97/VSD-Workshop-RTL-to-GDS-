

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
# magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def 
![Screenshot from 2024-08-27 05-49-16](https://github.com/user-attachments/assets/7d4afeb5-e999-469f-a893-0c3c55b01a73)
![Screenshot from 2024-08-27 05-50-44](https://github.com/user-attachments/assets/fbfbe795-2eca-4be2-bce5-acefe9062c5f)
![Screenshot from 2024-08-27 05-53-14](https://github.com/user-attachments/assets/881f77c3-eb83-4101-ab49-3c9858e64ac7)

**PLACEMENT**
run_placement 
![Screenshot from 2024-08-24 00-19-35](https://github.com/user-attachments/assets/98732cb2-af45-467a-80ec-879e32861db2)

magic view of floor plan
# magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def
![Screenshot from 2024-08-27 05-35-16](https://github.com/user-attachments/assets/63f66d2e-daa0-437d-bc98-b75cff6f5e7a)

Changing the io placer from 1 to 2
![Screenshot from 2024-08-27 06-14-53](https://github.com/user-attachments/assets/e81b44c2-163c-4b70-a5b5-512c6b60f09a)


**DAY 3**
# LIBRARY CELL DESIGN 
![Screenshot from 2024-08-27 06-21-50](https://github.com/user-attachments/assets/25262f2d-507f-467f-bf89-b427d63fc8d3)

# Layout of INVERTER

![Screenshot from 2024-08-27 06-21-41](https://github.com/user-attachments/assets/04aed524-0222-4e70-876e-4c8b3e226b62)

![Screenshot from 2024-08-27 06-24-51](https://github.com/user-attachments/assets/3e60a4c5-ba1f-4b42-ac35-1f9b8561541d)

# Connectivity of nmos
![Screenshot from 2024-08-27 06-27-04](https://github.com/user-attachments/assets/4ba7eb23-37e0-403f-a56d-b3db212ea8d2)

# Extracting the Spice Netlist
 extract all
 ext2spice
![Screenshot from 2024-08-27 06-29-15](https://github.com/user-attachments/assets/31eab7a3-4697-4113-af7f-a922c261888c)
![Screenshot from 2024-08-27 06-30-39](https://github.com/user-attachments/assets/23f5f0fe-7b94-431a-9192-c9869e44b2cb)

# modified spice file 
![Screenshot from 2024-08-27 06-32-31](https://github.com/user-attachments/assets/2e1d4555-3c21-419a-ae1f-41d7b235738e)

# Spice simulation resutls 
![Screenshot from 2024-08-27 06-35-45](https://github.com/user-attachments/assets/27d5a8a0-d398-4aa2-bf8b-21bf08351264)

# Plot 
![Screenshot from 2024-08-27 06-37-38](https://github.com/user-attachments/assets/1abe9ff3-339d-4a4a-b0c6-e69dabafcef3)


Maximum value is 3.3 
20% of max value is 0.66 xo is 2.1819e
80% of max value is 2.64 


DRC TESTS
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
tar xfz drc_tests.tgz
cd drc_tests
gvim .magicrc
magic -d XR &
![Screenshot from 2024-08-27 06-53-28](https://github.com/user-attachments/assets/73572879-2772-49cf-b670-340d979d4ff4)

met3.mag
![Screenshot from 2024-08-27 06-58-18](https://github.com/user-attachments/assets/16292945-e332-43ca-a348-4de6f78a0c88)

Loading Poly.mag
![Screenshot from 2024-08-27 07-08-06](https://github.com/user-attachments/assets/ad6bb249-eda6-4659-bc37-5b6e43f0015e)

editing the poly.9 
![Screenshot from 2024-08-27 07-27-03](https://github.com/user-attachments/assets/2fa7719e-374c-4fd7-b1c9-b11cc909f459)
![Screenshot from 2024-08-27 07-30-18](https://github.com/user-attachments/assets/68fdff19-554f-4bdb-9a92-98c76ff57344)

# nwell.mag
![Screenshot from 2024-08-28 05-10-26](https://github.com/user-attachments/assets/3d541c52-099d-4a1f-8735-5418af02cf0a)

updated tech file 
![Screenshot from 2![Screenshot from 2024-08-28 05-24-07](https://github.com/user-attachments/assets/e6e72d88-c2ed-4500-a766-b62853d7ea43)
024-08-28 05-19-58](https://github.com/user-attachments/assets/b23035c3-cc29-4312-a94a-e14e1ee06862)
![Screenshot from 2024-08-28 05-51-31](https://github.com/user-attachments/assets/2452c08a-d75b-4007-90f7-b7eab96672b1)
![Screenshot from 2024-08-28 05-38-51](https://github.com/user-attachments/assets/b57ce36e-2bd5-4561-9ca0-7614ecd36462)

**DAY4**
# LEF EXTRACTION
TRACKS INFO 
![Screenshot from 2024-08-28 06-02-50](https://github.com/user-attachments/assets/2362d347-e46e-4b59-b693-eafc060362c3)
Grids as per tracks info
![Screenshot from 2024-08-28 06-07-58](https://github.com/user-attachments/assets/66048686-c87d-4585-9d20-df47e8c0127b)

writing LEF 
![Screenshot from 2024-08-28 06-24-05](https://github.com/user-attachments/assets/c812239f-cd93-4fa8-b716-0829a9c1ceae)

VSD _INV LEF FILE
![Screenshot from 2024-08-28 06-25-16](https://github.com/user-attachments/assets/f953f901-d695-4a12-81a8-ae32e20e58d6)



![Screenshot from 2024-08-29 05-32-07](https://github.com/user-attachments/assets/7a9fbaff-d60f-454f-9671-d325f3f8f6d2)

Custom Inv Cell Added 
![Screenshot from 2024-08-29 05-35-15](https://github.com/user-attachments/assets/1e3b183a-83d9-47f9-9ccd-18d3882b41bb)
timing report
![Screenshot from 2024-08-29 05-36-32](https://github.com/user-attachments/assets/8515b9e8-fb9d-455a-823d-eb377b3d8661)

cHANGING THE CONFIGURATIONS IN ORDER TO REDUCE THE NEGATIVE SLACK MORE IN TO TIMING ORIENTED 
![Screenshot from 2024-08-29 05-47-56](https://github.com/user-attachments/assets/831cca7b-9f03-4d45-8af4-4ff1998d91db)

After running synthesis 
![Screenshot from 2024-08-29 05-56-31](https://github.com/user-attachments/assets/92f7d100-285b-4111-9e9b-080a0d4074a8)

Improved timing 
![Screenshot from 2024-08-29 05-57-35](https://github.com/user-attachments/assets/8909c0c7-9976-432c-96ff-a73f4d600031)

Custom cell included in the placement stage 
![Screenshot from 2024-08-29 06-34-22](https://github.com/user-attachments/assets/c42ee3ba-e8a6-45d3-b390-df029438e4e5)

![Screenshot from 2024-08-29 06-43-05](https://github.com/user-attachments/assets/2540cada-99a6-4eef-9e4c-6bb2857c328d)

![Screenshot from 2024-08-29 06-33-11](https://github.com/user-attachments/assets/7b9c5d11-74d5-4290-ab23-48e733c261d2)

Using Expand command 
![Screenshot from 2024-08-29 06-39-36](https://github.com/user-attachments/assets/fec31e51-84a0-478e-951b-103b30bffa03)

Pre_sta.conf
![Screenshot from 2024-08-29 06-52-13](https://github.com/user-attachments/assets/1c0cd647-d7d7-4559-92eb-1f6bd617c206)

my_base.sdc
![Screenshot from 2024-08-29 07-03-10](https://github.com/user-attachments/assets/d78fb704-1749-42db-9df9-1f754580b60b)

sta pre_sta.conf
![Screenshot from 2024-08-29 07-07-22](https://github.com/user-attachments/assets/1c664374-53f2-45c1-9410-1170fdb20195)

Fanout limited to 4 
![Screenshot from 2024-08-29 07-16-34](https://github.com/user-attachments/assets/efbe6a9f-a081-4ceb-9908-b5aab1929879)

Slack met 
![Screenshot from 2024-08-29 07-18-30](https://github.com/user-attachments/assets/f3e5ffc0-0f04-4eb5-9727-411f330a2961)

run_cts 
![Screenshot from 2024-08-29 07-29-18](https://github.com/user-attachments/assets/f956369e-ceff-4214-be87-bbc5a9df81ee)

Post CTS Anlaysis
![Screenshot from 2024-08-29 22-12-55](https://github.com/user-attachments/assets/eb8d1337-0558-4986-bdad-3c7966f85cc1)

Timing Met 
![Screenshot from 2024-08-29 22-16-29](https://github.com/user-attachments/assets/ab57713f-45da-40e4-8c0e-1cb297110d83)

**DAY 5**
PDN GENERATION
![Screenshot from 2024-08-29 23-44-14](https://github.com/user-attachments/assets/d7798e38-9826-4a16-99fe-aaf5cc43b0c1)

Power Distribution Network in Magic
![Screenshot from 2024-08-29 23-57-21](https://github.com/user-attachments/assets/66e3206e-ae0c-465e-893a-f5d220c91779)

![Screenshot from 2024-08-29 23-57-37](https://github.com/user-attachments/assets/939e908f-c1b3-4b47-ad6c-b5b9e271d055)

Now run_routing 

![Screenshot from 2024-08-30 00-01-43](https://github.com/user-attachments/assets/3230ebbd-2bed-48b1-a827-68d4997ef423)
![Screenshot from 2024-08-29 23-59-24](https://github.com/user-attachments/assets/504f1b34-82fe-4254-a121-6575df3df9ed)

![Screenshot from 2024-08-30 00-04-17](https://github.com/user-attachments/assets/2b71cdd6-fdee-450a-a6dd-a07fc9fc9e53)
![Screenshot from 2024-08-30 00-03-53](https://github.com/user-attachments/assets/7e7d780b-d3df-46f7-8390-4c0c52fb7870)

SPEF FILE

![Screenshot from 2024-08-30 00-14-51](https://github.com/user-attachments/assets/bae3f1fe-29a8-4a08-92fd-638f291f29f5)


Final  DEF 
![Screenshot from 2024-08-30 00-08-09](https://github.com/user-attachments/assets/de3fa258-91e3-4871-870e-d57d383f0f88)





















 





















 



