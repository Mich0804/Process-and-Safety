# Future improvements

 ## **Introduction:**
   For the assignment of "Process and Safety" a solution of the assembly process has been researched and implemented. This chapter gives an outline of future improvements and safety measurements. 
   
## **Future improvements:**
1.  **Change material of jig:**
    Currently the jigs are fully 3D-printed. For the initial setup of the assembly process, this was a good way to test the working principle of the process. Due to friction and a not yet optimal working process the current materials might wear out over time. To ensure better operation in a production process, the chosen materials could be exchanged for more durable materials e.g. metal components. 

2.  **Testing:**
    Due to unforeseen circumstances, limited testing has been executed to the setup. The current setup is therefore one of the first versions of the working principle of the assembly process. For future projects, more testing needs to be executed in an earlier stage to ensure more optimal review of the setup. This way, malfunctions of different components can be changed earlier in the process and optimalisation of the process is maintaned throughout the project. 

3. **Shielding setup and housing (exposed) wires:**
   Currently the setup is open and accesible for everyone and wires are exposed. This needs to be taken care of and will be explained further in the implementation of safety measurements below.

4. **Incorporate vision systems:**
    The setup of the assembly project is based on a fixed position for the different components. This might lead to suboptimal assembly since the robot will simply continue the process even though an individual component might not be in the right location. This can be solved through sensors and/or a vision system. 
    
    If a vision system is added to the assembly, a computer algorithm can be taught when the robot can continue with the assembly process. For an optimal working process of a vision system, multiple components need to be in tune with each other. These vision components are lenses, camera, lighting and filters. Besides these components the setup needs to be calibrated and aligned to accurately account for any discrepancies. Besides the setup of the vision system, also the software needs to be in line with the process. Object recognition and tracking needs to be taught to extract the data of the different components. All of these vision components can be expensive and can take up some time to test and implement. The decision to implement a vision system can be made through a cost-benefit-analysis.

   

## **Safety measurements:**
   Since the setup is currently still being tested, not all safety measurements have been incorporated. These safety measurements are crucial to ensure safe operation of the process and safe conditions for the uses/operator/visitiors. 

   - **Exposed wires:** Currently multiple wires are still open and reachable for users/operaters/visitors to touch. This can lead to unsafe operation, malfunction and hazardous situations for everyone involved. These wires are both electrical and pneumatic wires. For safe operation these wires need to be housed so that the operator cannot come in direct contact, but in such a way that checking and maintenace can still be performed. 
  
   - **Shielding of setup:** Currently the setup is open and accesible for everyone to touch all the components and even the robot. The effects of this open setup can be hazardous, therefore the setup needs to be shielded. The best way to do so is create a see-through setup around the robot and the assembly jigs, with an open area for the operator to add in new components. This open area can be made more safe through light curtains or zone scanning. 

   - **Light curtains:** In the risk analysis there is an increase in the risk index when the robot can come in contact with the operator and executes harm to the operator. For safer operation light curtains can be installed on the locations where the operator needs to perform actions e.g. solve malfunction of component placement.
  
   - **Maintenance operation:** In the risk analysis there is an increase risk index when deterioration has taken place to individual or multiple components. To decrease this risk a maintenace operation needs to be implemented in the software. This maintenance operation can for example give a warming when the maximum operation time has been exeeded. This will increase the chance of (scheduled) maintenance to be performed on time and that the maintenance is executed following the correct guidelines. 
  
   - **Operator training:** Besides these maintenace operation, the operator also needs to be made aware of the possible risks of deteriorated parts and the importance of (scheduled) maintenance. This awareness can be ensured with proper explaination and training for the operators with working with robots and the (PLC) programming. 


   
