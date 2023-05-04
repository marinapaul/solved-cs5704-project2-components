Download Link: https://assignmentchef.com/product/solved-cs5704-project2-components
<br>



<strong>Create a bounded Pipe component (also called a Deque) consistent with the following class diagram.</strong>

<strong><u>Pipe Component Diagram</u></strong>

<strong><u>(</u></strong><a href="https://drive.google.com/file/d/1J0435TeLDOCRSXueZ23mF"><strong>https://drive.google.com/file/d/1J0435TeLDOCRSXueZ23mF</strong></a><strong><u> xAnVFcVwY10/view?usp=sharing)</u></strong>

<strong>Please ensure:</strong>

<ul>

 <li><strong>All methods in CircArrayPipe should run in linear time (no loops)</strong></li>

 <li><strong>The append method in AbstractPipe should be implemented as a recursive method (no loops and it </strong><strong>should call itself)</strong></li>

 <li><strong>The package name for all classes should be “boundedpipe”</strong></li>

 <li><strong>For other requirements, see grading section (what grader will check) below</strong></li>

</ul>

<strong>The recordings on a bounded stack component should help a great deal, especially with the list-based </strong><strong>pipe implementation. The array-based pipe implementation, however, is significantly more complicated than the array-based stack implementation. To get an idea of how a circular-array pipe should work see </strong><strong>this</strong><strong><u> set of slides j</u></strong><a href="https://drive.google.com/file/d/16t417PxAb-1atboZ1R4atW"><strong>https://drive.google.com/file/d/16t417PxAb-1atboZ1R4atW</strong></a> <strong><u>5acl1 QRDn/view?  </u></strong><strong><u>usp=sharing)</u></strong><strong> . </strong><strong>A pipe is similar to a queue. In fact another name for a pipe data structure is a deque. A </strong><strong>pointer-stack implementation will be covered in a later Q&amp;A and should help with the linked-pipe.</strong>

<strong><u>Bounded Stack Component Recordings</u></strong>

<strong>The bounded pipe interface should be named</strong><strong> Pipe</strong><strong> and it should have the following methods:</strong>

<strong>void prepend(E element);</strong>

<strong>void append(E element);</strong>

<strong>E removeFirst(); </strong><strong>E removeLast(); </strong><strong>int length(); </strong><strong>int capacity();</strong>

<strong>Pipe&lt;E&gt; newInstance();</strong>

<strong>void clear(); </strong><strong>boolean isEmpty(); </strong><strong>boolean isFull();</strong>




<strong>9/28/2020                                                                                                                                                              </strong><strong>Project 2 – Components</strong>

<strong>void append(Pipe&lt;E&gt; that); Pipe&lt;E&gt; copy();</strong>

<strong>The Pipe interface should extend</strong><strong> Iterable</strong><strong> . And the pipe should not allow null values. The interface </strong><strong>should be fully documented with JavaDocs. The methods should list and document all exceptions. If any </strong><strong>argument is a null value, an illegal argument exception should be thrown. If any argument is </strong><strong>unacceptable for any reason, an illegal argument exception should be thrown. If any method is called </strong><strong>when the pipe is not in a correct state, an illegal state exception should be thrown.</strong>

<strong>The method newlnstance creates a new, empty bounded pipe with the same capacity as the calling pipe. </strong><strong>The method append that takes another pipe empties its pipe argument (that).</strong>

<strong>The complete pipe component will also have an abstract class</strong><strong> ‘AbstractPipe</strong><strong> and three concrete implementations: </strong><strong><sub>i</sub></strong><strong> ListPipe</strong><strong>1</strong><strong> ,</strong><strong> rCircArrayPipe</strong><strong> „ </strong><strong>and</strong><strong><u>  </u></strong><strong>LinkedPipe</strong><strong> . The</strong><strong> toString</strong><strong> method should look similar to </strong><strong>the one in the stack component. For example,</strong><strong> [A, B, C] : 20</strong><strong> represents a pipe with a bound of 20, where </strong><strong>A is the first element in the pipe and C is the last element in the pipe.</strong>

<strong>Write unit tests for your classes that cover all of your code. Treat the instructor as your customer: if any </strong><strong>requirements seem unclear or ambiguous, ask about them on Piazza! To assist in questions about the </strong><strong>interface methods, try to frame your question in terms of pre-state, statement, post-state. For example:</strong>

<strong>How does the removeFirst method work?</strong>

<strong>For example, what is the post-state in the following code?</strong>

<strong>[pre-state] p = [A, B, C]:20 </strong><strong>[statement] x = p.removeFirst(); </strong><strong>[post-state] x = ??? and p = ???</strong>

<strong>Submit your code to Web-CAT.</strong>

<strong>The Web-CAT portion of Project 2 is worth 40 points:</strong>

<ul>

 <li><strong>25 points from correctness and code coverage</strong></li>

 <li><strong>5 points for style</strong></li>

 <li><strong>10 points for code/implementation issues that grader will check. For example:</strong></li>

 <li><strong>Pipe interface should have complete Javadocs specifying what each method does. Include all </strong><strong>relevant annotations, such as @param, @return, *and* @throws.</strong></li>

 <li><strong>The “append” method in AbstractPipe must be recursive (no loops)</strong></li>

 <li><strong>AbstractPipe must only depend on public pipe methods. It should not use any subclasses </strong><strong>(ListPipe, CircArrayPipe or LinkedPipe)</strong></li>

 <li><strong>AbstractPipe should only import Iterator. It should not use any collection or helper classes like </strong><strong>Arrays or Collections</strong></li>

 <li><strong>The equals method should not depend on toString methods, and it should not be implemented by </strong><strong>comparing strings. Similarly, the equals method should not depend on the hashCode method</strong></li>

</ul>




9/28/2020                                                                                                        Project 2 – Components

o <strong>Concrete classes must not use Java classes beyond those listed in the diagram. For example, </strong><strong>Array implementation should not use Arrays, List, or Collections. List implementation should not </strong><strong>use Array, Arrays, or Collections. Linked implementation should not use List.</strong>

<strong>o CircArrayPipe methods must all be constant-time (no loops)</strong>

<strong>A separate related assignment (questions that require short answers) will be posted in the second or </strong><strong>third week and will be worth an additional 10 points.</strong>