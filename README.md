# Exercise-3---garage-management-system
Implementation of working with classes, inheritance and polymorphism (*) Use of Collections implementation enums (*) (*) Development and use of external Dll (assembly). (*) Work with several projects (*) Work with Exceptions


the exercise
The ultimate goal: a small system that "manages" a garage.
The system will know how to manage a garage that currently handles five types of vehicles -
 A regular motorcycle
(2 wheels with maximum air pressure 28, Octan98 type fuel, 5.5 liter fuel tank)
 Electric motorcycle
(2 wheels with maximum air pressure 28, maximum battery time - 6.1 hours)
 A normal car
(4 wheels with maximum air pressure 30, Octan95 type fuel, 50 liter fuel tank)
 Electric car
(4 wheels with maximum air pressure 30, maximum battery time - 8.2 hours)
 Truck
(16 wheels with maximum air pressure 26, Soler type fuel, 110 liter fuel tank)

Each vehicle has the following features:
 Model name (string)
 License number (string)
 The percentage of energy remaining in its energy source (for the fuel/electricity meter (float)
 A collection of wheels
Each wheel has the following features:
o Manufacturer name (string)
o Current air pressure (float)
o Maximum air pressure set by the manufacturer (float)
o Inflating operation (a method that receives data about how much air to add to the wheel, and changes the
The state of the air pressure if it does not exceed the maximum )

A motorcycle (regular/electric), in addition to the features of a car, also has the following features:
A, A1, A2, B: type license 
 Engine volume in cc (int)
A (regular/electric) car, in addition to the features of a car, also has the following features:
 Color (the possible colors are: yellow, white, black, blue)
(5 or 4, 3, 2) quantity doors
A truck, in addition to the features of a car, also has the following features:
 Do you transport dangerous materials (bool)
 Cargo volume - float
In vehicles that run on fuel, you can find the following information and activate the following actions:
(Soler, Octan95, Octan96, Octan98) Fuel type 
 Current amount of fuel in liters (float)
 The maximum amount of fuel in liters (float)
 Refueling operation (a method that accepts the amount of liters to add and the type of fuel, and changes the state of the fuel
If the type of fuel is suitable and there is no deviation from the size of the tank )

In electric vehicles you can find the following information and activate the following actions:
 Remaining battery time in hours (float)
 Maximum battery time in hours (float)
 Battery charging operation (a method that receives a figure that is the number of hours to add to the battery and "charges" the
The battery respectively as long as the number of hours does not exceed the maximum (
The following data must be kept on every vehicle in the garage:
 Owner name (string)
 Owner phone (string)
 The condition of the vehicle in the garage (possible states: under repair, repaired, paid)
o Every vehicle that enters the garage is in its initial state 'under repair'.

The system will provide the following functionality to its user:
1. To "put" a new car into the garage. If you try to enter a vehicle that is already in the garage (according to the license number),
The system will issue an appropriate message and use the vehicle that is already in the garage (and transfer the status).
The vehicle is "under repair"
2. Display the list of the license numbers of the vehicles in the garage, with the option of filtering according to the situation
theirs in the garage.
3. Change the status of a vehicle in the garage (the data requested from the user is the license number and the new status).
4. To inflate the car's tires to the maximum (according to the license number)
5. Refuel a vehicle that is driven by fuel (the data is license number, type of fuel to fill, amount to fill)
6. Charge an electric vehicle (the data is a license number, amount of minutes for charging)
7. Display complete vehicle data by license number (license number, model name, owner's name, condition
In the garage, the details of the wheels (air pressure and manufacturer), fuel condition + type of fuel / battery condition, and other details
relevant to the specific type of vehicle )

In order to develop the system, a Solution must be created that will contain two projects:
Ex03.GarageLogic .1
This is a project that produces a non-PE assembly dll (which only contains the object model).
and the logical layer of the system (the layer we would like to reuse even if
A different user interface than Console will open.)
This layer does not know how to print to the screen or receive data from a console.
To generate a dll, go to the properties of the project and select the option:
Output type: Class Library

Ex03.ConsoleUI .2
This is a project that produces the exe and in which there is an implementation of the user interface in the management system
Garage in Consul. This system uses the model implemented in the first project by
reference to the first project
