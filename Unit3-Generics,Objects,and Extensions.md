<h1>Introduction</h1>
This codelab exposes you to several Kotlin concepts that help you structure larger apps:
<li>1. Generics</li>
<li>2. Different kinds of classes (enum classes and data classes)</li>
<li>3. Singleton and companion objects</li>
<li>4. Extension properties and functions</li>
<li>5. Scope Functions</li>

<h2>What you'll learn</h2>
<li>How to define a generic type parameter for a class.</li>
<li>How to instantiate a generic class.</li>
<li>When to use enum and data classes.</li>
<li>How to define a generic type parameter that must implement an interface.</li>
<li>How to use scope functions to access class properties and methods.</li>
<li>How to define singleton objects and companion objects for a class.</li>
<li>How to extend existing classes with new properties and methods.</li>

---

<h2>Make a reasonable class with generics.</h2>
<ul>
  <p>Let's say you are planning a Quizz App which invoves following Questions.</p>
  <li>Fill-in-the-blank question: The answer is a word represented by a <code>String</code>.</li>
  <li>True or false question: The answer is represented by a <code>Boolean</code>.</li>
  <li>Math problems: The answer is a numeric value. The answer for a simple arithmetic problem is represented by an <code>Int</code>.</li>
  <p>In Addition, Quizz question will also have difficulty rating like in String as 'easy','medium','hard'.</p>
  <strong>Now,Define classes to represent each type of quiz question:</strong>
     

</ul>

