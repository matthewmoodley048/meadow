<script setup lang="ts">


</script>

<template>
  
    <h1>Educating a machine</h1>
  <hr class="rounded"/>
  <div class="columns">
    <h2>Introduction</h2>
    <div class="coverImage"/>
    <article class="blocks">
     <p>
        To start off, machine learning isn't necessarily a machine 'learning' per say, its more of creating a set of rules or calculations that the computer will execute (in other words an algorithm) against a set of data or examples that you provide it.</p>
      <p> 
When i put it that sense you might be asking, if it is just following a set of rules then why say it is learning? Well i left out one crucial part, arguably the part that  makes it special.
      </p>
      <p>
From the rules and data provided, it will then build a model based on the data.What this model can do then is essentially 'predict' the next set of values, as if it learned how to.
        So in simple terms its like giving a 7 year old, lets call him Timmy, some simple addition and subtraction problems to solve with the answers at the back (rules: addition and subtraction, dataset: the homework with answers) and then asking Timmy for answers to some other addition or subtraction problems.</p>
      <p>
To summarize and actually define what machine learning is, it is simply solving a practical problem by gathering the dataset, and then algorithmically building a statistical model based on the dataset, then use the model to solve the problem. 
     </p>
    </article>
  </div>
  <div class="columns">
    <hr class="rounded"/>
  <article class="blocks">
    <h2>Types of machine learning</h2>
      <p>
There are four types of machine learning, namely Supervised learning, Semi-supervised learning, Un-supervised learning and reinforcement learning.To keep this short ill be focusing on the two main types Supervised and Un-supervised. 
      </p>
      <p>
Supervised learning basically is training the model on a labeled data set, for a example a table consisting of different cars with labelled columns for make, year, engine size etc. With supervised learning, there are two types of techniques: Regression and Classification. 
      </p>
      <p>
Regression a method of predicting a continuous value from the data set. Taking from the previous example it would be predicting the engine size or the year of the car for instance.

      </p>
      <p>
Classification in a way the opposite of regression. Instead of trying to predict the value, it predicts the label of the value. So given a value for instance Honda, if successful, it would then predict the label as make.
      </p>
      <p>
Supervised learning is one of the more popular models to use as it is very accurate, some examples of use cases would be finding spam emails in your inbox or identifying how likely a patient is suspect to diabetes.
      </p>
      <p>
Now if that's supervised, what does un-supervised entail? Un-supervised is training the model on a dataset that contains no labels, because of this the algorithms used to build the model can become quite complex.

      </p>
      <p>
Now you might be thinking supervised seems like a better option, well in most use cases that  is true. Use cases where un-supervised learning shines is when anomaly prediction and a strong ability to better adapt to unseen data is required.
      </p>
      <p>
A use case would be to categorize customers ( budget conscious spender, high value spender) from a retail's store purchase history.
      </p>
  </article>
  </div>

  <div class="columns">
    <hr class="rounded"/>
    <article class="blocks">
      <h2>Evaluation methods</h2>
      <p>
Now that you have understand some of the machine learning types, lets talk about evaluation methods.
      </p>
      <p>
evaluation methods are ways in which to essentially confirm the effectiveness of the algorithms used for the model.
      </p>
      <p>
One of the ways is the to train and test. This way you train the model on the entire data set and then test the model on that same dataset. 
      </p>
      <p>
Going back to Timmy as an example it would be giving him addition and subtraction homework and then testing him on the same problems used in the homework.
      </p>
      <p>
This would make the model accurate but like Timmy it would struggle with problems outside the data provided.
      </p>
      <p>
another way is the train test split method.This method splits the dataset into portions used for training and testing. 
      </p>
      <p>
This helps alleviate the problem seen in the train and test method of predicting outside the dataset, but with the drawback of being less accurate.
      </p>
    </article> 
  </div>

  <div class="columns">
    <hr class="rounded"/>
    <article class="blocks">
      <h2>Conclusion</h2>
      <p>
So, to wrap it up, machine learning isn't some magic trick where a computer suddenly gets super smart. 
      </p>
     <p>
It's about building a fancy calculator, if you will, that can take a bunch of data and examples (like our friend Timmy with his math problems and answer sheet), crunch some serious numbers, and then predict what might happen next. 
      </p>
     <p>
 It's pretty cool, actually, like teaching a machine a new skill without explicitly telling it how.
But that's just the tip of the iceberg. 
      </p>
    </article> 
  </div>
  <hr class="rounded"/>
</template>

<style scoped>

h1 {
  font-weight: bold;
  font-size: 4vw;
  position: relative;
  top: 0px;
  padding-left: 1vw;
  margin: 0.5em;
  text-align: flex-start;
}

p {
  font-size: 2vw;
  margin-bottom: 1em;
}

h2{
  font-weight: bold;
  font-size: 2.5vw;
  margin: 0.5em;
}

.header h1,

hr.rounded {
  border-top: 2px solid #000000;
  border-radius: 5px;
  width: 105vw;
}

.coverImage {
  position: relative;
  background: url('../assets/images/machineLearning.jpg') no-repeat center;
  background-size: cover;
  width: 30vh;
  height: 30vh;
  margin-left: 5vw;
  box-shadow: inset 0px 0px 10px 50px #f2f2f2, 0px 0px 5px 5px #f2f2f2;
}

.columns {
columns: 1;
margin: 1em;
}

.blocks{
margin-top: 1em;
width: 70vw;
overflow-wrap: break-word;
}

  

@media (min-width: 1000px) {
  .header h1,

.blocks{
 width:32vw;
 margin: 1em;
 overflow-wrap: break-word;
}

.columns {
 columns: 2;
 width: 70vw;
 text-wrap: wrap;
 margin-left: 10em;
}

h1 {
 font-weight: bold;
 font-size: 3vw;
 position: relative;
 top: 0px;
 padding-left: 1vw;
 margin: 0.5em;                                                                                                                                                                        
 text-align: flex-start;
}

p {
 font-size: 1vw;
}

h2{
 font-weight: bold;
 font-size: 1.5vw;
 margin: 0.5em;
}


.coverImage {
 position: relative;
 background: url('../assets/images/machineLearning.jpg') no-repeat center;
 background-size: cover;
 width: 20vw;
 height: 20vw;
 margin-left: 1vw;
 box-shadow: inset 0px 0px 10px 50px #f2f2f2, 0px 0px 5px 5px #f2f2f2;  
}

}
</style>
./CoverObject.js
