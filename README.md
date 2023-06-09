Download Link: https://assignmentchef.com/product/solved-cs-202-computer-science-ii-project-4
<br>









<strong>Objectives:  </strong>The main objectives of this project is to test your ability to create and use C++ classes, with multiple constructors, static members/functions, and expand to operator overloading. A review of pointers, structs, arrays, iostream, file I/O and C-style strings is also included.

<strong>Description: </strong>

This project will significantly expand upon Project 3 by adding additional functionality, and implementing more abstract data types (ADTs) and their operations through classes. <strong>Pointers must be used for array manipulation</strong>, including arrays with ADTs (structs, classes) e.g, rental cars, rental agencies. <strong>Pointers must be used in function prototypes and function parameter lists</strong> – not square brackets. Make sure <u>all your C-string functions</u> (e.g. string copy, string compare, etc.) work with pointers (parameters list and function implementation). <strong>Const</strong> should be used in <strong>parameter lists</strong>,<strong> functions</strong>, and <strong>function signatures</strong> as appropriate. <u>Square brackets</u> should be used <u>only when</u> <u>declaring an array, </u>or if otherwise you specify your own overloaded <u>operator[]</u> . <strong>Pointers can only be moved by incrementing or decrementing</strong> (i.e., ++ or – -), or by <strong>setting the pointer back to the base address</strong> using the array name. You should use the arrow operator (-&gt;) with any pointers where appropriate.




The additional functionality is as follows: You are given an updated data file where there is 1 Agency location (<strong>Agency</strong>) which has <strong>5</strong> (potentially) high-tech cars (<strong>Car</strong>). Each car can also incorporate <strong>up to 3</strong> (0-3) special driving sensors (<strong>Sensor</strong>). You will have <strong>similar menu options</strong>, but the <strong>functionality has been updated</strong> below. Note: using multiple helper functions to do smaller tasks will make this project significantly easier.




<strong>The Sensor Class will contain the following <u>private</u> data members: </strong>

<ul>

 <li><strong>m_type</strong>, a C-string char array of 255 max characters (name of sensor type), valid strings for</li>

</ul>

Sensor m_type are “gps”, “camera”, “lidar”, “radar”, “none”.

<ul>

 <li><strong>m_extracost</strong>, a float (additional rent cost per day for the car that carries the sensor, for</li>

</ul>

“gps”:=$5.0/day, for “camera”:=$10.0/day, for “lidar”:=$15.0/day, for

“radar”:=$20.0/day, for “none”:=$0.0/day)

<ul>

 <li><strong>gps_cnt</strong>, a <u>static</u> int member (keeps track of existing gps-type sensors)</li>

 <li><strong>camera_cnt</strong>, a <u>static</u> int member (keeps track of existing camera-type sensors)</li>

 <li><strong>lidar_cnt</strong>, a <u>static</u> int member (keeps track of existing lidar-type sensors)</li>

 <li><strong>radar_cnt</strong>, a <u>static</u> int member (keeps track of existing radar-type sensors) <strong>and will have the following methods: </strong></li>

 <li><strong>Default Constructor</strong> – will set the aforementioned data members to default initial values.</li>

 <li><strong>Parameterized Constructor</strong> – will create a new object based on the values passed into it.</li>

 <li><strong>Copy Constructor </strong>– will create a new object which duplicates an input Sensor Ø <strong>Get/Set methods </strong>for appropriate data member(s).</li>

 <li><strong>A Get and a Reset</strong> static member function to return and to reset each of the static member variables.</li>

 <li><strong>A Method to check if 2 Sensor Objects are the same. </strong>You <u>should </u>make this an operator overload of (<u>operator==</u>). You may want to try for practice to make it a non-Class Member function which will have to access member data over Class methods.</li>

</ul>




<strong>The Car Class will contain the following <u>private</u> data members: </strong>

<ul>

 <li><strong>m_make</strong>, a C-string char array of 255 max characters (car make)</li>

 <li><strong>m_model</strong>, a C-string char array of 255 max characters (car model)</li>

 <li><strong>m_year</strong>, an int (year of production)</li>

 <li><strong>m_sensors</strong>, a Sensor class type array of size 3 (max allowable number of sensors per car). <em>Hint</em>: You are allowed to use an auxiliary member variable of your choice to keep track of how many actual sensors exist onboard, this will also help for instance in case adding a new sensor is required.</li>

 <li><strong>m_baseprice</strong>, a float (price per day for the sensorless vehicle)</li>

 <li><strong>m_finalprice</strong>, a float (price per day with the increased cost of the car sensors) Ø <strong>m_available</strong>, a bool (1 = true; 0 = false; try to display true/false using the</li>

</ul>

“std::boolalpha” manipulator like: cout &lt;&lt; boolalpha &lt;&lt; boolVariable; )

<ul>

 <li><strong>m_owner</strong>, a C- string char array of 255 max characters (the current lessee; if no lessee, i.e.</li>

</ul>

the Car object is available), set to a ‘ ’-starting (0-length) C-string).

<strong>and will have the following methods: </strong>

<ul>

 <li><strong>Default Constructor</strong> – will set the aforementioned data members to default initial values.</li>

 <li><strong>Parameterized Constructor</strong> – will create a new object based on the values passed into it. Ø <strong>Copy Constructor </strong>– will create a new object which duplicates an input Car</li>

 <li><strong>Get methods </strong>for data members.</li>

 <li><strong>Set methods </strong>for data members except the <strong>m_sensors</strong>, and<strong> m_finalprice</strong>.</li>

 <li><strong>UpdatePrice </strong>– a method to update the <strong>m_finalprice</strong> after any potential changes (to the <strong>m_baseprice</strong> or the <strong>m_sensors</strong>)</li>

 <li><strong>Print </strong>– will print out all the car’s data.</li>

 <li><strong>EstimateCost</strong> – will estimate the car’s cost <em>given</em> (a parameter passed to it) a number of days to rent it for.</li>

 <li><strong>A Method to Add a Sensor </strong>to the Car You <u>should</u> make this an operator overload of (<u>operator+</u>). <em>Hint</em>: a Car Class member method will be the better choice, since it will have access to private members. You may want to try that for practice.</li>

 <li><strong>A Method to Add a lessee (the name of a lessee) </strong>to the Car You <u>should</u> make this an operator overload of (<u>operator+</u>). <em>Hint</em>: bear in mind what “adding a renter” to a Car object might imply about other data members.</li>

</ul>




<strong>The Agency Class will contain the following <u>private</u> data members: </strong>

<ul>

 <li><strong>m_name</strong>, a C-string char array of 255 max characters (</li>

 <li><strong>m_zipcode</strong>, a <u>preferably </u><u>const</u> int number of size 5</li>

 <li><strong>m_inventory</strong>, an array of Car objects with a size of 5 <strong>and will have the following methods: </strong></li>

 <li><strong>Default Constructor</strong> – will set the aforementioned data members to default initial values.</li>

 <li><strong>Get/Set methods </strong>for <strong>m_name</strong> and <strong>m_zipcode</strong> data members – <strong>by-Value</strong>.</li>

 <li><strong>A Method to Index an Object of the</strong> <strong>m_inventory</strong> data member – <strong>by-Reference</strong>. (<em>Hint</em>: This will allow you to access (read and write) to the agency’s inventory like in Project_3.) You <u>should</u> make this an operator overload of (<u>operator[]</u>). <em>Reminder</em>: Any calls to this operator are excluded from the Project’s restrictions about using brackets.</li>

 <li><strong>ReadAllData</strong> – read all of the data for the agency from a user-provided file.</li>

 <li><strong>PrintAllData</strong> – prints out all of the data for an agency (including car info).</li>

 <li><strong>PrintAvailableCars</strong> – prints out all of the data (including Car info) only for the available Car Objects of the agency.</li>

</ul>







<strong>The menu must have the following updated functionality: </strong>

<ul>

 <li><strong>1) Read ALL</strong> data from <strong>file</strong>. The provided sample file HighTechAgency.txt is <strong>structured</strong> :</li>

</ul>

The <u>first line is the car agency</u> info, <u>followed by 5 cars</u>.

For each car the order is: <u>year make model baseprice {sensors} available [lessee].</u>

The <u>sensors are enclosed in {braces}</u> and can be <u>0 up to 3 ws-separated names</u>.

The <u>lessee name is [optional]</u>, it will only be there <u>if the car is available</u>.

<ul>

 <li><strong>2) Print to terminal ALL data</strong> for <strong>the Agency</strong> and <strong>all its corresponding Cars</strong> in a way that demonstrates this relationship (similarly to Project_3).</li>

 <li><strong>3) Print to terminal </strong>the<strong> TOTAL number of sensors</strong> built to equip the agency’s car fleet (total number by sensor type).</li>

 <li><strong>4) Find</strong> the <strong>most expensive available </strong>car – <strong>ask the user</strong> if they want to rent it – update that car’s <strong>lessee and availability status</strong> if the user says yes.</li>

 <li><strong>5) Exit</strong></li>

</ul>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>The following minimum functionality and structure is required: </strong>

<ul>

 <li>Ask the <strong>user</strong> for the <strong>input file </strong></li>

 <li>The list of <strong>Sensors</strong> must be stored in an <strong>array of Objects</strong>.</li>

 <li>The list of <strong>Cars</strong> must be stored in an <strong>array of Objects</strong>.</li>

 <li>Use <strong>character arrays</strong> to hold your strings (i.e., C-style) exclusively (using the string data type is still not allowed).</li>

 <li>Write <strong>multiple functions</strong> (<em>Hint</em>: You could have each menu option be a function).</li>

 <li>At least one function must use <strong>Pass-by-Reference</strong>.</li>

 <li>At least one function must <strong>Return-a-Reference</strong>.</li>

 <li>Otherwise, as before, you are free to use <strong>pass by-Value, pass by-Reference</strong>, <strong>pass byAddress</strong> for your function parameters.</li>

 <li>Variables, data members, functions, function signatures, should all be <strong>const</strong> in a perfect program, unless there is no other way for the program to work. (This might seem as an overstatement. However, try to remember the <strong>const</strong> keyword and design around it as much as you can). You are <u>required</u> to at least <u>try</u>.</li>

 <li><strong>Pointers </strong>must be used for<strong> all array manipulation</strong> (iterating over elements to read/modify <u>cannot</u> be performed with bracket operator accessing). The only exception on [] is if you are using your own overload of operator[].</li>

 <li><strong>Pointers </strong>must be used in<strong> function prototypes </strong>and<strong> function parameter lists </strong>(the bracket notation is not allowed in parameters lists).<strong>Pointers </strong>can only be<strong> moved by incrementing or decrementing</strong>:</li>

</ul>

<strong>double</strong><strong> d</strong><strong>[</strong><strong>3</strong><strong>]</strong><strong> = {1,2,3}; </strong><strong>double*</strong><strong> d_Pt = d; </strong>

<strong>for</strong><strong> (</strong><strong>int</strong><strong> i=0; i&lt;3; ++i,++d_Pt){ </strong><strong>cout</strong><strong> &lt;&lt; </strong><strong>*</strong><strong>d_Ptd; } </strong>

<ul>

 <li>Or by<strong> setting </strong>the pointer<strong> back to the base address</strong> using the array name. <strong>d_Pt = d; </strong><strong>cout</strong><strong> &lt;&lt; </strong><strong>*</strong><strong>d_Pt &lt;&lt; endl; </strong></li>

 <li>Write your <strong>own C-string copy</strong>, <strong>C-string compare</strong> Their prototypes will have the form (you must use the prototypes exactly as provided, with <strong>char *</strong> parameters):</li>

</ul>

<strong>// copies characters from source to destination until a NULLcharacter ‘ ’ is found in source, then it NULL-terminates destination too, and returns  </strong><strong>void</strong> <strong>myStringCopy</strong><strong>(</strong><strong>char *</strong><strong> destination, </strong><strong>const char * </strong><strong>source);</strong>

<strong> </strong>

<strong>// returns 0 when the strings match, i.e. their characters are equal one-by-one until a NULL-character ‘ ’ is found in both strings and at the same position as well </strong>

<strong>// returns a value &lt;1 if the first character that does not match has a lower value in str1 than in str2 </strong>

<strong>// returns a value &gt;1 if the first character that does not match has a higher value in str1 than in str2  </strong><strong>int </strong><strong>myStringCompare</strong><strong>(</strong><strong>const char *</strong><strong> str1, </strong><strong>const char *</strong><strong> str2);</strong> <strong> </strong>

Ø The other functionality and structure of the program should remain the <strong>same as Project #3</strong>, including <strong>writing to screen</strong> and <strong>file</strong>, as well as<strong> restrictions on string</strong> libraries, <strong>global variables</strong> and <strong>constants</strong>, etc.




<strong>Implement the concepts of encapsulation and data hiding (necessary)! </strong>

<strong>Use the const keyword where appropriate (almost everywhere you can make it)! </strong>

<strong>Implement Class Constructors with Initializer-Lists as much as possible (advised)! </strong>

<strong>            </strong>

<strong>Implement operator overloads as much as you can ! </strong>

<strong>            </strong>This is a chance to experiment as much as possible with more advanced concepts and the intricacies of classes. It is not a strict requirement that <strong>const</strong> data members which can only be instantiated with a list initialization are there in your code right now, neither is it necessary to make your member functions in the operator overload approach. Try your best in order to acquaint yourself with these new concepts however, and figure out what might be giving you a hard time understanding and/or implementing at this early point. <strong> </strong>

<strong>The completed project should have the following properties: </strong> Ø Written, compiled and tested using Linux.

<ul>

 <li>It must compile successfully using the g++ compiler on department machines. Instructions how to remotely connect to department machines are included in the Projects folder in WebCampus.</li>

 <li>The code must be commented and indented properly.</li>

</ul>

Header comments are required on all files and recommended for the rest of the program. Descriptions of functions commented properly.

<ul>

 <li>A one page (minimum) typed sheet documenting your code. This should include the overall purpose of the program, your design, problems (if any), and any changes you would make given more time.</li>

</ul>

<strong> </strong>

<strong>Turn in:</strong> Compressed .cpp file and project documentation.




<strong>Submission Instructions: </strong>

<ul>

 <li>You will submit your work via WebCampus</li>

 <li>Name your code file proj4.cpp</li>

 <li>If you have header file, name it proj4.h</li>

 <li>If you have class header and source files, name them as the respective class (Sensor.h Sensor.cpp Car.h Car.cpp Agency.h Agency.cpp) This source code structure is not mandatory at this point, but advised.</li>

 <li>Compress your:

  <ol>

   <li>Source code</li>

   <li>Documentation</li>

  </ol></li>

</ul>

Do not include executable  Ø Name the compressed folder:

PA#_Lastname_Firstname.zip

([PA] stands for [ProjectAssignment], [#] is the Project number)  Ex: PA4_Smith_John.zip







<strong>Late Submission:</strong>

A project submission is “late” if any of the submitted files are time-stamped after the due date and time. Projects will be accepted up to 24 hours late, with 20% penalty.

















