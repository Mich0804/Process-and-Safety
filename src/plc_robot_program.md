# PLC + Robot program

#### PLC program

    CASE step OF
	0: // init
		timer(IN := TRUE, PT:=T#2000MS);
		IF timer.Q THEN
			timer(IN := FALSE);
			GVL.O1_start_robot_programma := FALSE;
			GVL.Output_2 := FALSE;
			GVL.O3_motoren_aan := FALSE;
			GVL.Output_4 := FALSE;
			step := 1;
		END_IF
		
	1: 	// check of opslag is vol
		timer(IN := TRUE, PT:=T#10000MS);
		IF GVL.I1_sensor_1_opslag = TRUE AND GVL.I2_sensor_2_opslag = TRUE AND GVL.I3_sensor_3_opslag = TRUE THEN
			opslag_vol := TRUE;
			timer(IN := FALSE);
			step := 2;
		ELSIF timer.Q THEN
			timer(IN := FALSE);
			step := 99;
		END_IF
	2: //start robot programma
		GVL.O1_start_robot_programma := TRUE;
		IF GVL.I5_programma_bezig_robot = TRUE THEN
			step := 3;
		END_IF
	3:
		WHILE GVL.I5_programma_bezig_robot = TRUE DO
			IF GVL.I6_programma_klaar_robot = TRUE THEN
				step := 0;
			ELSIF GVL.I7_error = TRUE THEN
				step := 99;
			END_IF
		END_WHILE	
    END_CASE

#### GVL

    VAR_GLOBAL
        I1_sensor_1_opslag AT %I* : BOOL;
	    I2_sensor_2_opslag AT %I* : BOOL;
	    I3_sensor_3_opslag AT %I* : BOOL;
	    I4_sensor_4_robot AT %I* : BOOL;
	    I5_programma_bezig_robot AT %I* : BOOL;
	    I6_programma_klaar_robot AT %I* : BOOL;
	    I7_error AT %I* : BOOL;
	    Input_8 AT %I* : BOOL;
    
	    O1_start_robot_programma AT %Q* : BOOL;
	    Output_2 AT %Q* : BOOL;
	    O3_motoren_aan AT %Q* : BOOL;
	    Output_4 AT %Q* : BOOL;
    END_VAR

#### Robot program
The robot program is still to be made. This will be done before the assesment.