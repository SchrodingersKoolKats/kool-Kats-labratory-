kool-Kats-labratory
===================

Client: Jacob Springs Farm (Section 2)
--------------------------

Jacob Springs Farm represents a minority of smaller farms local to Boulder that emphasize their farming systems on efficiency, sustainability, and being organic. Their main goal is to minimize costs to compete with large scale farms that have more funds and resources. The main products they farm include grass fed proteins such as duck, lamb, goose, chicken and eggs and fruits, herbs, and vegetables. There is a difference in the techniques that Jacob Springs Farm uses. They use rotational grazing and organic feed. Their whole process is based on being organic as possible removing unnecessary hormones, pesticides, and chemical fertilizer that larger farms use. 

![Alt Text](https://scontent-b-ord.xx.fbcdn.net/hphotos-ash2/v/t1.0-9/574624_628485870516300_1925504509_n.jpg?oh=d5a81c287057533a278c6cc7f0aa3327&oe=54C0582A)
Picture of Jacob Springs Farm

----------------------------

Problem: (Section 3)
-----------------------------

On any given day, there is a lot of activitiy and commotion on the farm ranging from beheading chickens to fixing fences to support the rotational grazing system. In the midst of all this activity, it is important to have good time management and a schedule that reduces friction and wasting time. There are many tasks for a farmer and this is the perspective we are using when handling any problems the farm presents. 

Andre Houssney is the specific farmer our group will be working with. He oversees the management and functionality of the farm. He presented a problem of time management and waste of water in his current system to fill his water tanks. In the current system, he has a timer that is connected to the water pump and once he turns the timer on it pumps water to the tanks which are 550 ft up a 17 ft hill. The problem with the current system is that he is unsure of how long to put the timer on for. Many factors such as weather and rain affect how long the timer should be turned on. Also, Andre has no efficient way to check the water level in the tanks besides walking up the hill himself to check on it. This creates problems as mentioned before concerning wasting time and this can take Andre away from more pressing issues on the farm. Not only that, Andre can end up wasting water once the tanks start to overflow. In our group's adventure out to the farm we witnessed this first hand while he was showing us the tanks. Another problem that Andre hopes to remedy soon is the placement of the tanks currently. There are three smaller tanks that have grown algae on the inside of them due to exposure of sunlight. As a result, Andre has built a new shed and has bought two new tanks. These will be placed within the shed and that is where we will be focusing our work. 

The system must fit in the water tank and needs to be self sufficient. The opening of the water tank isn't too wide, perhaps 12 inches, and our system needs to be able to maneuver that comfortably. The system must be able to monitor water levels within the two tanks (7ft and 5ft tall) and be capable of shutting off the pump from a distance of 550 ft to prevent overflow. The switch to turn the pumps off come from a 120V wall outlet which will also need to be accounted for. These are the specifications of this project.

![Alt Text](http://i.imgur.com/kl3MDRR.png)

Cad drawing of water tank

![Alt Text](http://i.imgur.com/wPhato3.jpg)
Layout of the farm

-------------------------------

Design Alternatives: (Section 4)
--------------------------------

Our preliminary brainstorm session came up with four ideas: float valve, pressure sensor, infrared sensor, and a conductivity sensor. However, we consider the infrared sensor the most viable option. 

The reason the float valve isn't a reasonable choice is due to the fact that this mechanism is largely mechanical and would work well if the switch were close to the tank. However, the switch is 550 ft down an incline back towards the house. Also, a float valve isn't very interesting. But we value the concept of a float valve and we will attempt to use the "float" concept. 

![Alt Text](http://www.freedrinkingwater.com/images-parts/tank-float-valve-setup-red-new.jpg)
Pressure Valve

The reason the pressure sensor was discarded is because the difficulty it brings. Although it is not too difficult to determine the depth of the water from the water pressure, we found that pressure sensors that can measure the change in pressure that we are looking at are rather expensive. Therefore, since we only need to know when the tank is full not how full the tank is we decided that using a pressure sensor was not worth the price as there are other low cost viable methods for solving this problem.

The reason the conductivity sensor was not a viable option was because how ineffective it truly worked in the water. We tested a sensor consisting of two wires but unfortunately they would have to be extremely close to each other in order to work. As a result, we decided to go with the infrared sensor. 

---------------------------------

Design Idea One: (Section 5)
------------------------------------------

The infrared sensor requires some more complicated technology. The general design idea is that we have the infrared sensor powered by an Arduino board in the tank connected to a pvc pipe apparatus. This apparatus would be cemented to the bottom of the tank and would have holes drilled into the side of the pipe. Inside the pipe a ping pong ball would be placed. As water would pump from the bottom and fill the tank as well as the tube, the ping pong ball would rise steadily up to the top of the apparatus. Once there, the ping pong ball would break the infrared sensor beam. This would cause the Arduino to send a signal via an Xbee Wireless Antenna to another Arduino board in the shed. This Arduino would have another Xbee Wireless Antenna ready to receive the signal and then it will use a solenoid with resistors to create a magnetic field that would effectively turn off the water pump. 

![Alt Text](https://cdn.sparkfun.com//assets/parts/1/8/3/00241-02.jpg)
Infrared Sensors

We understand that some setbacks include the water resistance of the sensors and the capabilities of this system to be self sufficient and to send a signal possibly through some barriers like the shed. However, we considered this too and figure that we can power this system with a solar cell that can be supported with a rechargeable battery. Also, we do not think that the signal will have problems reaching the receiver considering the 1 mile radius of the Xbee. Until we test more we will not have a definitive conclusion. 

--------------------------------------------------

Design Idea Two:
--------------------------------------

The second option we still considered is the use of a conductivity sensor. This would be more simple to install into the tank because we would not have to rely on an apparatus that has to cement into the bottom. This could hang from the top and all that would be required were two wires to descend towards the water. Once the water touched the wires, a current would be allowed to flow that would power the Arduino board for a system identical to the system used for infrared sensors. This could be a cheaper option and requires more testing to determine which design idea we will go with. 

An important thing to consider with this design idea is the amount of electricity that could be in the water. We do not want to shock someone who came into contact with this water. However, after doing more research, we found that it isn't a viable option because the wires have to be extremely close together in order for it to work. 

----------------------------------------------
Update of Construction Progress: (Section 5)
-----------------------------------------------
Currently we are focusing on the connection between the two radios. This is different from the primary design to use the XBee Wireless Antennas because we found a cheaper alternative. However, it is difficult to figure out the code and we are working on that so the system at the tank can communicate the Arduino board back at the shed. Most of the group has little experience with programming and code so this proves to be a slow process that will take most of the work time. 

Besides that, the rest of the group has developed the actual pipe system that will go into the tank. We found that using a mixture of clamps is the best option for attaching the pipe to the side of the tank so it does not move. Specifically we are using an Astoria clamp which is an old fashioned hose clamp. This is fastened around the pipe and it has one side that is threaded so a screw can be placed there. Attached to that threaded side using washers and bolts is another beam clamp that has been modified for our design. A hole big enough for the bolt has been drilled into one side and that is where it attaches to the Astoria clamp. On the other side we have another screw coming through. The plastic lip to the water tank will be placed inbetween the space created by the screw and bolt. This should securely fasten the pipe to the lip of the tank. Also, we have placed a cap on the bottom of the pipe so we can pour sand down into the pipe to weigh it down to prevent further movement of the pipe in the water. 

The other obstacle is to figure out how to make our system self sufficient via solar panels and rechargeable batteries. The group has not considered how to best manufacture these components. 

-----------------------------------------------

Update Number Two:
----------------------------------------
The group has now figured out the connection between the two Xbee Wireless Antenna's. The group decided to go back to this design after further failure with the radios. Ironically, both set ups eventually worked but the Xbee Antennas were finished first.

The solenoid and relay has been completed as well. The set up used was provided by Sparkfun. All that was needed was soldering and figuring out some simple coding. It is called the Beefcake Relay Control Kit. As a result of this, we completed a board that will allow Andre to fill the tank either half-way or completely. Additionally, a stop button was included so Andre could manually shut the water pump off if need be. The way this system completely works is that once the infrared sensors on the PVC pipe at the tank, which is already finished, it sends a signal from the Xbee transmitter at the tank to the receiver at the water pump. That signal will trigger the water pump to shut off via the Beefcake. 

The last thing required for this project is to make everything look professional and to finish the solar panel. The relay set up with the buttons will be mounted onto the wall and protected with acrylic. The pipe looks professional enough as it is, and the solar panel, which we have already bought, is contemporary. The exact battery needed is still being determined but other than that, it is a matter of simply hooking it up to the rest of the Arduino systems. This should be able to provide electricity for all the components of this project even with intervals of cloudy and snowy days. 

--------------------------------------------

Final Update:
-------------------------------------------
The project is now completely finished and has been presented at the Design Expo. The solar panel has not been completely tested but the group is confident it will work to recharge the batteries. Currently, there are four 1.2 V rechargeable batteries connected to the Arduino board at the shed and is powered by the solar panel. For further improvement we could upgrade the battery to a more expensive one that uses more voltage. However, the design we have currently works just as well. The PVC pipe system is finished now as well. There is a clamp on top that will allow it to latch on to the lip of the water tank and the bottom has been capped off. At the bottom we will place sand so it will weigh it down to prevent the tube from swaying in the water to improve accuracy. 
The Xbee and beefcake relay is all set up on a piece of acrylic that can be drilled into the wall. The three buttons are set up there as well so he can press a button corresponding to filling the tank halfway or completely full. The third button is for stopping the water pump in an emergency. 
At the tank, we have a Pelican case that is more expensive however we are absolutely confident it will protect the system from weather. It has holes drilled into it that are resealed with silicon that allow wires to go through it. A solar panel is hooked up to this which will go outside of the shed. This is our final product and it demonstrates almost complete functionality.  

Here is the final code we used for the Arduino and Xbee antennas to get them to communicate. 

Home Code: 
---------------

  #include <SoftwareSerial.h>
SoftwareSerial XBee(2, 3); // RX, TX

int button1; //low button
int button2; //high button
int pumpstatus; // 0 makes the relay turn the pump off
int stopbutton;
int goal;

const int button1pin = 13;
const int button2pin = 12;
const int relaypin = 8;
const int stopbuttonpin = 7;

//char fill_fully = 'F';
char fill_halfway = 'H';
char shut_off = 'S';

void setup()
{
  XBee.begin(9600);
  Serial.begin(9600);
  pinMode(button1pin, INPUT);
  pinMode(button2pin, INPUT);
  pinMode(relaypin, OUTPUT);
  pinMode(stopbuttonpin, INPUT);
}

void loop()
{
  button1 = digitalRead(button1pin);
  button2 = digitalRead(button2pin);
  stopbutton = digitalRead(stopbuttonpin);
    //for buttons, HIGH means the button is unpushed,
    // LOW means the button is pushed 
  if (stopbutton == LOW)
  {
    goal = 0; //stop
  }
  else if (button1 == LOW) 
  {
    goal = 1; //fill halfway
  }
  else if (button2 == LOW)
  {
    goal = 2; //fill fully
  }
  
  switch(goal)
  {
    case 0:
      digitalWrite(relaypin, LOW); //shut off the pump
      break;
    case 1:
      digitalWrite(relaypin, HIGH);
      XBee.write(fill_halfway);
      //delay(1000);
      break;
    case 2:
      digitalWrite(relaypin, HIGH);
      //delay(1000);
  }


    if (XBee.available()) 
    {
      char off = XBee.read();
      //if XBee is picking up a signal to turn off
      if (off == 83)
      {
        digitalWrite(relaypin, LOW);
        goal = 0;
      }
    }
  }
  -------------------
  Tank Code:
--------------------
  ---------------------
  #include <SoftwareSerial.h>
SoftwareSerial XBee(2, 3); // RX, TX

int lowsensor;
int highsensor;

const int lowsensorpin = 5;
const int highsensorpin = 6;

char fill_halfway = 'H';
char shut_off = 'S';

void setup()
{
  XBee.begin(9600);
  Serial.begin(9600);
  pinMode(lowsensorpin, INPUT);
  pinMode(highsensorpin, INPUT);
}

void loop(){
lowsensor = digitalRead(lowsensorpin);
highsensor = digitalRead(highsensorpin);
Serial.println(highsensor);
if (highsensor == 1) {
  XBee.write(shut_off);
}
  if (XBee.available()) {
      if (XBee.read() == fill_halfway) {
      //wait till low sensor reads a zero
         if (lowsensor == 1) {
         XBee.write(shut_off);
         }
      }
   }
}


Budget/Bill of Materials: (Section 9)
---------------------------------------------
| Object                                 | Price     |
|----------------------------------------|-----------|
| White LED                              | $1.71     |
| Silicone                               | $5.41     |
| Ping Pong Balls                        | $3.24     |
| PVC Pipe                               | $6.17     |
| Poster                                 | $32.00    |
| Miscellaneous Components from Tim      | $10.00    |
| McGuckin Hardware                      | $66.97    |
| Sparkfun Materials (Xbee and Arduinos) | $150.00   |
| Lamp                                   | $4.00     |
| Solder Board                           | $5.00     |
| Total                                  | $284.50   |
--------------------------------------------------------------

Future Modifications:
------------------------------------------
For the future, we are trying to develop a system that works with basically no error. This means that the sensors work consistently and the wireless communication is not faulty. This could include buying more expensive sensors or devices that can secure it better than simple electrical tape. Also, a better battery is under consideration. What we mean is we could find a battery of higher voltage that could last longer if no energy was given to it for an extended period of time. However, other than that, the only other improvements would be the aesthetics of the system making it prettier. It is not store shelf quality but it is definitely functionable and capable of marketing. We looked up similar systems that were sold professionally. One was called the Tunze Osmolator which is specialized for aquariums. The price was about $3100. Our group has managed to make a similar system that costs significantly less. This project definitely demonstrates efficiency and the critical design process. 

Timeline (Section 10)
--------------------------------------------------------
![Alt Text](http://i.imgur.com/hpnylpA.png?1) 
We have finished the system inside the tank.


Helpful Links and Resources: 
------------------------------------------

sparkfun.com

https://www.facebook.com/JacobSpringsFarm/timeline?ref=page_internal

Tim May 

Andre the farmer

Professor Soltys (Thank you by the way. Great semester)

Jace and Spencer, the TAs (Awesome dudes!)



