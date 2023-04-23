Download Link: https://assignmentchef.com/product/solved-ads-assignment-2-word-ladders
<br>
Finding the shortest path between two places is a quite common task. It might be the solution to finding a GPS-route or a tool to see how related different subjects are<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. Therefore efficient algorithms for this task is of course quite crucial.

<h1>Aims</h1>

The goals of the lab are:

<ul>

 <li>Implementing BFS.</li>

 <li>Debugging your code.</li>

 <li>Structuring your code in a logical fashion.</li>

 <li>Reason about correctness of your algorithm.</li>

 <li>Reason about upper bounds for time complexity.</li>

</ul>

<h1>Problem formulation</h1>

We construct a graph where each node represents a five-letter word (the words are not necessarily in the English dictionary, but consist only of lowercase English letters, a–z). Furthermore we draw an (directed) arc from <em>u </em>to <em>v </em>if all of the last four letters in <em>u </em>are present in <em>v </em>(if there is more than one of a specific letter among the last four letters in <em>u</em>, then at least the same number has to be present in <em>v </em>in order for us to draw the edge). For example there is an edge from ”hello” to ”lolem” but not the other way around. There is both an edge from ”there” to ”where” and the other way around. There is not an edge from ”there” to ”retch” since ”e” is only present once in ”retch”.

You will be asked to answer a series of queries. For each query you will be given two words, the ”starting”-word and the ”ending”-word. The task is to find the length of the shortest path from the ”starting” to the ”ending” word for each query.

<h1>Input</h1>

The first row of the input consists two integers <em>N,Q</em>, 1 ≤ <em>N </em>≤ 5 · 10<sup>3 </sup>and 1 ≤ <em>Q </em>≤ 5 · 10<sup>3</sup>, the number of words we consider and the number of queries. Then follows <em>N </em>lines containing one five-letter word each. After this <em>Q </em>lines follow containing two space-separated five-letter words each. For each of these lines answer the query.

<h1>Output</h1>

For each query output a single line with the answer. If there exists a path from the ”starting” to the ”ending” word, print the length of the shortest path. Otherwise print ”Impossible”. Note that you have to write exactly ”Impossible” to get the verdict ”Correct” of the checker.

<h1>Examination and Points of Discussion</h1>

To pass the lab make sure you have:

<ul>

 <li>Have successfully implemented the algorithm with the correct time complexity.</li>

 <li>Have neat and understandable code.</li>

 <li>Have descriptive variable names.</li>

 <li>Have filled in the blanks in the report.</li>

 <li>Have run the check_solution script to validate your solution.</li>

</ul>

During the oral presentation you will discuss the follwoing questions with the lab assistant:

<ul>

 <li>How do you represent the problem as a graph, and how is the graph built?</li>

 <li>If one were to perform backtracking (find the path along which we went), how would that be done?</li>

 <li>What is the time complexity, and more importantly why?</li>

 <li>Is it possible to solve the problem with DFS: why or why not?</li>

 <li>Can you think of any applications of this? Of BFS/DFS in general?</li>

</ul>

<strong>Sample Input 1                                                                                 Sample Output 1</strong>

<table width="622">

 <tbody>

  <tr>

   <td width="311">5 3there where input putin hello there where putin input hello putin</td>

   <td width="311">11Impossible</td>

  </tr>

 </tbody>

</table>




<a href="#_ftnref1" name="_ftn1">[1]</a> https://en.wikipedia.org/wiki/Six_degrees_of_separation