# ESP32 Weather Station
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Anish R. | Lynbrook High School | Electrical Engineering | Incoming Junior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/ioF2Q5K0R9g?si=t-uc9BIFGQG2-f9l" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my second milestone, I was able to add a gas sensor to my project which I coded to pick up CO2 readings(in PPM) from its environment. I was also able to get this CO2 data displayed on a site called ThingSpeak. What this modification allows me to do is to collect live data locally and store and visualize it somewhere. I have been surprised by how integrating code from different tutorials to make different parts of the project work(e.g. the sensor, uploading data to ThingSpeak, getting data from OpenWeatherMap) produces bugs which are oftentimes simple to solve. I have also been surprised as to how certain, simple parts of the project and the way parts of it fundamentally work, like making a variable the correct datatype, and not understanding the way the esp32 worked led to major bugs and issues with my project. While completing this milestone, I ran into some issues such as when trying to integrate code to upload data to ThingSpeak with the code I had so far. I was using temperature data from OpenWeatherMap as a placeholder for CO2 data since I had not received the sensor at the start of the week but had  started trying to upload code to ThingSpeak on the first day of the week. I had a hard time uploading the temperature data and eventually found out it was due to its datatype and eventually was able to properly convert the temperature values to a proper data type. I also had issues with the gas sensor only giving readings of 0. After experimenting with the code I had and attempting to debug, my instructor and I realized that the sensor, which gave values in analog, was connected to a pin using the same Analog-Digital converter on the esp32 as the WiFi, allowing us to solve the problem. For my final milestone, I want to fine tune my code to refine the project, make CO2 readings more accurate with a library for the sensor, and complete another milestone, perhaps doing something with the live data from the gas sensor.


# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/1Nc4m7QwlBI?si=LO3d6VFibx1tRRjC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My first milestone was completing my base project which was getting weather data for some city(Lancaster, in my case) through OpenWeatherMap with the esp32 and displaying it on a display module. I wired the esp32 to the display through a breadboard, connecting the display to the esp32’s ground pin and power pin as well as to data pins 21 and 22. This enabled the display to receive power and display things with code through the esp32. I also followed two separate tutorials, one that showed me how to get weather data from OpenWeatherMap and another that showed me how to display things to the display module. After this, I worked to combine the two different codes from the tutorials and now have the display module showing live temperature, pressure, humidity, and wind speed data for Lancaster, US. One challenge I faced was getting data from OpenWeatherMap, as doing so through the code requires an API key, something I was not familiar with. Due to this, I was confused when trying to fetch OpenWeatherMap data but eventually was able to do it. Additionally, when trying to combine the code for the display module and OpenWeatherMap data, I did not fully understand all parts of both codes and how something actually gets displayed to the display. I worked with my instructor to understand how to combine the code without my errors and he also explained the concept of a buffer, which gets built up with each command to display something but must be pushed onto the display with a display.display() command. Another big issue I faced was too much data being displayed on the display, which is less than a square inch large. I tried implementing scrolling to display all the text cleanly, which was not successful, and instead listed out only the important information, as not all information initially displayed was relevant for a user, line by line. My next steps are to do a modification, likely either with a new piece of hardware which could collect local data to be displayed, or by harnessing the esp32’s WiFi capabilities.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
