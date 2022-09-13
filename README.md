# 40K_Servo

Here I will describe how to run my code to monitor the diode 
temperature and current for the 40K servo. I will desribe the code from top to bottom.

First first cell imports the relevant packages. 
%matplotlib inline is a magic function that allows us to animate the plots.

The PrologixInterface class provides useful methods to establish a connection between your computer 
and the prologix controller, so that the prologix controller can talk to the Lakshore330.

The next cell presents three useful functions for tracking the diode current and temperature. 
The function find_heater_range returns whether the heater is on low, med, or high setting. Then the next function find_heater_percentage 
returns the percentage of the maximum current that the heater is at for the given heater setting. We use both pieces of information to
compute the heater current (which is computed by the function find_max_current). The function get_data simply returns the temperature.

The functions create_file, create_csv, and write_csv allow us to log the current and temperature data in a csv file.

To run the temperature logger, your simply need to run all the cells in order.
