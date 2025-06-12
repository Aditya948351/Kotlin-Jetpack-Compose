<h1>⭐Introduction</h1>
This codelab exposes you to several Kotlin concepts that help you structure larger apps:
<ul>
  <li>1. Generics</li>
  <li>2. Different kinds of classes (enum classes and data classes)</li>
  <li>3. Singleton and companion objects</li>
  <li>4. Extension properties and functions</li>
  <li>5. Scope Functions</li>
</ul>

<h2>What you'll learn</h2>
<ul>
  <li>How to define a generic type parameter for a class.</li>
  <li>How to instantiate a generic class.</li>
  <li>When to use enum and data classes.</li>
  <li>How to define a generic type parameter that must implement an interface.</li>
  <li>How to use scope functions to access class properties and methods.</li>
  <li>How to define singleton objects and companion objects for a class.</li>
  <li>How to extend existing classes with new properties and methods.</li>
</ul>

---

<h1>⭐Make a reasonable class with generics.</h1>
<ul>
  <p>🌟Let's say you are planning a Quizz App which invoves following Questions.</p>
  <li>Fill-in-the-blank question: The answer is a word represented by a <code>String</code>.</li>
  <li>True or false question: The answer is represented by a <code>Boolean</code>.</li>
  <li>Math problems: The answer is a numeric value. The answer for a simple arithmetic problem is represented by an <code>Int</code>.</li>
  <p>In Addition, Quizz question will also have difficulty rating like in String as 'easy','medium','hard'.</p>
</ul>
<strong>Now,Define classes to represent each type of quiz question:</strong>
<ul>
  <li>1. Navigate to <a href = "https://play.kotlinlang.org/"/>Kotlin Playground</a> to practice Kotlin Language on Web based IDE</li>
  <li>2. In Kotlin Playground, create three classes named <code>FillInTheBlankQuestion</code>,<code>TrueOrFalseQuestion</code><code>NumericQuestion</code></li>
  <li>3. Your code should be like this with answertext as String for FillInTheBlankQuestion,<code>Boolean</code> for TrueOrFalseQuestion,<code>Int</code> for NumericQuestion:</li>
  
```kotlin
class FillInTheBlankQuestion(
    val questionText: String,
    val answer: String,
    val difficulty: String
)

class TrueOrFalseQuestion(
    val questionText: String,
    val answer: Boolean,
    val difficulty: String
)

class NumericQuestion(
    val questionText: String,
    val answer: Int,
    val difficulty: String
)
```
</ul>
<ul> <li> <p>The only difference in all classes is the data type of the <code>answer</code> (<code>String</code>, <code>Boolean</code>, <code>Int</code>).</p> </li> <li> <p>You might think of using <strong>inheritance</strong> — creating a parent class for shared properties.</p> </li> <li> <p><strong>But that doesn't work well here because:</strong></p> <ul> <li>You still need to define a separate <code>answer</code> in each subclass.</li> <li>It’s awkward to have a parent class without an <code>answer</code> property.</li> </ul> </li> <li> <p>🔁 <strong>Instead of inheritance, use <code>generics</code> in Kotlin:</strong></p> </li> <li> <p><code>Generics</code> let you create one class where the <code>answer</code> can be any data type.</p> </li> <li> <p>This makes your code <strong>simpler, cleaner, and easier to manage</strong>.</p> </li> <li> <p>✅ So, one <code>Question&lt;T&gt;</code> class works for any type of question.</p> </li> </ul>


<h2>🤔So,What is Generic Datatype?</h2>
<ul>
  <p><strong>Generic types</strong> let you use a placeholder for a data type. Instead of creating different classes for each data type (like <code>String</code>, <code>Int</code>, or <code>Boolean</code>), you use a single class with a type parameter like <code>&lt;T&gt;</code>.</p>
</ul>
