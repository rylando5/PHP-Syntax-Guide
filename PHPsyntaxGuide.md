1. PHP comments 
PHP supports both one-line comments and multi-line comments. 
- // This is a single line comment 
- /* this is a multi line comment */
- Comments are great for leaving descriptions about the logic within your code. 
- Also a very friendly thing to do for other developers that will have to look at your code. 


2. PHP Variables 
- Variables in PHP and like most other programming languages  are meant to store data. 
- In PHP a variable does not need to be declared prior to adding a value to it. PHP will automatically convert the variable to its given value. In most cases that variable will be reuseable throughout the script. 
- the assignment operator (=) is used to assign the value to the variable. 
- All php lines are ended with a semi-colon to let the PHP engine know its the end of that statement. 

Rules and guidelines for naming variables. 
- All PHP variables must start with a $ sign. Then followed by the variables name. 
- Must start with letter or underscore_ 
- Cannot start with a number 
- Variable name cannot contain spaces. 

Constants in PHP
You might ask, what is a constant variable? A constant is a variable with a fixed value. - Once they are defined they can no longer change. 
- A prime example of when you would use a constant 
- database usernames and password, websites base URL, Or Company name. 
- Constants in PHP are defined in PHP using the define() function which then accepts two arguments 
- The name of the constant, and its value
- After it has been defined it can be accessed by using its name


Example 
$variable = "value"; 

define("VARIABLE_NAME", "Variable value");

3. Echo / Print
The echo statement is used to display things to the browser. Some would call it a cousin of console.log. 

The print statement is also used to output things to the browser. Print can only accept one argument and has a return value of 1, making it useful in expressions. 

Echo is marginally faster than print due to the fact that it has no return value and can accept multiple parameters. 

Examples
Echo:

$variable = "this is the value";
echo $variable; // outputs "this is the value";
echo "<p> You can also include inline HTML in an echo statement</p>"


Print: 
$variable = "This is me writing a string";
print $variable; // outputs "This is me writing a string"
print "<h1> You can also include inline HTML in a print statement </h1>"


4. Data Types 

The following data types are supported by the PHP engine. 
- Integers
- Strings 
- Floating Point Numbers
- Arrays 
- Booleans 
- Objects
- NULL
- Resource

Integers:
Integers are whole numbers without a decimal point. Ranging between -2147483648 and 2147483647 in 32 bit systems, and between -9223372036854775808 and 9223372036854775807 in 64 bit systems.

echo 794; // outputs 794

Strings: 
A string is a sequence of letters, numbers or special characters. They must be enclosed in "quotes". You can use either single or double. Strings can be concatenated by using a period. 

$variable = "this is a string";
echo $variable // output "this is a string"

Floating Point Numbers:
Integers that allow decimal points. 

Arrays:
An array is simply a variable that is capable of holding several values. In PHP you must specify that it is an array by using the array() keyword. Then inside the parenthesis you place your values. All arrays are zero based meaning that no matter the number of values in a array the first one will always start at 0. 

there is 3 types of arrays in PHP 
- Indexed array - A simple array with numeric key 
- Associative array - An array where each key has its own specific value. 
- Multidimensional array - An array holding one or more arrays within itself 

Indexed array: 
$video_game_characters = array("Geralt of rivea", "Yennifer", "Ciri"); 

Associative array: 
$capitals_in_countries = array("Finland"=>"Helsinki", "Russia"=>"Moscow", "Italy"=>"Rome")

Multidimensional array: 
$countries_and_capitals = array(
    array(
        "Russia"=> "Moscow"
    ),
    array(
        "Italy"=>"Rome"
    ),
    array(
        "Ukraine"=>"Kiev"
    )
);

echo "The capital of Russia is: " . $countries_and_capitals[0]["Russia"];


Booleans: 
Booleans are true/false statements. 1 = true and 0 = false
$r = true; 


Objects: 
Objects store data/information on how data should be processed. Almost like a set of instructions carried in a single "package". Objects are created based on this template via the new keyword. 

class sayHello{
    function hello(){
        echo "Hello World";
    }
}
$obj = new sayHello; 
var_dump($obj);


NULL: 
NULL represents empty variables that do not carry any data/value. If a variable hasn't been assigns a value it will automatically be given a value of NULL 

$variable = NULL; 
echo $variable // this will not have an output. 


Resources: 
A resource is a special kind of variable strictly holding a reference to an external resource i.e a database. 

$fp = fopen("test.txt", "w");
echo get_resources_type($fp) . "\n"; 



5. PHP strings 
A string is a sequence of letters, numbers or special characters. They must be enclosed in "quotes". You can use either single or double. Strings can be concatenated by using a period. Strings contain many built in functions you can use to manipulate the stings. I will provide examples of two. 

To calculate the length of a string 
strlen is used to calculate the number of characters in a sting 

$variable = "This is another string";
echo strlen($variable);  //out put 22

Counting the Numbers of Words in a string. 
str_word_count() function does exactly what it looks like. 

$variable = "oh look, another string"; 
echo str_word_count($variable); // output 4


6. PHP Numbers
One thing to note about numbers in PHP is that it provides an automatic data type conversion. Meaning that if you assign an integer a value to a variable, The type of variable will automatically be an integer. If you assign a string to the same variable the type will change to a string. 

Integer Rules: 
- Integers be in decimal, hexadecimal or octal form 
- Integers cannot contain decimal points
- Integers can be either positive or negative 
- Integers must contain at least one digit

Of course PHP contains ways to be able to check if a variable is an integer. 
- is_int()      $r = 15;        echo is_int($r)     returns 15, integer 
- is_integer()  $x = 2.5;       echo is_integer($x) returns false, not a true integer
- is_long()     $h = "hello"    echo is_long($h)    returns nothing, clearing a string not an int. 

If your variables are integers then all should return true 


Floating Point Numbers: 
Floating point numbers are simply decimal or fractional numbers. 

I will provide 2 ways to check if a variable is a floating point number. 
- is_float()    $r = 200;        echo is_float($r) // nothing will be returned why? not a float!
- is_double()   $x = 1.5;        echo is_double($x) // returns 1, 1 = true! It surely is a float!



7. PHP Constants
A constant is a variable with a fixed value. - Once they are defined they can no longer change. 
- A prime example of when you would use a constant 
- database usernames and password, websites base URL, Or Company name. 
- Constants in PHP are defined in PHP using the define() function which then accepts two arguments 
- The name of the constant, and its value
- After it has been defined it can be accessed by using its name

Example of a constant: 
DEFINE("favorite_sunglasses", "Oakley Eye-Jackets"); 
echo favorite_sunglasses // Outputs  "Oakley Eye-Jackets"



8. PHP operators
- Arithmetic operators
- Assignment operators
- Comparison operators
- Increment/Decrement operators
- Logical operators
- String operators


Arithmetic Operators: 
similar to most programming languages
+ Addition 
- Subtraction 
* Multiplication 
/ Division 
% Modulus aka "percentage" 
** Exponentiation "to the power of!" 

Assignment Operators: 
- (=) most commonly used to assign a value to a variable the left operand gets set to the value of the expression on the right
- r (+=) h Similar to addition, returning the sum of the two values. 
- r (-=) h the same as subraction, returning the difference of the two values 
- r (*=) h Similar to multiplication. returns the final product of multiplication. 
- r (/=) h Similar to division, returning the computation of the two values 
- r (%=) h Similar to modulus, returning the percentage of the two values 

PHP comparison operators
- == Equal $x == y $y returns true if $x is equal to $y
- === Returns true if the two values are identical 
- != not equal 
- !== Not identical 
- > Greater than 
- < Less than 
- >= Greater than or equal to 
- <= Less than or equal to 
- <=> Less than. Equal to or Greater than 

Increment / Decrement Operators 
- ++$y Pre-increment increments $y by one, then returns $y
- $y++ Post-increment, Returns $y then increments $y by one 
- --$x Pre-decrement Decrements $x by one then returns $x
- $x-- Post-decrement Returns $x, then decrements $x by one

PHP Logical Operators 
- And -  $x and $y   True if both $x and $y are true
- or - $x or $y      True if either $x or $y is true
- xor $x xor $y      True if either $x or $y is true but not both
- && (and)  $x && $y True if both $x and $y are true
- || (or)   $x || $y  True if either $x or $y is true
- !  (not)  !$x        True if $x is not true


String Operators: 
- . Concatenation "used to attach separate strings together"
- .= Concatenation assignment



9. If & Else & Elseif

- if (condition){
    // code will run if the condition is met
}

- if..Else
Will execute if one piece of code if a condition is met, and different piece of code if not 
else statements also do not take conditions 

if (condition){
    //this runs if condition is met
} else {
    //this executes as a last resort is previous conditions aren't met
}

- if..elseif..else
Runs code for more than two conditions 
if (condition){
// code to run if condition is met
} else if(condition) {
//code to run if this condition is met 
} else {
    last resort code to run is previous conditions aren't met
}

10. Functions 

PHP contains more than 1000 built in functions, I guess that is what makes this language so powerful. 

User defined Functions 
- A function is a block of code with a set of instructions within it that can be reused through out a script. 
- A function must be called in order to be executed. 
- A function will be execute automatically when a page loads. 

Creating a function: 
function function_name(){
    // set of "instructions" set to run once the function is called 
}

Functions with parameters or Arguments 
function function_name($firstparam, $secondparam){
//code to be run 
}; 

function_name($paramvalue1, $paramvalue2)





11. PHP arrays 
An array is simply a variable that is capable of holding several values. In PHP you must specify that it is an array by using the array() keyword. Then inside the parenthesizes you place your values. All arrays are zero based meaning that no matter the number of values in a array the first one will always start at 0. 

there is 3 types of arrays in PHP 
- Indexed array - A simple array with numeric key 
- Associative array - An array where each key has its own specific value. 
- Multidimensional array - An array holding one or more arrays within itself 

Indexed array: 
$video_game_charecters = array("Geralt of rivea", "Yennifer", "Ciri"); 

Associative array: 
$capitals_in_countries = array("Finland"=>"Helsinki", "Russia"=>"Moscow", "Italy"=>"Rome")

Multidimensional array: 
$countries_and_capitals = array(
    array(
        "Russia"=> "Moscow"
    ),
    array(
        "Italy"=>"Rome"
    ),
    array(
        "Ukraine"=>"Kiev"
    )
);

echo "The capital of Russia is: " . $countries_and_capitals[0]




12. PHP Loops
- Loops are simply used to be executed the same code over and over. If and when the condition is met the loop stops. 
- PHP contains 4 types of loops 

While loop: 
loops through a block of code as long as the condition specified evaluates true. 

while(condition){
    //code that will run
}

$total = 0;
$number = 1; 

while ($number <= 10){
    $total += $number;
    $number++;
}
echo $total; //Output 55

do while loop:
The block of code is executed once before the condition is evaluated. If the condition is met, the statement repeats forever as long as the condition stays true. 

do{
//code goes here
} while (condition that is applied)

$i = 0;
do {
 echo $i;
} while ($i > 0);
The code inside the loop body executes first to display the variable $i. Because the value of the $i is 0, the condition is met, the loop stops.

for loops:
Will loop through a block of code until its counter will reach a specified number. 
inside a for-loops condition operations are separated by semi colons 

for(starting counter value; ending of counter value; incrimination){
    //code gets executed inside the for-loops body
}


function reverse_the_loop($lets_reverse){
    for($i = 0; $i<= count($lets_reverse); $i++){
        $the_output = array_reverse($lets_reverse);
        echo $the_output[$i];
    }
    
}
reverse_the_loop($reverse);

in the example above i used this for-loop to loop backwards through an array from 6-1


Foreach loop:
Commonly used to loop through a block of code one for each of the elements within an array. 

$colors = ["red", "green", "blue"];

foreach($colors as $color){
    echo $color . '<br>';
}

output 
red
green
blue