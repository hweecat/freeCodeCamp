---
title: Use model.find() to Search Your Database
---
# Use model.find() to Search Your Database


---
## Hints

### Hint 1
Replace `Model` with the name of your model from the previous sections. Most likely this is `Person`.

### Hint 2
Use `{name: personName}` for the first argument in `Model.find()`.


---
## Solutions

<details><summary>Solution 1 (Click to Show/Hide)</summary>

Code for `myApp.js`

```javascript
/** 1) Install & Set up mongoose */
const mongoose = require('mongoose');
mongoose.connect(process.env.MONGO_URI);

/** 2) Create a 'Person' Model */
var personSchema = new mongoose.Schema({
  name: String,
  age: Number,
  favoriteFoods: [String]
});

/** 3) Create and Save a Person */
var Person = mongoose.model('Person', personSchema);

var createAndSavePerson = function(done) {
  var janeFonda = new Person({name: "Jane Fonda", age: 84, favoriteFoods: ["vodka", "air"]});

  janeFonda.save(function(err, data) {
    if (err) return console.error(err);
    done(null, data)
  });
};

/** 4) Create many People with `Model.create()` */
var arrayOfPeople = [
  {name: "Frankie", age: 74, favoriteFoods: ["Del Taco"]},
  {name: "Sol", age: 76, favoriteFoods: ["roast chicken"]},
  {name: "Robert", age: 78, favoriteFoods: ["wine"]}
];

var createManyPeople = function(arrayOfPeople, done) {
  Person.create(arrayOfPeople, function (err, people) {
    if (err) return console.log(err);
    done(null, people);
  });
};

/** 5) Use `Model.find()` */
var findPeopleByName = function(personName, done) {
  Person.find({name: personName}, function (err, personFound) {
    if (err) return console.log(err);
    done(null, personFound);
  });
};
```
</details>
