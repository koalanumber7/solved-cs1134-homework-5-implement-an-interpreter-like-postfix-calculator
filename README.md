Download Link: https://assignmentchef.com/product/solved-cs1134-homework-5-implement-an-interpreter-like-postfix-calculator
<br>
<strong>Homework # 5</strong>

<strong><u>Question 1: </u></strong>

Implement an interpreter-like<strong> postfix calculator</strong>. Your program should repeatedly:

<ul>

 <li>Print a prompt to the user. The prompt should be: ‘–&gt;’</li>

 <li>Read an expression from the user</li>

 <li>Evaluate that expression</li>

 <li>Print the result</li>

</ul>

Your calculator should support 2 kinds of expressions:

1 .<strong><u> Arithmetic expressions</u></strong> – are given in postfix notation. The tokens of the expression are separated by a space.

2 .<strong><u> Assignment expressions</u></strong> – are expression of the form:

<em>variable_name </em>=<em> arithmetic_expression</em>

When evaluated, it first evaluates the<em> arithmetic_expression</em> (given in postfix notation), and then it associates that value with<em> variable_name</em> (in a data structure of your choice).

<u>Notes:</u>

<ul>

 <li>The value of an assignment expression, is the name of the variable being</li>

 <li>Assume that the<em> variable_name</em>, the ‘=’ symbol, and the <em>arithmetic_expression </em>are separated by a space.</li>

</ul>

<u>Notes:</u>

1 . Arithmetic expressions can contain variable names, for referencing to values associated with variables that were defined before.

2 . You may assume that the input the user enters, is valid. That is, the arithmetic expressions are legal; all variables used in an expression were already defined; etc.

3 . The program should keep reading, and evaluating expressions until the user types ‘done( )’.

Your program should interact with the user<strong> exactly</strong> as demonstrated in the example below:

<table>

 <tbody>

  <tr>

   <td width="35">– – &gt;4–&gt; 4–&gt;x–&gt; 4–&gt; 8–&gt;y–&gt;</td>

   <td width="39">45 1x =xx xy =y</td>

   <td width="19">–5+1</td>

   <td width="20">1x</td>

   <td width="39">–+ 3</td>

   <td width="19">4</td>

   <td width="19">*</td>

   <td width="39">– 2</td>

   <td width="349">/</td>

  </tr>

 </tbody>

</table>




<strong><u>Question 2: </u></strong>

Give a Python implementation for the <em>MaxStack </em>ADT. The <em>MaxStack </em>ADT supports the following operations:

<ul>

 <li>MaxStack (): initializes an empty MaxStack object</li>

 <li>is_empty() : returns True if maxS does not contain any elements, or False otherwise.</li>

 <li>len(maxS): Returns the number of elements in maxS</li>

 <li>maxS .push(e) : adds element e to the top of maxS.</li>

 <li>maxS .top(): returns a reference to the top element of maxS, without removing it; an exception is raised if maxS is empty.</li>

 <li>maxS .pop() : removes and return the top element from maxS; an exception is raised if maxS is empty.</li>

 <li>maxS .max() : returns the element in maxS with the largest value, without removing it; an exception is raised if maxS is empty.</li>

</ul>

<strong><u>Note</u></strong><u>:</u> Assume that the user inserts only integers to this stack (so they could be compared to one another, and a maximum data is well defined).

For example, your implementation should follow the behavior below:

&gt; &gt; &gt; maxS = MaxStack ()

&gt;&gt;&gt; maxS.push(3) &gt;&gt;&gt; maxS.push(1) &gt;&gt;&gt; maxS.push(6) &gt;&gt;&gt; maxS.push(4) &gt;&gt;&gt; maxS.max()

6

&gt;&gt;&gt; maxS.pop() 4

&gt;&gt;&gt; maxS.pop() 6

&gt;&gt;&gt; maxS.max()

3

<strong><u>Implementation Requirements</u></strong><u>:</u>

1 . For the representation of MaxStack objects, your data members should be:

<ul>

 <li>A Stack– of type ArrayStack</li>

 <li>Additional (1) space – for additional data members, if needed</li>

</ul>

2 . Your implementation should support the max operation in (1) worst-case time.

For all other Stack operation, the running time should remain as it was in the original implementation.

<strong><u>Hint</u></strong><u>:</u> You may want to store a tuple, as elements of the ArrayStack. That is, to attach to every “real” data in this stack some additional information.




<strong><u>Question 3: </u></strong>

Give a Python implementation for the <em>MidStack </em>ADT. The <em>MidStack </em>ADT supports the following operations:

<ul>

 <li>MidStack (): initializes an empty MidStack object</li>

 <li>is_empty() : returns True if S does not contain any elements, or False otherwise.</li>

 <li>len(midS): Returns the number of elements m i d S</li>

 <li>push(e) : adds element e to the top of m i d S .</li>

 <li>top(): returns a reference to the top element of midS, without removing it; an exception is raised if S is empty.</li>

 <li>pop() : removes and returns the top element from m i d S ; an exception is raised if midS is empty.</li>

 <li>mid_push (e): adds element e in the middle of m i d S .</li>

</ul>

That is, assuming there are <em>n </em>elements in S: In the case <em>n </em>is even, e would go exactly in the middle. If n is odd, e will go after the <u>~~1 </u>

~<em>th </em>element.

For example, your implementation should follow the behavior as demonstrated in the two execution examples below:

&gt; &gt; &gt; midS = MidStack()

&gt;&gt;&gt; midS.push(2) &gt;&gt;&gt; midS.push(4) &gt;&gt;&gt; midS.push(6) &gt;&gt;&gt; midS.push(8) &gt;&gt;&gt; midS.mid_push(10)

&gt;&gt;&gt; midS.pop() 8

&gt;&gt;&gt; midS.pop() 6

&gt;&gt;&gt; midS.pop() 10

&gt;&gt;&gt; midS.pop() 4

&gt;&gt;&gt; midS.pop() 2




<strong><u>Implementation Requirements</u></strong><u>:</u>

1 . For the representation of MidStack objects, your data members should be:

<ul>

 <li>A Stack – of type ArrayStack</li>

 <li>A double ended queue – of type ArrayDeque</li>

 <li>Additional (1) space – for additional data members, if needed</li>

</ul>

2 . Your implementation should support the mid_push operation in ( 1)

amortized time. For all other Stack operation, the running time should remain as

<table>

 <tbody>

  <tr>

   <td width="23">

    <table width="100%">

     <tbody>

      <tr>

       <td></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

it was in the original implementation (That is,  1 amortized for push and pop,

and ( 1) worst-case for top, len and is_empty).

<strong><u>Question 4: </u></strong>

Give an alternative implementation for the <em>Queue </em>ADT.

<strong><u>Implementation Requirements</u></strong><u>:</u>

1 . For the representation of Queue objects, your data members should be:

<ul>

 <li><strong>Two </strong>Stacks – of type ArrayStack</li>

 <li>Additional (1) space – for additional data members, if needed</li>

</ul>

2 . Any sequence of <em>n </em>enqueue and dequeue operations (starting with an empty

queue) should run in worst-case of () altogether.

<strong><u>Question 5: </u></strong>

Implement the following function: <strong>de f </strong>permutations (lst)

The function is given a list lst of integers, and returns a list containing all the different permutations of the elements in lst. Each such permutation should be represented as a list.

For example, if lst= [1, 2, 3], the call permutations(lst) could return

[[1, 2, 3],   [2, 1, 3], [1, 3, 2], [3, 2, 1], [3, 1, 2], [2, 3, 1 ] ]

<strong><u>Implementation Requirements</u></strong><u>:</u>

1 . Your implementation should be <strong>non-recursive</strong>.

2 . Your implementation is allowed to use a Stack, a Queue, and (1) additional

space.

<strong><u>Hint:</u></strong> Use the stack to store the elements yet to be used to generate the permutations, and use the queue to store the (partial) collection of permutations generated s o far.