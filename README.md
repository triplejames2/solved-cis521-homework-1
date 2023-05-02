Download Link: https://assignmentchef.com/product/solved-cis521-homework-1
<br>
Instructions

In this assignment, you will answer some conceptual questions about Python and write a collection of basic algorithms and data structures.

A skeleton file homework1. py containing empty definitions for each question has been provided. Since portions of this assignment will be graded automatically, none of the names or function signatures in this file should be modified. However, you are free to introduce additional variables or functions if needed.

Unless explicitly stated otherwise, you may not import any of the standard Python modules, meaning your solutions should not include any lines of the form import x or

from x import y. Accordingly, you may find it helpful to refresh yourself on Python’s built-in <u>functions</u> and<u> data types.</u>

You will find that in addition to a problem specification, each programming question also includes a pair of examples from the Python interpreter. These are meant to illustrate typical use cases, and should not be taken as comprehensive test suites.

You are strongly encouraged to follow the Python style guidelines set forth in<u> PEP 8,</u> which was written in part by the creator of Python. However, your code will not be graded for style.

Once you have completed the assignment, you should submit your file on Eniac using the following turnin command, where the flags – c and -p stand for “course” and “project”, respectively.

turnin -c cis521 -p hw1 homeworkl.py

You may submit as many times as you would like before the deadline, but only the last submission will be saved. To view a detailed listing of the contents of your most recent submission, you can use the following command, where the flag -v stands for “verbose”.

turnin -c cis521 -p hw1 -v

<ol>

 <li>Python Concepts [6 points]</li>

</ol>

For each of the following questions, write your answers as triply-quoted strings using the indicated variables in the provided file.

<ol>

 <li>[2 points] Explain what it means for Python to be both strongly and dynamically typed, and give a concrete example of each.</li>

 <li>[2 points] You would like to create a dictionary that maps some 2-dimensional points</li>

</ol>




to their associated names. As a first attempt, you write the following code:

points_to_names = {[O, 0]: “home”, [1, 2]: “school”, [-1, 1]: ‘marker}

However, this results in a type error. Describe what the problem is, and propose a solution.

<ol start="3">

 <li>[2 points] Consider the following two functions, each of which concatenates a list of strings.</li>

</ol>

<table>

 <tbody>

  <tr>

   <td width="310">def concatenatel(strings result =s  strings:result += sreturn result</td>

   <td width="394">def concatenate2(strings return “”.join(strings</td>

  </tr>

 </tbody>

</table>




One of these approaches is significantly faster than the other for large inputs. Which version is better, and what is the reason for the discrepancy?

<ol start="2">

 <li>Working with Lists [15 points]</li>

 <li>[5 points] Consider the function extract_and_apply(1, p, -F) shown below, which extracts the elements of a list 1 satisfying a boolean predicate p, applies a function -F to each such element, and returns the result.</li>

</ol>

def extract_and_apply(1, p, f):

result = []for x in 1:

if p(x):

result append(f(x))

return result

Rewrite extract_and_apply(1, p f in one line using a list comprehension.

<ol start="2">

 <li>[5 points] Write a function concatenate seqs that returns a list containing the concatenation of the elements of the input sequences. Your implementation should consist of a single list comprehension, and should not exceed one line.</li>

</ol>

&gt;&gt;&gt; concatenate([[1, 2], [3, 4]])              &gt;&gt;&gt; concatenate([“abc”, (0, [0])])

[1, 2, 3, 4]                                    I                     , 0, [0] ]

<ol start="3">

 <li>[5 points] Write a function transpose matrix that returns the transpose of the input matrix, which is represented as a list of lists. Recall that the transpose of a matrix is obtained by swapping its rows with its columns. More concretely, the equality matrix[i][j] == transpose matrix) [j ] [i] should hold for all valid indices i and j. You may assume that the input matrix is well-formed, i.e., that each row is of equal You may further assume that the input matrix is non-empty. Your function</li>

</ol>




should not modify the input.

&gt;&gt;&gt; transpose([[1, 2, 3]])                      &gt;&gt;&gt; transpose([[1, 2], [3, 4], [5, 6]])

[[<sup>1</sup>], [<sup>2</sup>], [<sup>3</sup>]]                                 [[1, 3, 5], [2, 4, 6]]

<ol start="3">

 <li>Sequence Slicing [6 points]</li>

</ol>

The functions in this section should be implemented using sequence slices. Recall that the slice parameters take on sensible default values when omitted. In some cases, it may be necessary to use the optional third parameter to specify a step size.

<ol>

 <li>[2 points] Write a function copy seq that returns a new sequence containing the same elements as the input sequence.</li>

</ol>




<table>

 <tbody>

  <tr>

   <td width="710">

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

<table>

 <tbody>

  <tr>

   <td width="209">

    <table width="100%">

     <tbody>

      <tr>

       <td>&gt;&gt;&gt; copy(“abc”)‘abc’&gt;&gt;&gt; copy((1, 2, 3)) (1, 2, 3)</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="312">

    <table width="100%">

     <tbody>

      <tr>

       <td>

        <table>

         <tbody>

          <tr>

           <td width="29">[0,</td>

           <td width="23">0,</td>

           <td width="23">0]</td>

           <td width="29">[0,</td>

           <td width="22">0,</td>

           <td width="182">0]</td>

          </tr>

          <tr>

           <td width="29">[1,</td>

           <td width="23">0,</td>

           <td width="23">0]</td>

           <td width="29">[0,</td>

           <td width="22">0,</td>

           <td width="182">0]</td>

          </tr>

         </tbody>

        </table> </td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="307">

    <table width="100%">

     <tbody>

      <tr>

       <td>&gt;&gt;&gt; x = [0, 0, 0]; y = copy(x)&gt;&gt;&gt; print x, y; x[0] = 1; print x, y</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>




<ol start="2">

 <li>[2 points] Write a function all_but_last ( seq’ that returns a new sequence containing all but the last element of the input sequence. If the input sequence is empty, a new empty sequence of the same type should be returned.</li>

</ol>

&gt;&gt;&gt; all_but_last(“abc”)                        &gt;&gt;&gt; all_but_last(“”)

&gt;&gt;&gt; all_but_last((1, 2, 3))                    &gt;&gt;&gt; all_but_last(H)

(1, 2)                                         []

<ol start="3">

 <li>[2 points] Write a function every_other seq that returns a new sequence containing every other element of the input sequence, starting with the first. <em>Hint: This function </em><em>can be written in one line using the optional third parameter of the slice notation.</em></li>

</ol>

&gt;&gt;&gt; every_other([1, 2, 3, 4, 5])               &gt;&gt;&gt; every_other([1, 2, 3, 4, 5, 6])

[<sup>1</sup>, <sup>3</sup>, <sup>5</sup>]                                         [<sup>1</sup>, <sup>3,</sup><sup> 5</sup>]

&gt;&gt;&gt; every_other(“abcde”)                       &gt;&gt;&gt; every_other(“abcdef”)

<ol start="4">

 <li>Combinatorial Algorithms [11 points]</li>

</ol>

The functions in this section should be implemented as generators. You may generate the output in any order you find convenient, as long as the correct elements are produced. However, in some cases, you may find that the order of the example output hints at a possible implementation.




of their more sophisticated features here. Simply keep in mind that where you mightnormally return a list of elements, you should instead yield the individual elements.

Since the contents of a generator cannot be viewed without employing some form of iteration, we wrap all function calls in this section’s examples with the list function for convenience.

<ol>

 <li>[6 points] The prefixes of a sequence include the empty sequence, the first element, the first two elements, etc., up to and including the full sequence itself. Similarly, the suffixes of a sequence include the empty sequence, the last element, the last two</li>

</ol>

elements, etc., up to and including the full sequence itself. Write a pair of functions prefixes seq and suffixes seq that yield all prefixes and suffixes of the input sequence.




<table>

 <tbody>

  <tr>

   <td colspan="2" width="220">&gt;&gt;&gt; list(prefixes([1,</td>

   <td width="23">2,</td>

   <td width="46">3]))</td>

  </tr>

  <tr>

   <td width="93">[[],</td>

   <td width="127">[<sup>1</sup>],    [<sup>1</sup>,    <sup>2</sup>],    [<sup>1</sup>,</td>

   <td width="23"><sup>2</sup>,</td>

   <td width="46"><sup>3</sup>]]</td>

  </tr>

  <tr>

   <td colspan="2" width="220">&gt;&gt;&gt; list(suffixes([1,</td>

   <td width="23">2,</td>

   <td width="46">3]))</td>

  </tr>

  <tr>

   <td width="93">[[<sup>1</sup>,</td>

   <td colspan="2" width="150"><sup>2</sup>,    <sup>3</sup>],   [<sup>2</sup>,     <sup>3</sup>],    [<sup>3</sup>],</td>

   <td width="46">[]]</td>

  </tr>

  <tr>

   <td width="93"></td>

   <td width="127"></td>

   <td width="23"></td>

   <td width="46"></td>

  </tr>

 </tbody>

</table>







<ol start="2">

 <li>[5 points] Write a function slices seq that yields all non-empty slices of the input sequence.</li>

</ol>

&gt;&gt;&gt; list(slices([1, 2, 3]))                  &gt;&gt;&gt; list(slices(“abc”))

[[1], [1, 2], [1, 2, 3], [2], [2, 3],          I      , ‘ab’, ‘abc’, ‘b’, ‘bc’,

[<sup>3</sup>]]

<ol start="5">

 <li>Text Processing [2o points]</li>

 <li>[5 points] A common preprocessing step in many natural language processing tasks is text normalization, wherein words are converted to lowercase, extraneous whitespace is removed, etc. Write a function normalize text that returns a normalized version of the input string, in which all words have been converted to lowercase and are separated by a single space. No leading or trailing whitespace should be present in the output.</li>

</ol>

„. normalize(“This is an example.”)          &gt;&gt;&gt; normalize(”    EXTRA SPAC

‘this is an example.’                          ‘extra .pace’

<ol start="2">

 <li>[5 points] Write a function no_vowels text that removes all vowels from the input string and returns the result. For the purposes of this problem, the letter ‘y’ is not considered to be a vowel.</li>

</ol>

&gt;&gt;&gt; no_vowels(“This Is An Example.”)          &gt;&gt;&gt; no_vowels(“We love Python!”)

‘Ths    , xmpl.’                               ‘W Iv Pythn!’




which they are each separated by a single space. If the input string contains no digits, then an empty string should be returned.




&gt;&gt;&gt; digits_to_words(“Zip Code: 19104”) line one zero four’

&gt;&gt;&gt; digits_to_words(“Pi is 3.1415…’) ‘three one four one five’




<ol start="4">

 <li>[5 points] Although there exist many naming conventions in computer programming,</li>

</ol>

two of them are particularly widespread. In the first, words in a variable name are separated using underscores. In the second, words in a variable name are written in mixed case, and are strung together without a delimiter. By mixed case, we mean that the first word is written in lowercase, and that subsequent words have a capital first letter. Write a function to_mixed_case name that converts a variable name from the former convention to the latter. Leading and trailing underscores should be ignored. If

the variable name consists solely of underscores, then an empty string should be returned.

&gt;&gt;&gt; to_mixed_case(“to_mixed_case”)             &gt;&gt;&gt; to_mixed_case(” EXAMPLE NAME “)

‘toMixedCa.,                              ‘exampleName

<ol start="6">

 <li>Polynomials [37 points]</li>

</ol>

In this section, you will implement a simple Polynomial class supporting basic arithmetic, simplification, evaluation, and pretty-printing. An example demonstrating these capabilities is shown below.

&gt;&gt;&gt; p, q = Polynomial([(2, 1), (1, 0)]), Polynomial([(2, 1), (-1, 0)])

&gt;&gt;&gt; print p; print q

2x + 1 2x – 1 &gt;&gt;&gt; r = (p * p) + (q * q) – (p * q); print r

4xA2 + 2x + 2x + 1 + 4x^2 – 2x – 2x + 1 – 4x^2 + 2x – 2x + 1

&gt;&gt;&gt; r.simplify(); print r

4xA2 + 3

&gt;&gt;&gt; [(x, r(x)) for x in range(-4, 5)]

[(-4, 67), (-3, 39), (-2, 19), (-1, 7), (0, 3), (1, 7), (2, 19), (3, 39), (4, 67)]

<ol>

 <li>[2 points] In this problem, we will think of a polynomial as an immutable object, represented internally as a tuple of coefficient-power pairs. For instance, the polynomial 2x + 1 would be represented internally by the tuple ( (2, 1) , (1, 0) ) . Write an initialization method _init_ self polynomial that converts the input sequence polynomial of coefficient-power pairs into a tuple and saves it for future use. Also write a corresponding method get_polynomial self that returns this internal representation.</li>

</ol>

&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])          &gt;&gt;&gt; p = Polynomial(((2, 1), (1, 0)))

&gt;&gt;&gt; p get_polynomial()                              &gt;&gt;&gt; p.get_polynomial()




((2, 1), (1, 0))                               ((2, 1), (1, 0))

<ol start="2">

 <li>[4 points] Write a _neg_( self method that returns a new polynomial equal to the negation of This method will be used by Python for unary negation.</li>

</ol>

&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])          &gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])

&gt;&gt;&gt; q = -p; q.get_polynomial()                 &gt;&gt;&gt; q = -(-p); q get_polynomial()

((-2, 1), (-1, 0))                             ((2, 1), (1, 0))

<ol start="3">

 <li>[3 points] Write an _add_ self other method that returns a new polynomial equal to the sum of self and other . This method will be used by Python for addition. No simplification should be performed on the result.</li>

</ol>

&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])          &gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])

&gt;&gt;&gt; q = p + p; q.get_polynomial()            &gt;&gt;&gt; q = Polynomial([(4, 3), (3, 2)])

((2, 1), (1, 0), (2, 1), (1, 0))               &gt;&gt;&gt; r = p + q; r.get_polynomial()

((2, 1), (1, 0), (4, 3), (3, 2))

<ol start="4">

 <li>[3 points] Write a _sub_ self other method that returns a new polynomial equal to the difference between self and other . This method will be used by Python for subtraction. No simplification should be performed on the result.</li>

</ol>

&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])          &gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])

&gt;&gt;&gt; q = p – p; q.get_polynomial()            &gt;&gt;&gt; q = Polynomial([(4, 3), (3, 2)])

((2, 1), (1, 0), (-2, 1), (-1, 0))            &gt;&gt;&gt; r = p – q; r.get_polynomial()

((2, 1), (1, 0), (-4, 3), (-3, 2))

<ol start="5">

 <li>[5 points] Write a mul self other method that returns a new polynomial equal to the product of self and other . This method will be used by Python for No simplification should be performed on the result. Your result does not need to match the examples below exactly, as long as the same terms are present in some order.</li>

</ol>

&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])          &gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])

&gt;&gt;&gt; q = p * p; q.get_polynomial()              &gt;&gt;&gt; q = Polynomial([(4, 3), (3, 2)])

((4, 2), (2, 1), (2, 1), (1, 0))              &gt;&gt;&gt; r = p * q; r.get_polynomial()

((8, 4), (6, 3), (4, 3), (3, 2))

<ol start="6">

 <li>[3 points] Write a call self, x) method that returns the result of evaluating the current polynomial at the point x. This method will be used by Python when a polynomial is called as a function. <em>Hint: This method can be written in one line using </em><em>Python’s exponentiation operator,</em><em> **</em><em> , and the built-in sum function.</em></li>

</ol>




&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])           &gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])

&gt;&gt;&gt; [p(x) for x in range(5)]                    &gt;)&gt; q = -OD * P, + P

[1, 3, 5, 7, 9                                 &gt;&gt;&gt; [q(x) for x 1.. range(5)]

[0, -6, -20, -42, -72]

<ol start="7">

 <li>[8 points] Write a simplify self method that replaces the polynomial’s internal representation with an equivalent, simplified representation. Unlike the previous methods, simplify self does not return a new polynomial, but rather acts in place. However, because the fundamental character of the polynomial is not changing, we do not consider this to violate the notion that polynomials are immutable.</li>

</ol>

The simplification process should begin by combining terms with a common power. Then, terms with a coefficient of zero should be removed, and the remaining terms should be sorted in decreasing order based on their power. In the event that all terms have a coefficient of zero after the first step, the polynomial should be simplified to the single term 0 • x<sup>°</sup>, i.e. 0, 0 .

<table>

 <tbody>

  <tr>

   <td width="348">&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)])&gt;&gt;&gt; q = -p + (p * p); q.get_polynomial()((-2, 1), (-1, 0), (4, 2), (2, 1),(2, 1), (1, 0))&gt;&gt;&gt; q.simplify(); q.get_polynomial((4, 2), (2, 1))</td>

   <td width="333">&gt;&gt;&gt; p = Polynomial([(2, 1), (1, 0)]) &gt;&gt;&gt; q = p – p; q.get_polynomial()((2, 1), (1, 0), (-2, 1), (-1, 0)) &gt;&gt;&gt; q.simplify(); q.get_polynomial() ((0, 0),)</td>

  </tr>

 </tbody>

</table>




<ol start="8">

 <li>[9 points] Write a _str_ self method that returns a human-readable string representing the polynomial. This method will be used by Python when the st r function is called on a polynomial, or when a polynomial is printed.</li>

</ol>

In general, your function should render polynomials as a sequence of signs and terms

each separated by a single space, i.e. usigni term1 sign2 term2               signN termN”,

where signs can be “+” or        , and terms have the form “ax^b” for coefficient a and

power b. However, in adherence with conventional mathematical notation, there are a few exceptional cases that require special treatment:

<ul>

 <li>The first sign should not be separated from the first term by a space, and should be left blank if the first term has a positive coefficient.</li>

 <li>The variable and power portions of a term should be omitted if the power is 0, leaving only the coefficient.</li>

 <li>The power portion of a term should be omitted if the power is 1.</li>

 <li>Coefficients with magnitude 0 should always have a positive sign.</li>

 <li>Coefficients with magnitude 1 should be omitted, unless the power is 0.</li>

</ul>

You may assume that all polynomials have integer coefficients and non-negative integer powers.




<table>

 <tbody>

  <tr>

   <td width="360">&gt;&gt;&gt; p = Polynomial([(1, 1), (1, 0)]) &gt;&gt;&gt; qs = (p, p + p, -p, -p – p, p * p) &gt;&gt;&gt;    q in qs: q.simplify(); str(q)• • •‘x + 1’ ‘2x + 2’‘-x – 1’ ‘-2x – 2’ ‘xA2 + 2x + 1’</td>

   <td width="341">&gt;&gt;&gt; p = Polynomial([(0, 1), (2, 3)]) &gt;&gt;&gt; str(p); str(p * p); str(-p * p)‘Ox + 2xA3’‘OxA2 + OxA4 + OxA4 + 4xA6’ ‘OxA2 + OxA4 + OxA4 – 4xA6’ &gt;&gt;&gt; q = Polynomial([(1, 1), (2, 3)])&gt;&gt;&gt; str(q); str q * q); str(-q * q)‘x + 2xA3’‘xA2 + 2xA4 + 2xA4 + 4xA6’ ‘-xA2 – 2xA4 – 2xA4 – 4xA6’</td>

  </tr>

 </tbody>

</table>




<ol start="7">

 <li>Feedback [5 points]</li>

 <li>[1. point] Approximately how long did you spend on this assignment?</li>

 <li>[2 points] Which aspects of this assignment did you find most challenging? Were there any significant stumbling blocks?</li>

 <li>[2 points] Which aspects of this assignment did you like? Is there anything you would have changed?</li>

</ol>