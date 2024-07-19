---
layout: lesson
title: VECTORS AND THEIR GEOMETRY
course: calculus-III
unit: unit1
lessonID: vectors-and-geometry
nextID: algebraic-operations-vectors
---
In high school, we learned that a vector is a quantity with magnitude and direction. Here, we will present a more abstract notion of vectors, that we will be able to generalize in order to solve more complex problems. Physical examples of vectors that you have learned about before could be: *position*, *momentum*, or maybe *electric field*. These can be constrasted with scalars, which are just numbers. For example, *temperature*, *pressure*, or *altitude*. 

In the previous lesson, we talked about points in three dimensional space. Now we will discuss the concept of direction in space. A *vector* in three dimensional space is an ordered triplet \\(\textbf{v} = (a,b,c)\\), where \\(a,b,c\\) are each real numbers. This is represented visually by drawing an arrow from the origin to the point \\((a,b,c)\\). The numbers \\(a,b,c\\) are known as the *components* of the vector, where \\(a\\) is the \\(x\\) component, \\(b\\) the \\(y\\) component, and \\(c\\) the \\(z\\) component. Just as important are vector in two dimensional space, written as \\((a,b)\\). 

It is often useful to translate the vector around in space, while keeping all of its components the same. This means that the vector's starting point and ending point will both change, but that the difference of the two stay the same. Thus the two vectors in the following figure are actually the same vector, even though they begin at different points. 

insert figure

In this course, vectors will always be denoted by boldface letters, for example, \\(\textbf{v} = (a,b,c)\\). If written by hand, this is most often done as \\( \vec{v} = (a,b,c)\\). In more advanced mathematics, this special notation is often dropped altogether, writing \\(v = (a,b,c)\\). We will not be writing vectors in such a way in this course. Now let's discuss operations with vectors from a geometric standpoint. 

#### Scalar Multiplication
Vectors can be multiplied by scalars, and this changes the vector's length but not its direction. Actually, the direction can be changed, but only to point in the opposite direction. This is done by multiplying by a negative number. Let's show graphically how multiplying vectors by scalars works: 

(insert figure here)


#### Addition 
Vectors can be geometrically added *tip to tail* by drawing the tip of one on top of the tail of the other. For example, in two dimensions, 

(insert figure here)

The same aproach works in three dimensions, although it may be harder to draw. 


#### Subtraction
In order to subtract vectors geometrically, we need to introduce the *negative* of a vector. The negative of a vector has the same magnitude but the exact opposite direction. The negative of a vector is obtained by multiplying it by \\(-1\\). Then, the negative of the vector is added to the original. For example, 

(insert figure here)

#### The Cartesian Basis

The three numbers \\(a,b,c\\), defined before as the *components* of the vector, allow us to write *decompose* vector in terms of a basis. For this, we write 

$$\textbf{v} = (a,b,c) = a\hat{\textbf{i}} + b\hat{\textbf{j}} + c\hat{\textbf{k}}$$

where we call \\(\hat{\textbf{i}},\hat{\textbf{j}},\hat{\textbf{k}}\\) the basis vectors in the \\(x,y,z\\) directions respectively. Geometrically, \\(\hat{\textbf{i}}\\) is the vector with length 1 pointing along the \\(x\\) axis, and similarly for the other two. 



### Exercises
<ol>
<li> <div> Given the following vectors (insert figure here), construct the following vectors: </div>
<ol type = "a">
<li> \(3\textbf{a}\)</li>
<li> \(-2\textbf{c}\)</li>
<li> \(2\textbf{a}-\textbf{b}\)</li>
<li> \(\textbf{a}+\textbf{b}-\textbf{c}\)</li>
<li> \(3\textbf{a}-2\textbf{b}+2\textbf{c}\)</li>
</ol>
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
<ol type = "a">
<li> \(3\textbf{a}\)</li>
<li> \(-2\textbf{c}\)</li>
<li> \(2\textbf{a}-\textbf{b}\)</li>
<li> \(\textbf{a}+\textbf{b}-\textbf{c}\)</li>
<li> \(3\textbf{a}-2\textbf{b}+2\textbf{c}\)</li>
</ol>
</div> </li>


</ol>


















