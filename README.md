Download Link: https://assignmentchef.com/product/solved-csci1100-homework-1-calculations-and-strings-2
<br>
<h2>Input format for homeworks in this class</h2>

Your program must read the same number of inputs as are required according to the given problem. For example, if we tell you to read a name first and an email address next, that means your program must have two input statements. If it does not, you will get an error like:

EOFError: EOF when reading a line

This means either you are trying to read too many or too few inputs. Read the problem specification carefully.

In all homeworks, we will use a convention specific to CS-1. If we ask you to read an input, then after you read it you must immediately print that input. For example, the following is the correct method to input the name string and the email address string:

name = input(<sup>’</sup>Enter a name ==&gt; <sup>’</sup>) print(name) email = input(<sup>’</sup>Enter an email ==&gt; <sup>’</sup>) print(email)

The above program will produce a different output in Wing IDE and on Submitty, as shown below:

If you forgot to add the print function calls, you would actually see something like this in the submission server which will be considered incorrect output:

Please enter a name==&gt; Please enter your email==&gt;

The difference — and this is not really important for actually completing Homework 1 — is that for each part of the homework, we place all the input into a file and do what’s called “running from the command-line.” In the above example, we are using an input file (let’s assume it is called input.txt) that contains the two strings Rensselaer and <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2a585a4343444c456a585a43044f4e5f">[email protected]</a> on two lines.

When a program is run from a command shell, we use a command-line of the form:

python part1.py &lt; input.txt

Unfortunately, the free version of the WingIDE that we have been using in class does not allow us to specify this input. But, you can do the command-line form on Mac/Linux with a Terminal window, and on Windows using Linux-derived Cygwin tools. If you want to learn how, you can ask us during office hours. Anyway, here is the bottom line:

<strong>Anytime you read input, just print it immediately afterwards to match the expected output.</strong>

<h1>The Actual Homework Description</h1>

With all of that as a backdrop, here is the actual homework assignment, in three parts.

<h2>Part 1: Astronomical Calculations</h2>

Jupiter, the largest planet in our solar system, has a diameter of 88,846 miles and its average distance from the Sun is about 483,632,000 miles. These are big numbers and as such they are a bit hard to understand intuitively. One way to appreciate them is to compare them to the values for Earth, which has a diameter of 7,926 miles and a distance from the Sun of about 92,957,100 miles. The size can also be compared to the Sun, which has an average diameter of about 864,938 miles. Use 186,000 miles per second as the speed of light. Write a Python program to calculate and output

<ol>

 <li>the ratio of the Sun’s radius to Jupiter’s,</li>

 <li>the ratio of the Sun’s radius to Earth’s,</li>

 <li>the ratio of Jupiter’s radius to Earth’s,</li>

 <li>the ratio of Jupiter’s distance from the Sun to the Earth’s distance from the Sun,</li>

 <li>the ratio of Jupiter’s volume to that of the Earth (assuming both are spheres),</li>

 <li>the time in minutes it takes light to travel from the Sun to Earth (use 186<em>,</em>000 miles per second as the speed of light), and</li>

 <li>the time in minutes it takes light to travel from the Sun to Jupiter.</li>

</ol>

Your output must match

Sun-to-Jupiter radius ratio: &lt;number&gt;

Sun-to-Earth radius ratio: &lt;number&gt;

Jupiter-to-Earth radius ratio: &lt;number&gt;

Jupiter-to-Earth Sun distance ratio: &lt;number&gt;

Sun-to-Jupiter volume ratio: &lt;number&gt;

Sun-to-Earth volume ratio: &lt;number&gt;

Jupiter-to-Earth volume ratio: &lt;number&gt;

Sun to Earth light travel time in minutes: &lt;number&gt;

Sun to Jupiter light travel time in minutes: &lt;number&gt;

where in each case &lt;number&gt; is replaced by the floating point value your program calculates. <strong>You must </strong>use the value 3.14159 for <em>π </em>or your output will differ from ours. (We will see very soon how to get more accurate values of <em>π</em>.)

Your program must have the five distances and diameter values typed into the code each <strong>exactly once </strong>and then use variables after that. This would make it easy to change if, for example, we decided to use the values for Saturn instead. It would be even better if a string variable stored the name for Jupiter and then this name were used in the print statements.

Upload your Python program file to Submitty as Part 1 of HW 1.

<h2>Part 2: Speed Calculations</h2>

Many exercise apps record both the time and the distance a user covers while walking, running, biking or swimming. Some users of the apps want to know their average pace in minutes and seconds per mile, while others want to know their average speed in miles per hour. For example, if I run 6.3 miles in 53 minutes and 30 seconds, my average pace is 8 minutes and 29 seconds per mile and my average speed is 7.07 miles per hour.

Your job in Part 2 of this homework is to write a program that asks the user for the minutes, seconds and miles from an exercise event and outputs both the average pace and the average speed. Here is an example showing the expected output of your program:

Minutes ==&gt; 53

Seconds ==&gt; 30

Miles ==&gt; 6.3

Pace is 8 minutes and 29 seconds per mile. Speed is 7.065420560747664 miles per hour.

You can expect minutes and seconds to both be integers, but miles will be a float. The two outputs for the Pace must both be integers, so please use integer division and remainder operations. Note that if you have a float value then the function int gives you the integer value. For example

&gt;&gt;&gt; x = 29.52

&gt;&gt;&gt; y = int(x)

&gt;&gt;&gt; print(y)

29

The output for the Speed will be a float. (Very soon we will learn methods for shortening the speed output, but we will not do so for this assignment.) Notice that our solution generates the blank line before the output of the calculations. When you have tested your code and are sure that it works, please submit it as Part 2 of Homework 1.

<h2>Part 3: Madlibs</h2>

In this part you will write a Python program to construct the Madlib given below:

Hello &lt;proper name&gt;,

Good morning! Are you looking forward to a/an &lt;adjective&gt; &lt;noun&gt;?

You will &lt;verb&gt; a lot of &lt;noun&gt; and feel &lt;emotion&gt; when you do.

If you do not, you will &lt;verb&gt; this &lt;noun&gt;.

Did you watch the &lt;noun&gt; this &lt;season&gt;?

Were you &lt;emotion&gt; when the &lt;team-name&gt; won?

Have a/an &lt;adjective&gt; day!

You will ask the user of the program for the missing words — those enclosed in &lt; &gt; — using the input function. You will then take all the user specified inputs, and construct the above Madlib. (Be sure to reread the <em>Input format for homeworks in this class </em>discussion in the instructions above.) Make sure your output looks like the above paragraph, except that the missing information is filled in with the user input. Here is an example run of the program (how it will look at the homework submission server):

Let<sup>’</sup>s play MadLibs for Homework 1 Type one word responses to the following: proper_name ==&gt; Alex adjective ==&gt; interesting noun ==&gt; semester verb ==&gt; write noun ==&gt; code emotion ==&gt; proud verb ==&gt; struggle noun ==&gt; semester noun ==&gt; Olympics season ==&gt; summer emotion ==&gt; excited team-name ==&gt; USA adjective ==&gt; nice

Here is your Mad Lib…

Hello Alex,

Good morning! Are you looking forward to a/an interesting semester?

You will write a lot of code and feel proud when you do. If you do not, you will struggle this semester.

Did you watch the Olympics this summer?

Were you excited when the USA won? Have a/an nice day!

We’ve provided reasonable inputs, but the idea of MadLibs is to input random words and see how silly the result looks. Try it!

Of course, the program you write will only work for the specific MadLib we’ve written above. A more challenging problem, which you will be capable of solving by the end of the semester, is to write a program that reads in <strong>any </strong>MadLib, figures out what to ask the user, asks the user, reads the input, and generates the final MadLib.

When you have tested your code and you are sure that it works, please submit it as the solution to Part 3 of the homework.