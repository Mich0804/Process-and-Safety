# Design choices

Here we will go over our design and explain why we made certain decisions. For a more detailed description of the system with pictures please look at the design overview first. \
\
The system consists of multiple parts that are all mounted on top of a wooden plate. I will divide the system into multiple sub systems. \
•	The motor box\
o	The motor holders\
o	The motors\
o	The motor attachments for holding the parts \
\
The motor box is an acrylic/3dprinted box that contains the motor holders, the motors and attachment pieces for holding the parts. The box itself consists of a 3d printed bottom plate which has engraved circles for positioning the motor holders. It has 4 acryllic plates, 1 at the top, 1 for each side and 1 for the back. The front of the box is open so the motors can be wired. \ 
\
The motor holders are 3d printed. These holders are glued to the bottom plate of the box. Each motor holder has 2 openings at the sides for wiring of the motors. They keep the motors in place using friction, so that when something goes wrong the motors just pop out of the holders instead of the system breaking. \
\
The motors are 24V DC motors which have a low RPM. We chose for low RPM motors so we could have a controlled testing environment where breakage of the system is very unlikely. The motors are powered by a 24V power supply and are controlled with the PLC which was delivered by Saxion. \
\
Attached to the shaft of each motor is an attachment piece which holds the parts. This attachment is 3d printed using TPU plastic which is flexible. The reason for this is that the attachment acts like a spring so that when pressure is applied, the part gets pushed against the main body of the valve without the risk of breaking the attachment or motor. The attachment pieces are also designed to make up for any offset- or angular misalignments. 
The attachment pieces are attached to the motor shaft with an air tight seal. This is possible because of the flexible plastic. I printed this with an infill percentage of 70%, with this the attachment is strong enough and also just flexible enough to be able to push it onto the motor shaft. Because of this the seal is air tight. \
\
•	The storage bridge \
o	The storage tubes \
o	3 inductive sensors. \
The storage bridge is also made from acryllic. It consist of 2 side plates and a top plate. Attached to the top of the storage bridge are 3 storage tubes which hold 3 different parts. The tubes are attached to the bridge using super glue. There are 3 inductive sensors which check if all the parts are in storage. \
\
•	The air cylinder \
o	The pusher on the air cylinder \
o	Attachment pieces \
o	Throttle valve \
The air cylinder is a single-acting cylinder from Rexroth. It pushes the motor box underneath the storage bridge to load the parts onto the motor attachments. It is attached to one of the motor holders with a 3d printed pusher using nuts and bolts. The reason we are pushing the box instead of the bridge is because the bridge has a very high center of gravity which would cause that it would easily fall over if pushed.  The air cylinder is attached to a wooden base using 3d printed attachment pieces and screws. \ 
The air cylinder has a threaded shaft. First the pusher was attached with a 3d printed thread this was later changed to a 3d printed pusher with a metal nut inside of it because the 3d printed thread could brake easily because of the force of the air cylinder. \
\
•	The robot \
o	The grippers \
As a group we came up with the idea to use a gripper which is mounted on the head of the robot to pick up the little parts, but more important also pick up the valve itself without all the parts which have to be screwed on. The idea was to clamp the valve inside the gripper with designed brackets which slides on the provided gripper and fit tight around the valve, so when the gripper is closed it is fixated. The original idea was to put all the caps which have to be screwed on in a bracket where the robot moves toward and after that the head of the robot should be rotated and moved down a little bit, so the valve will screw itself on the cap, instead of the other way around. But after testing this principle, this didn’t work out, so the idea was altered a little bit. The caps are now still put on a bracket, but this bracket is mounted on top of a motor. The caps will now be rotated instead of the valve. The robot arm picks up the valve and rotates it to the desired angle and position of the first bracket. After that it pushed down a little bit, and the motor starts spinning. When the cap is screwed on around two turns the valve (and cap) will be lifted out the bracket and will be moved and rotated to the next position and continuous the steps again until everything is mounted on the valve. \
\
There are three items which have to be grabbed by the gripper, a small metal part, a larger metal part, and the body of the valve. They all differ in sizes, because the diameter is different. This was a problem, as the gripper works on air, it has two positions, just open or closed, nothing in between. The best solution is to use a gripper which can also be opened and closed on other desired positions, but for now this was not possible. So therefore a second set of gripper adapters have to be used to grab the two loose metal parts. This requires a tool change. If another type of gripper could be used, this tool change wouldn’t be needed. For example a linear actuator one (which works with a motor). The decision to design an adaptor which slides over the existing 3D printed gripper arms is made because of three different reasons. First, this way is costs less filament to actually print the parts, but this is just a small reason. The second one is that a tool change will be faster, you just slide off and on the new adapters. The third reason is that the M3 screws that are on the gripper actuator still have to be accessible, otherwise the gripper arms cannot be removed.  With more testing time another gripper could have be designed, but the design and gripper were only known for a short time before. \
\
•	Wooden plate \
Al of the parts are attached to a wooden plate using either screws or glue. \
\
•   Storage plates \
The small brass ring and cylinder is stored on a storage plate. This has fingers on it with chamfered edges to centre the parts on them. \
The fingers for the ring are a couple of centimers up so that the robot can easily pick them up. The cylinder is tall enough so for that part this wasnt necesarry. \
