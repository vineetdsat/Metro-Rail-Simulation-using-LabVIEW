# Metro-Rail-Simulation-using-LabVIEW
This simulation represents the Bengaluru green line metro; an LED  Representing the Train which moves from one station to another while announcing the current station and the upcoming station, and then back-traces its path to return to the initial station.
# Screenshots
![](Screenshots/Screenshot%20(27).png)

![](Screenshots/Screenshot%20(28).png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![](Screenshots/Screenshot%20(46).png)

![](Screenshots/Screenshot%20(47).png)

![](Screenshots/Screenshot%20(49).png)

# Description 

● During the final week of our internship, we were assigned a project. The project assigned
to us by our instructor, Mr. Sagar, was the Stimulation of the Bangalore Metro Train
System.

● Using LabVIEW, we created the front panel and block diagram for the same topic.

● FRONT PANEL:
  ○ The front panel shows the actual simulation.
  
  ○ We used a blinking LED to represent the train moving from station to station.
  
  ○ The “train track” includes the Green Line stations of the Bangalore Metro, which
    are: Yelachenahalli, Jaya Prakash Nagar, Banashankari, Rashtreeya Vidyalaya
    Road, Jayanagar, National College, Nadaprabhu Kempegowda Station (Majestic),
    Yeshwantpur, Peenya, and finally Nagasandra.
    
  ○ The “train” starts at Yelachenahalli and makes its way from station to station
    through the entire Green Line.
    
  ○ When it reaches the end, i.e. Nagasandra, the train comes back in the reverse
    order all the way back to Yelachenahalli.
    
  ○ At each station, there is an announcement which states the station that the train is
    at currently and also the name of the station which comes next.
    
    
● BLOCK DIAGRAM:
  ○ We used State Machine Architecture for this project.
  
  ○ As mentioned before, this Architecture uses the following functions mainly:
    ■ While Loop
    ■ Case Structure
    ■ Shift Register
    ■ Transition Code
    
  ○ As we can see from the Block Diagram (Fig. 8) below, we make the train move
    forward by incrementing the left coordinate of the LED by 1. This continuously
    changes the LED’s x-coordinate and so it moves horizontally. If we were to
    change the y-coordinate, the LED would move up and down (or vertically).
    
  ○ A case structure is also used, which continuously compares the coordinates of the
    train with the upcoming station. If the coordinates match up, the train stops there
    since it recognizes that it is a station. The announcement is made, and then the
    train moves forward to the next station.
    
  ○ For the announcement, we used a SpeechSynthesizer function which knows to be
    used whenever the train and station are matched up.
    
  ○ From Fig. 9, we can see the list of cases for the train to travel to Nagasandra from
    Yelachenahalli, and then return to each station before finally reaching its
    destination of Yelachenahalli again.
    
  ○ Finally, we have a case structure for the stopping of the train when it reaches
    Yelachenahalli station again. It initializes the position of the train and stops it after
    one to and fro motion through the track.
