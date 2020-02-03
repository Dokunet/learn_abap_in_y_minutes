# learn_abap_in_y_minutes


* --Comments--
* single line comments start with the multiplication symbol.
" comments can be put at the end of a line with a "

* Text output on screen for the user with WRITE
WRITE('Hello World')
* for assigning strings both ' and " are allowed.

* --Überlegungen zu was noch hier rein kommt--
* Some basic information on SAP ABAP
* Lines end with a dot. (As opposed to Java's ;)
* Methods, classes, if's, loop's are closed with ENDMETHOD, ENDCLASS, ENDIF, etc. (As opposed to Java's })
* ABAP is the main programming language for SAP's ERP software and is strictly bound to this software
* Most programms in ABAP are in a dialog with the user. Hence the many ways to get user input or tools for visualisation and GUI building.
* reading and filling tables while sometimes refacturing the information is the bread and butter of ABAP Developers.
* that is the reason why i will introduce the SQL coding capabilities of ABAP
* Keywords are written with all caps


* --Messages--
* Messages can be used as notifications or warnings to the user. They come in a variety of presets




* Variables, datatypes, inline, typisierung

DATA(x) = 3. 	" inline declaration of variable. Assignment of value needed. 

DATA:		" declaring multiple Data
      some_variable		TYPE int4,		" variable of type integer length 4 bit?
      some_string		TYPE string,		" variable of type string.
      some_table		TYPE TABLE OF string,	" table that holds only strings
      some_structure		TYPE REF TO.		" 

* booleans are represented with " " for False and "X" for True.

* Arithmetic operations and braces need spaces, seperating them from the numbers. beware of the spaces between operators, braces and numbers. 

addition = 1 + 2.		 " => 3.
subtraction = 5 - 7.		 " => -2.
multiplication = ( 3 * 4 ).	 " => 12.
division = 20 / 4.		 " => 5.
potentiation = 2 ** 4.		 " => 16.
whole_number_division = 7 DIV 4. " => 1.
modulo = 7 MOD 3.		 " => 1.


* --Conditionals--
IF addition < multiplication.
 WRITE "1+2 is smaller than (3*4)".
ELSEIF potentiation > division.
 WRITE "2**4 is bigger than 20/4".
ELSEIF whole_number_division = modulo.
 WRITE "7 DIV 4 is equal to 7 MOD 3".
ELSE.
 
ENDIF.

* --Logical operators--




* --Loops--

WHILE <Bedingung> <Keyword>.
<zu wiederholendes>

ENDWHILE.


* --Structures--
* Structures -> arrays -> one dimensional

* the keyword Types lets us create custom datatypes. These custom datatypes are structures (which can be thought of as one dimensional arrays).
TYPES:
       BEGIN OF first_type,				" first_type is the name of our custom structure
         first_attribute TYPE string,			" attributes for first_type are initialized with their respective datatype
         second_attribute TYPE integer,			" 
       END OF first_type,				" beware that there needs to be a comma here! not a point as one might have thought.

       BEGIN OF second_type,				" multiple types can be defined after the keyword TYPES.
         first_attribute TYPE string,			
         second_attribute TYPE TABLE OF some_table,	" attributes can be tables	
	 third_attribute TYPE first_type,		" or structures like custom datatypes themselves
       END OF second_type.				" at last here goes the full stop.

some_string = first_type-first_attribute.		" you get values out of structures with the - .

MOVE-CORRESPONDING first_type TO second_type.		" this will put the values of attributes in first_type into corresponding attributes of second type. Corresponding meaning, attributes of the same name.

* --internal Tables two dimensional--




* --Field Symbols--
* Field symbols are usefull when reading data from an internal table. they allow one to iterate over an internal table without creating a structure in memory.




* --SQL Select Statements and Databank Tables--




* --Functions (Perform)--




* --Classes--
* Definition and Implementation (like in c in 2 different files)




* --Methods--
* can be called with -> or => for static methods




* --Setting up ALV Table (Table visualization)--

* --Field Catalog--



* --Parameters and Select Options--




* --Debugging--




* --Eigenheiten der SAP GUI und Navigation--




* --Besonderes und Vergleiche--

*- IMPORTING und EXPORTING immer aus sicht dessen, was gerade verwendet wird





* wichtige Transaktionen:
* SE24, Klassen anschauen/bauen
* SE11, Tabellen oder andere Datentypen anschauen/bauen


* Um Auftrag abzuschließen:
* SE10
* F9 auf unteren (Auftrag den man abschicken möchte)
* F9 auf oberen
* stms
* nach unten scrollen
* aktualisieren und auf wagen drücken
* synchron machen
* haken wegnehmen
* transportnummer speichern (strg + y)


