# CortanaCommands
Custom Cortana MQTT command visual studio project
This is a complementary code sample by ElectronHacks.com please visit the links below for more info.

Use this project to create custom Cortana commands using MQTT (or other stuff).

For instance, in this example you can say "Cortana, please open the garage door" and a command will be sent to your MQTT server to open your garage door (MQTT garage door not included but I have another video on that).

Referenced library is M2MQTT, installed via github
This is a Visual Studio 2015 project.

The project is UWP Windows Universal Platform so it can run on your computer, laptop, tablet, and phone with no changes, just target your OS in Visual Studio and deploy (debug)

You only need to debug the project once then you will find it in your windows 10 start menu, after that just say "Hey Cortana" to get Cortana to listen, "Please" this is the callable name of the program, you could change it to whatever you want, then "open the garage door" Cortana will launch the program and send the MQTT message then close

The program can tell the difference betweeen being launched by cortana and being launched by the user, if launched buy the user a page opens where the user can execute the commands by pressing buttons.

To test download a MQTT test client like MQTT.fx, connect to iot.eclipse.org, subscribe to topic Cortana/# to wach the MQTT traffic. If the program can't connect to the MQTT Broker it will crash.


------------

Tutorial found here:

YouTube video: https://www.youtube.com/watch?v=0d4Q0tzI7X4

Blog post: http://www.electronhacks.com/2016/06/custom-cortana-mqtt-commands/


------------

Some shutouts to smart people that helped me figure this out because they shared their knowledge online...

Charles Clayton on YouTube with custom Cortana commands: 
https://www.youtube.com/watch?v=0Wcn-ZK9mi4 
https://www.youtube.com/watch?v=GICF03UAOcQ&feature=youtu.be

Bob Tabor. There is a great windows 10 video tutorial series on MSDN 80 videos long, this is great if you are a beginner to learn how to code with Visual Studio and make UWP apps. There is also a cool Cortana Example.
https://channel9.msdn.com/Series/Windows-10-development-for-absolute-beginners
https://channel9.msdn.com/Series/Windows-10-development-for-absolute-beginners/UWP-079-Hero-Explorer-Cortana-Integration

Paolo Patierno, the maker of M2Mqtt library. Here is the example that made me realize it actually was simple to use MQTT in Universal Windows apps. The code is supposed to run on a raspberry pi running windows 10 core but with a little coaxing you can figure out how to get it running on regular windows.
https://paolopatierno.wordpress.com/2015/08/17/windows-iot-core-and-m2mqtt-a-simple-marriage/
