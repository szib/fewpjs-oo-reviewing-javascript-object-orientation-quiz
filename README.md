## Quiz: Reviewing JavaScript Object Orientation

???

# Reviewing JavaScript Object Orientation

?:

```javascript
class Tree {
  constructor(type) {
    this.type = type;
  }
}
```

How would we create an instance of the above `class`?

( ) `Tree.initialize(‘Oak’)` (X) `new Tree(‘Oak’)` ( ) `new Tree().constructor(‘Oak’)` ( ) `let oak = new Tree(); Tree.type = ‘Oak’`

?: If we created an instance of Tree and stored it as the variable `oak`, how would we access the `type` property?

[ ] `oak(‘type’)`
[ ] `oak.properties(‘type’)`
[X] `oak[‘type’]`
[X] `oak.type`

?: Once that instance is created, how would we modify the `type` property?

[X] `oak.type = ‘maple’`
[ ] `oak.properties(‘type’) = ‘maple’`
[ ] `oak(‘type’) = ‘maple’`
[X] `oak[‘type’] = ‘maple’`

?:

```javascript
class Example {
  constructor(text) {
    this._text = text
  }
}
```

Above, we have an `Example` class. If we wanted to add a method called `info()` within the `Example` class, how would we write it?

( ) `function info() { }` (X) `info() { }` ( ) `get info() { }` ( ) `set info() { }`

?: Once we have defined our `info()` method, we might need to use the method somewhere else in our `Example` class. Choose the exact code necessary to access the `info()` method from within the `Example` class.

(X) `this.info()` ( ) `self.info()` ( ) `example.info()` ( ) `Example.info()`

?: The constructor within `Example` class assigns a variable `_text` to whatever is passed in when a new `Example` is created. If we wanted to create a getter method called `text()` to access this property, how would we write it?

( ) `text() { return this._text }`
( ) `text = () => { return this._text }`
(X) `get text() { return this._text }`
( ) `text = () => this._text`

?: What code would we need to write in order access our newly create getter method from within the `Example` class?

( ) `example.text` (X) `this.text` ( ) `self.text` ( ) `Example.text`

?: With a getter method, we can access the `_text` property indirectly. If we wanted to create a corresponding setter method, how would we write it?

( ) `text(text) { this._text = text }` ( ) `text = (text) => { this._text = text }` (X) `set text(text) { this._text = text }` ( ) `text = (text) => this._text = text`

?: Say we wanted to set our `_text` variable to ‘hello world!’ using our new setter class. From inside the `Example` class, what code would we need to write?

( ) `this.text() = ‘hello world!’` ( ) `this.text(‘hello world!’)` (X) `this.text = ‘hello world!’` ( ) `example.text = ‘hello world!’`

?:

```javascript
let example = new Example()
```

If the `example` variable is assigned to a new instance of Example, how would we access the info() method using `example`? Write the exact code needed.

( ) `this.info` ( ) `example.info` ( ) `this.info()` (X) `example.info()`

?: We’ve also created a getter method, `text`. How would we access this method using the `example` variable? 

( ) `example.get(‘text’)` (X) `example.text` ( ) `example.get(“text”)` ( ) This is not accessible

?: Using the setter method we created earlier, if we wanted to set `_text` to 'hello world!' using our `example` variable, how would we do it?

( ) `example.text(‘hello world!’)` (X) `example.text = ‘hello world!’` ( ) `example.text() = ‘hello world!’` ( ) `this.text = ‘hello world!’`

?: All class methods and properties are accessible from outside of the class.

(X) True ( ) False

?:

```javascript
class House {
  constructor(address, owner) {
    this.address = address;
    this.owner = owner;
  }
}

let house1 = new House('22 Elm St', 'Alan Turing');
let house2 = new House('11 Broadway', 'Grace Hopper');
house1.owner = 'Ada Lovelace';
house2.address = '1440 G St NW';
```

Imagine the code above executing. At the end, what is the value of the `address` property of `house1`?

(X) ‘22 Elm St’ ( ) ‘11 Broadway’ ( ) ‘1440 G St NW’ ( ) ‘Ada Lovelace’

?: What is the `address` value of `house2`?

( ) ‘22 Elm St’ ( ) ‘11 Broadway’ (X) ‘1440 G St NW’ ( ) ‘Ada Lovelace’

???
