Download Link: https://assignmentchef.com/product/solved-cs2336-project-three-simple-integral-calculator
<br>
<strong>Objective:</strong> Use object-oriented programming to implement and utilize a binary tree

<strong>Problem:</strong> Doc Brown has gotten himself in a jam. The software he uses to evaluate integrals has become corrupt and he is in need of assistance. Without this software, his quantum physics calculations will be incorrect, possibly creating time paradox of epic proportions! Doc Brown is enlisting your assistance in the matter. Your future may depend on it.

<strong>Pseudocode:</strong> Your pseudocode should describe the following items

<ul>

 <li>Identify the functions you plan to create for each class

  <ul>

   <li>You do not have to include pseudocode for basic items like constructors, accessors, mutators</li>

  </ul></li>

 <li>For each function, identify the following

  <ul>

   <li>Determine the parameters</li>

   <li>Determine the return type</li>

   <li>Detail the step-by-step logic that the function will perform</li>

  </ul></li>

</ul>

<strong>Details:</strong>

<ul>

 <li>Start the program by prompting the user for the input filename o This would normally be hardcoded in an application, but zyLabs requires a filename for multiple test files</li>

 <li>This program will read basic integrals from a file and evaluate them.</li>

 <li>If the integral is definite, the program will create the anti-derivative and evaluate for the given interval.</li>

 <li>If the integral is indefinite, then just the anti-derivative should be created.</li>

</ul>

<strong>Classes</strong>

<ul>

 <li>Use good programming practice for classes – proper variable access, mutators and accessors, proper constructors, etc.</li>

 <li>Remember that classes exist to be used by other people. Just because you don’t use it in the program doesn’t mean it shouldn’t be coded and available for others to use in theirs.</li>

 <li>As with previous projects, you are open to design the classes as you see fit with the minimum requirements listed below</li>

 <li>All classes must be of your own design and implementation.

  <ul>

   <li><strong>Do not use the pre-defined Java classes (-20 points if pre-defined classes used)</strong></li>

  </ul></li>

 <li><strong>Requirements</strong>

  <ul>

   <li>Binary Tree class

    <ul>

     <li>Named <strong>BinTree.java</strong></li>

     <li>Root pointer</li>

     <li>Will contain functions for basic functionality of a binary tree

      <ul>

       <li>Insert</li>

       <li>Search</li>

       <li>Delete</li>

      </ul></li>

     <li>May contain other functions</li>

     <li>All traversals of the tree will be done recursively (-10 points if not)

      <ul>

       <li>This includes functions that add, delete, or search the tree</li>

      </ul></li>

     <li>The order of the nodes matters

      <ul>

       <li>A binary tree Is better than a linked list</li>

      </ul></li>

    </ul></li>

   <li>Node class

    <ul>

     <li>Named <strong>Node.java</strong></li>

     <li>Generic class (-10 points if not)</li>

     <li>Left and right pointers</li>

     <li>Payload object to hold data</li>

    </ul></li>

   <li>Payload class

    <ul>

     <li>Named <strong>Payload.java</strong></li>

     <li>Coefficient</li>

     <li>Exponent</li>

    </ul></li>

  </ul></li>

</ul>

<strong>Expressions</strong>

<ul>

 <li>Consist of simple polynomial terms – the highest degree will be 10

  <ul>

   <li>If multiple terms include the same exponent, combine those terms</li>

  </ul></li>

 <li>Exponents will be represented by the ^ character.</li>

 <li>Do not assume that the expression will be in order from highest to lowest exponent.</li>

 <li>All coefficients will be integers.</li>

 <li>The | (pipe) character will be used to represent the integral symbol</li>

 <li>If an integral is definite, there will be a number before and after the | character</li>

</ul>

<pre><code> ∫ x dx = a|b x dx The endpoints of the interval for the definite integral will be integer values</code></pre>

<ul>

 <li>The variable will always be ‘x’ and the integral will always end with dx</li>

 <li>There will always be a space before the first term of the integral and before dx o Do not assume there will be spaces anywhere else in the expression</li>

 <li>If a term has no coefficient, it is assumed to be 1</li>

 <li><strong>Example Input:</strong>

  <ul>

   <li>| 3x^2 + 2x + 1 dx</li>

   <li>1|4 x^-2 +3x+4 dx</li>

   <li>– 2|2 x^3 – 4x dx</li>

  </ul></li>

</ul>

<strong>Input:</strong> All expressions will be read from a file. There is no limit to the number of expressions that can be in the file. Each expression will be on a separate line (see examples above).

<strong>Output:</strong>

<ul>

 <li>All output will be written to the console</li>

 <li>Each anti-derivative will be displayed to a separate line

  <ul>

   <li>Definite integrals will also include the interval and value (see examples below) &#x25aa; Values will be to 3 decimal places</li>

  </ul></li>

 <li>Use the ^ character to represent exponents</li>

 <li>Order the terms from greatest to least exponent</li>

 <li>Fractions will be simplified

  <ul>

   <li>All fractions will be enclosed in parentheses</li>

  </ul></li>

 <li>A space will proceed and follow each operator (+ or -)</li>

 <li>Indefinite anti-derivative format

  <ul>

   <li>expression_space_plus_space_capital C_newline</li>

  </ul></li>

 <li>Definite anti-derivative format

  <ul>

   <li>expression_comma_space_upper bound_pipe_lower bound__space__equal__space_value_newline</li>

  </ul></li>

 <li><strong>Example Output (based on input above):</strong>

  <ul>

   <li>x^3 + x^2 + x + C</li>

   <li>(3/2)x^2 + 4x -x^-1, 1|4 = 35. 250</li>

   <li>(1/4)x^4 – 2x^2, -2|2 = 0</li>

  </ul></li>

</ul>

<strong>EXTRA CREDIT:</strong> Add to your program to allow evaluation of indefinite integrals containing trigonometric functions (potential 15 extra points)

<ul>

 <li><strong>The trig terms must be stored in the tree with all other nodes.</strong></li>

 <li>Simple expressions inside the trig functions

  <ul>

   <li>The term inside the trig function will not have an exponent</li>

  </ul></li>

 <li>The trig anti-derivatives will be listed at the end of the expression in the order encountered</li>

 <li>There will be a space between the trig function and the inner coefficient of the trig function

  <ul>

   <li>This is true for both input and output</li>

  </ul></li>

 <li><strong>Example Input:</strong>

  <ul>

   <li>| sin x + cos x dx</li>

   <li>| 1 – cos 4x dx</li>

   <li>| 3x^4 – 6x^2 + 2 sin 10x dx</li>

  </ul></li>

 <li><strong>Example Output:</strong>

  <ul>

   <li>– cos x + sin x + C</li>

   <li>x – (1/4)sin 4x + C</li>

   <li>(3/5)x^5 – 2x^3 – (1/5)cos 10x + C</li>

  </ul></li>

</ul>