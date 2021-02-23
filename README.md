# simple_pandemic_simulation
I’ve spent literally too many hours on this project, unfortunately, from time to time, there are some bugs, it’s far from perfect.<br>
To remove an agent, first it needs to be selected by clicking it. Clicking on agents also marks current agent path for couple of seconds. Program loads the map from json file, that was created using program “Tiled” (open source tile map creator). Sliders allow adjustment of several parameters.
Every step specific agent make, it uses A* to find best possible route. 
There should be only one agent at one tile at the same time (expect for shops).
Map contains teleporters, so there was need to create special heuristic for used A* algorithms. 
Teleports works similarly to intersections (there can be only one agent inside two tiles that build a teleporter). 
A* implementation includes existance of teleports. 
Agents can infect other agents on adjacent tiles, and while they are inside the shop. 
I hope, despite the shortcomings of the project I’ve show a lot of effort. I’ve tried my best to stick to OOP objectives, and also I’ve tried to implement at least couple of design patterns.<br>
Program can be run using following comand:<br>
java --module-path path_to_javafx --add-modules javafx.controls,javafx.fxml,javafx.media -jar path_to_jar_file "path to my_second_map.json"
<br>
Example:<br>
java --module-path C:/Users/Janek_PC/Desktop/openjfx-11.0.2_windows-x64_bin-sdk/javafx-sdk-11.0.2/lib --add-modules javafx.controls,javafx.fxml,javafx.media -jar C:/Users/Janek_PC/IdeaProjects/opp_fx/out/artifacts/opp_fx_jar2/opp_fx.jar "C:\\Users\\Janek_PC\\Desktop\\my_second_map.json"