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
