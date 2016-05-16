> **The goal of this guide:** How to communicate between elements using databinding in polymer. If you come across terms you don't understand Google them or feel free to ask a team member within digital reach.

# How to use Polymer databinding

### Table of content
- Why?
- How?
- In-depth

### Why?

Elements have one function and the website is built out of many elements. The same data is used in different elements though. Therefore data has to flow through elements.

👁Example: A user writes his/her name in a 'text-input' element. You want to store this information in a database. Communication with database happens in a different element though. Also, it wouldn't make sense if all the input elements would communicate with the database themselves, it would be better if the element 'add-user-form' (which has a lot of 'text-input' elements in it) would do all the communication with the 'database-communication' element. Therefore the same data has to be communicated to at least three elements: text-input, add-user-form and database-communication. A change in one of the elements would also have to cause a change in the other two.

### How?

Databinding is [[one way]] or {{two way}}. All types of information can be communicated between elements (strings, objects, booleans, etc.). The type of the property on the on the child's side has to be the same as the one on the parent's side (you can't fit an object in a string). It is possible to pair a string that is inside an object with a string, e.g.
``` html
user-name="{{user.name}}".
```

#### In parent element:
``` Html
<child-element
    data-object="{{dataObject}}"
></child-element>
```

Note that data-object, the name of the object in the child element, is with a -, known as [kebab-case](https://en.wikipedia.org/wiki/Letter_case#Special_case_styles), while the other is in [camelCase](https://en.wikipedia.org/wiki/CamelCase).
This is because Html is case insensitive where Javascript isn't. The object in the both elements can be used by {{dataObject}} and not {{data-object}} !

#### In parent and child element:

``` javascript
properties: {
    dataObject: {
        type: Object,
        notify: true
    },
},
```
**notify: true** is very important since it signals polymer that changes in the object in the current element have to be signaled to other elements. You are guaranteed 🔮to spend a few hours on this at least once by forgetting it 😞.

### More in-depth
[This video](https://www.youtube.com/watch?v=1sx6YNn58OQ) explains how polymer communicates changes across elements. Well worth the watch!
