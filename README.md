Download Link: https://assignmentchef.com/product/solved-csc421-2516-homework-3
<br>
<strong>Submission: </strong>You must submit your solutions as a PDF through MarkUs. You can produce the file however you like (e.g. LaTeX, Microsoft Word, scanner) as long as it is readable.

<strong>Late Submission: </strong>MarkUs will remain open until 3 days after the deadline, after which no late submissions will be accepted. The late penalty is 10% per day, rounded up.

Weekly homeworks are individual work. See the Course Information handout<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> for detailed policies.

<ol>

 <li><strong> [5pts] </strong>For this question, you may wish to review the properties of expectation and variance: <a href="https://metacademy.org/graphs/concepts/expectation_and_variance">https://metacademy.org/graphs/concepts/expectation_and_variance</a></li>

</ol>

Dropout has an interesting interpretation in the case of linear regression. Recall that the predictions are made stochastically as:

<em>y </em>= X<em>m</em><em>jw</em><em>jx</em><em>j,</em>

<em>j</em>

where the <em>m<sub>j</sub></em>’s are all i.i.d. (independnet and identically distributed) Bernoulli random variables with expectation 1/2. (I.e., they are indepdendent for every input dimension and every data point.) We would like to minimize the cost

<em>,                                                               </em>(1)

where the expectation is with respect to the’s.

Now we show that this is equivalent to a regularized linear regression problem:

(a) <strong>[2pts] </strong>Find expressions for E[<em>y</em>] and Var[<em>y</em>] for a given <strong>x </strong>and <strong>w</strong>. (b) <strong>[1pt] </strong>Determine ˜<em>w<sub>j </sub></em>as a function of <em>w<sub>j </sub></em>such that

E[<em>y</em>] = <em>y</em>˜ = <sup>X</sup><em>w</em>˜<em><sub>j</sub>x<sub>j</sub>.</em>

<em>j</em>

Here, ˜<em>y </em>can be thought of as (deterministic) predictions made by a different model.

(c) <strong>[2pts] </strong>Using the model from the previous section, show that the cost J (Eqn. 1) can be written as

<em>,</em>

where R is a function of the ˜<em>w<sub>D</sub></em>’s which does not involve an expectation. I.e., give an expression for R. (Note that R will depend on the data, so we call it a “data-dependent regularizer.”)

<em>Hint: write the cost in terms of the mean and variance formulas from part (a). For inspiration, you may wish to refer to the derivation of the bias/variance decomposition from the Lecture 12 course notes.</em>

1

CSC421/2516 Winter 2019                                                                                                                            Homework 3

<ol start="2">

 <li><strong>Binary Addition [5pts] </strong>In this problem, you will implement a recurrent neural network which implements binary addition. The inputs are given as binary sequences, starting with the <em>least </em>significant binary digit. (It is easier to start from the least significant bit, just like how you did addition in grade school.) The sequences will be padded with at least one zero on the end. For instance, the problem</li>

</ol>

100111 + 110010 = 1011001

would be represented as:

<ul>

 <li><strong>Input 1: </strong>1, 1, 1, 0, 0, 1, 0</li>

 <li><strong>Input 2: </strong>0, 1, 0, 0, 1, 1, 0</li>

 <li><strong>Correct output: </strong>1, 0, 0, 1, 1, 0, 1</li>

</ul>

There are two input units corresponding to the two inputs, and one output unit. Therefore, the pattern of inputs and outputs for this example would be:

Design the weights and biases for an RNN which has two input units, three hidden units, and one output unit, which implements binary addition. All of the units use the hard threshold activation function. In particular, specify weight matrices <strong>U</strong>, <strong>V</strong>, and <strong>W</strong>, bias vector <strong>b<sub>h</sub></strong>, and scalar bias <em>b<sub>y </sub></em>for the following architecture:

<em>Hint: </em>In the grade school algorithm, you add up the values in each column, including the carry. Have one of your hidden units activate if the sum is at least 1, the second one if it is at least 2, and the third one if it is 3.

2

<a href="#_ftnref1" name="_ftn1">[1]</a> <a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">http://www.cs.toronto.edu/</a><a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">~</a><a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">rgrosse/courses/csc421_2019/syllabus.pdf</a>