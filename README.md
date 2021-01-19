

Preh cell monitor linux-based command line utility

requires MYBMM for the modules

only supports CAN bus

this CMU came with my BMW battery packs.  Together with the smart contactors you can monitor and control the battery packs.  The contactors have shunts for measuring current.  they have CAN bus output for voltage, contactor status, etc.  good stuff!

this util just dumps what CMUs have what cells


For CAN:

sitool -t can:<device>[,speed]

example:

	sitool -t can:can0,500000


for CANServer/Can-over-ip

sitool -t can_ip:<ip addr>,[port],<interface>,[speed]

example:

	sitool -t can_ip:10.0.0.1,3930,can0,500000


To start the Sunny Island remotey:

sitool -t can:<device>[,speed] -s

example:

	sitool -t can:can0,500000 -s


To stop the Sunny Island remotey:

sitool -t can:<device>[,speed] -S

example:

	sitool -t can:can0,500000 -S
