Download Link: https://assignmentchef.com/product/solved-practical-final-exercise-part-1-and-2-solution
<br>
Practical Final Exercise part 1

Your task is to write a program that will store GPS data based on location of the reading. To complete this task, we will use a custom data model and implement the Observer and Adapter design patterns. Refer to the included driver for questions on class and method names used.

<ol>

 <li>Custom Data Model</li>

 <li>Create a data interface that will define only getters for Location(String), Time(Calendar), Longitude(double), Latitude(double), Altitude(double), and Speed(double).</li>

</ol>

Location will be based on Zip Code which may have a dash, so use String for this.

(1 interface-GPSDataInterface)

<ol>

 <li>Create a class that will store this data interface in a Map with the location as the key and a sorted set of the data interface as the value.</li>

</ol>

* Constructor will take a Comparator parameter

* get the most recent data object based on the location as a parameter-getCurrentGPS

* add data object with the data interface as a parameter-add

(1 class-GPSDataManager)

<ol>

 <li>For sorting, create a comparator class that implements the Comparator Interface and base the comparison on time. This will be used when creating the sorted set.</li>

</ol>

(1 class-CalendarComparator)

<ol start="2">

 <li>Adapter Pattern</li>

</ol>

A data class from a customer will be used that contains Location(int), Time(Date), Longitude(double), Altitude(double), and Velocity(double) (note the different name,

data type, and missing elements).

<ol>

 <li>Code a Data Class that will represent this data with appropriate constructor for setting the data and getters for the data.</li>

</ol>

(1 class-ExternalGPSData)

<ol>

 <li>Code an adapter class that will translate the data from the external data object to your data interface. Return 0 for any missing data elements and convert data as</li>

</ol>

needed.

(1 class-ExternalGPSDataAdapter)

<strong><u>The following instructions above this sentence is supposed to be for the file</u></strong><strong><u> </u></strong><em><strong><u>FinalExercisePart1.java</u></strong></em>




<strong><u>The following instructions below this sentence is for the file</u></strong><strong><u> </u></strong><em><strong><u>FinalExercise.java</u></strong></em>

Practical Final Exercise Part 2

Your task is to write a program that will store GPS data based on location of the reading. To complete this task, we will use a custom data model and implement the Observer and Adapter design patterns. Refer to the included driver for questions on class and method names used.




<ol>

 <li>Observer Pattern</li>

 <li>Create custom listener interface for added data only with the method: gpsDataModified.</li>

</ol>

(1 interface-GPSDataListenerInterface)

<ol>

 <li>Create a custom Event class to be used for the added. The added data event will push the added data object out with the method: getData.</li>

</ol>

(1 class-GPSDataEvent)

Incorporate this into the custom data manager and fire events for the add and remove methods.


