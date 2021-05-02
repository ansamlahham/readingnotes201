# HTML Tables; JS Constructor Functions

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an **object-oriented** model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

### Model epic fails videos

Imagine you've been tasked to build a program that models the popularity of [epic fail](http://www.urbandictionary.com/define.php?term=epic+fail) videos. After months of painstaking research, you've determined that the two essential metrics for gauging popularity are **an epic rating** and **whether or not the video has animals**.

Since you'll be modeling the popularity of many types of videos—parkour epic fails, corgi epic fails, etc.—you'll want to build self-contained objects with the **same attributes and behaviors**. That way, when you need to change the algorithm for determining popularity, the changes will be small and targeted.

![](http://www.gifbin.com/bin/082011/1312218114_corgi_rodeo.gif)

As you read this article, type out and run all code samples you come across. **Do not copy and paste**. Writing out and testing your code will help you remember how to implement domain models in JavaScript later.

### What’s a Table?
A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results ***The <-table> element is used to create a table. The contents of the table are written out row by row. <-tr> You indicate the start of each row using the opening <-tr> tag. (The tr stands for table row.) It is followed by one or more <-td> elements (one for each cell in that row). At the end of the row you use a closing </-tr> tag.<-td> Each cell of a table is represented using a <-td>element. (The td stands for table data.) At the end of each cell you use a closing <-/td> tag.

Here's some tips to follow when building your own domain models.

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
1. Model its attributes with a constructor function that defines and initializes properties.
1. Model its behaviors with small methods that focus on doing one job well.
1. Create instances using the `new` keyword followed by a call to a constructor function.
1. Store the newly created object in a variable so you can access its properties and methods from **outside**.
1. Use the `this` variable within methods so you can access the object's properties and methods from **inside**.

### Define a constructor and initialize properties

To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an `EpicFailVideo` object.

| Property     | Data              | Type    |
|--------------|-------------------|---------|
| `epicRating` | `1` to `10`       | Number  |
| `hasAnimals` | `true` or `false` | Boolean |

Here's an implementation of the `EpicFailVideo` constructor function.

```javascript
var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail);
console.log(corgiFail);
```

### Generate random numbers

To model the random nature of user behavior, you'll need the help of a random number generator. Fortunately, the JavaScript standard library includes a `Math.random()` function for just this sort of occasion.

```javascript
var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.generateRandom(1, 5));
console.log(corgiFail.generateRandom(1, 5));
```
### Calculate daily Likes

Popularity of a video is measured in Likes. And the formula for calculating Likes is the number of viewers times the percentage of viewers who'll Like a video. In other words, **viewers times percentage**.

To calculate the number of viewers per day, generate a random number between 10 and 30 and then multiply it by the epic rating of that video.

| Random number | Epic rating | Viewers per day |
|---------------|-------------|-----------------|
| 10            | 10          | 100             |
| 20            | 9           | 180             |
| 30            | 8           | 240             |

The percentage of viewers who'll Like a video depends on whether or not the video contains animals.

| Animals | Percentage |
|---------|------------|
| Yes     | 75%        |
| No      | 40%        |

With this knowledge in hand, let's model the number daily Likes an epic fail video will receive.

```javascript
var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

EpicFailVideo.prototype.dailyLikes = function() {
  var viewers, percentage;

  viewers = this.generateRandom(10, 30) * this.epicRating;

  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }

  return Math.round(viewers * percentage);
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.dailyLikes());
console.log(corgiFail.dailyLikes());
```