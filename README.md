Demo code and assignments for RAS-598 Space Robotics and AI will be posted here. 

Course website: https://deepgis.org/dreamslab/ses598/

#Assignment 1:

    ##Final Paramaters:


        Kp_linear = 8.05     This value gave smooth movement through the entire range
       
        Kd_linear = 0.015    This lower value resulted in much smoother movement
       
        Kp_angular = 6.75     Kp_angular affected the width of turns the most and this value
                              resulted in tight turns while remaining smooth
       
        Kd_angular = 0.025    This value gave the most smooth and even cornering
       
        self.spacing = 1.0    This value allowed for the most area to be covered with
                              little to no overlap


    ##Performance Metrics and Analysis:


    ![Results of sim showing the average and max cross-track error](/images/turtle_results.png)




    ![Path of sim](/images/turtle_path.png)


        As seen in the above images the max cross-track error was 0.324 and the average
        cross-track error was 0.163, along with the consistency of the path the pd
        tuning is shown to be fairly good.


    ![Graph of sim results](/images//turtle_graph.png)


        Though when looking at the graph in the above image the linear velocity does fluctuate
        fair amount. While the path and cross-track error results are very good the pd controller
        could use more tuning to further even out the linear velocity.


    ##Discussion of Tuning Methodology:


        My tuning method was to start by tuning Kd_angular lower and lower values to achive smooth
        cornering. Once I though it was cornering fairly smooth I then adjusted Kp_angular to
        adjust the width of the turns to be relativley tight while still remaining consistent
        through the turn, I would also make minor adjustments to Kd_angular. Once Kd_angular and
        Kp_angular where properly tuned I then began to tune Kd_linear and Kp_linear using the same Methodology I used for Kd_angular and Kp_angular. After these wehre tuned I moved on to adjust the spacing, I first lowered the apscing down to 0.25 and observed the reults. This resulted in mcuh overlap in the path, I then increased the spacing by increments of
        0.1 untill it achived the desired reults.


    ##Challenges and Solutions
