# 207-final-project-Beer-Dispenser
Repository for CS 207 Project
A beer dispenser was build as a final class project for CS 207. The purpose of building a beer dispenser was to make something both useful, fun, and something original. While moving a liquid from one container to another container is not that difficult, the final product has interesting and useful features that make pouring a glass of beer an informative and fun process. The most important of these features being automation. 
	The general goal of this project was to, with the press of one button, pour a perfect beer every time. This is done by using a submersible bilge pump that pumps the beer out of a growler and into a glass. A laser is shining through the glass and onto a photo-resistor so that when the desired amount of beer is poured the laser beam will refract in the liquid as it is more dense than air and break the connection made with the photo-resistor and stop the pump. Additional features that were included are: a temperature sensor that senses the temperature of the beer growler and lets the user know the temperature in degrees Celsius, a flow sensor that can tell how much beer in flowing into the glass so in the future more precise amounts of beer could be dispensed, and a solenoid valve that stops the flow of liquid abruptly as to not allow the glass to overflow. The project was mounted to a cardboard box as it was the most simple solution, but a a small refrigerator would be an ideal solution, but expensive. 
	In the original proposal, the build used compressed air to pressurize the growler but this was not ideal as it was dangerous as I wanted to use the most common container for pub quality beer at home, a glass beer growler. Having no experience with pneumatics or gas regulation, it was decided that a pump would be a better solution. This solution using a pump was also less expensive, more reliable and sustainable than the pressurized growler idea.

Inspirations

The idea for the project came about when a good friend of mine invited me to his house to see his new beer fridge. He told me I should buy one, so I decided to make one in an attempt to show him up. Looking online I found an instructibles article for a similar project that used compress CO2 to dispense beer manually, not automatically. This sample project also included a payment system that I did not was to implement given what it was going to be used for. This was the main sourced used as it had useful information on parts and specifically using relays to control solenoid valves. While a useful starting point, I opted for a more automated and sustainable build that I would actually want to use long term. This way my goal of pouring the perfect beer every time  was achievable as it takes the human error out of the equation. 

Required Materials. 
1 Arduino uno
1 Breadboard
1 Bilge Pump
1 Solenoid valve
1 photo resistor 
2 leds one green one red
2 push buttons
1 5v relay
PVC tubing to be cut to desired length
many Wires and Generic resistors
1 Temperature sensor
1 Laser Pointer

Building Process

The building process began one a doable design was decided upon. The First idea was to use only a solenoid valve and have gravity feed the liquid into the glass when the valve was open. This was not a good solution as it required the growler to be mounted above the enclosure upside down taking away from the generality of the build. A pump allowed liquid to be poured from any container placed anywhere nearby. The first and greatest challenge was getting the relays to work. It was difficult to find an easy explanation of how to wire a relay like the one that came with out kit, but after some research and experimentation it function as desired and was a useful learning exercise[3]. After this was figured out the next challenge was soldering all the components that needed leads to connect to the Ardunio or longer leads so they could be mounted (pump, solenoid valve, photo-resistor, temperature sensor). This was difficult as I had not soldered before and only had access to and archaic solder gun. It made soldering the small leads of the temperature sensor for example difficult and took a few tries. The next challenge was fitting all the connection on the breadboard as there are many and the breadboard got very cramped. The buttons needed to be accessible on the breadboard so some though went into the placement of every component. Then it was time to gather all the tubing and cut it to size and attached it securely to all the parts that the liquid flows though (pump, solenoid valve, flow sensor). Having chosen a pump with an end that a piece of generic tubing from a beer/wine making kit fit over perfectly made this process easy. Then came then final step of the build which was mounting all the parts onto the cardboard enclosure (laser pointer, photo-resistor, spout where the beer flows out of). For power sources, everything except the solenoid valve is powered off the Ardunio, the solenoid valve required a higher voltage so it was powered off a battery pack. 
The code is broken down accordingly: 
Setup: Pins are initialized as either input or output. The serial monitor is activated also.
Loop: contains only two function calls one called “start” and another called “sensor”
Start: This checks to see if the machine is ready to operate and displays the result to 	the LEDs on the breadboard, green for ready, red for not ready. Then it check the state 	of both buttons and and if the button1 is pressed it switches the illuminated LED from 	green to red and starts the pump and opens the valve. When button1 is released it 	closes the valve, turns off the pump, and switches the on LED back to green. This is 	the momentary button. The second button, button2 will only produce results if the laser 	is inline with the photo-resistor, that is checked using the variable thresh. Like button1, 	button2 turns on the motor and opens the valve and switches the LEDs, but the motor 	and valve will stay active once button2 is released.  The pouring will continue until the 	laser gate is broken. Should something go wrong or you want to stop the automation, 	pressing any button will immediately deactivate the pump and close the valve and stop 	the flow of beer. This is done using another function called stopbutton.
Sensor: the function “sensor” collects the readings from all the inputs (photo-resistor, 	temperature sensor, and flow sensor) and prints them to the serial monitor.


User Manual for the Beer Dispenser

To operate the beer dispenser you first must power on the Ardunio with a computer as the temperature sensor, flow sensor, and photo-resistor all return values to the serial monitor. Next you must place the tube connected to the bottom of the pump into the vessel containing the liquid you wish to pour. The next thing is to ensure the laser pointer is on and lined up with the photo-resistor, and place a glass into the ring drawn on the bottom of the cardboard enclosure. Then if the green light on the breadboard is illuminated the machine is ready to operate. Pressing the first button will cause liquid to flow only while the button is held down, the second button will automatically pour until the laser gate is broken when the glass is full. While the machine is automatically pouring repressing any of the buttons will immediately stop the machine from running. You can now enjoy your perfectly poured beer.

Team
Ben Polasek
