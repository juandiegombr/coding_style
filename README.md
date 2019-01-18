# Frontend Documentation

___
### Index
- [Vue project structure](https://github.com/juandiegombr/coding_style/tree/master#vue-project-structure)
- [Why coding style matters?](https://github.com/juandiegombr/coding_style/tree/master#why-coding-style-matters)
  - [Standard Javascript rules](https://github.com/juandiegombr/coding_style/tree/master#standard-javascript-rules)
  - [Custom Javascript rules](https://github.com/juandiegombr/coding_style/tree/master#custom-javascript-rules)
  - [Custom HTML/Template rules](https://github.com/juandiegombr/coding_style/tree/master#custom-htmltemplate-rules)
  - [Custom css/scss rules](https://github.com/juandiegombr/coding_style/tree/master#custom-cssscss-rules)
___

# Vue Project Structure

## Reference links
- [Structuring Vue Components](https://vueschool.io/articles/vuejs-tutorials/structuring-vue-components/) by Alex Jover.

## Folders structure
- **./src:** Folder where the Vue project is located.
  - **/assets:** Place for global style and images.
    - **/sass:**
    - **/images:**
  - **/components:**
    - **/icons:** All .svg icons wrapped in a Vue component
    - **/common:** All components not matching any other condition.
    - **/ui:** All global components related to the UI (button, input, list)
  - **/filters:** Contains all files used as global filters.
  - **/lang:** Contains all files related to internationalization.
    - **messages:** All countries translations. (es, es-MX, es-CO, pr-BR)
    - **index.js:** Init Vue internationalization.
    - **numberFormats.js:** Number & currencies translations.
  - **/pages:** It has the same structure of our index route file.
    - **/home:** Contains all components used only in home page
  - **/router:** All the App routes.
  - **/services:** Contains all files that manage the connection with the backend.
  - **/store:** Contains all files and folders related to Vuex.
    - **/modules:** All Vuex files to structure the store.
    - **index.js:** Init Vuex store.
  - **/utils:** Where global constants and functions are placed.
    - **App.vue:** Main Vue file.
    - **main.js:** Inits Vue project
    
# Why coding style matters?
## Coding style helps collaboration

> The most important thing when working on a team is **communication.** People need to be able to work together effectively and the only way to do that is by communicating. As developers, we communicate primarily through code. We communicate with other parts of the software through code and we communicate with other developers through code.

> Any large code base with multiple team members should looks as if only one programmer wrote it.

# Standard Javascript rules

## Reference links
- [Javascript Standard style](https://standardjs.com/rules.html#javascript-standard-style)

## Rules
- **No semicolons!** Please.
```js
console.log(foo) // Correct
console.log(foo); // Incorrect
```
- Use **2 spaces** for indentation.
```js
// Correct
const fn (arg) {
  console.log('foo')
}

// Incorrect
const fn (arg) {
    console.log('foo')
}
```
- Do not use **multiple spaces** for indentation.
```js
const foo = 'bar' // Correct
const foo =      'bar' // Incorrect
```
- Must have a **space** before blocks.
```js
if (foo) {...} // Correct
if (foo){...} // Incorrect
```
- **No spaces** inside parentheses.
```js
foo('bar') // Correct
foo( 'bar' ) // Incorrect
```
- Use **spaces** inside comments.
```js
// Correct
//Incorrect
```
- **No spaces** in template strings.
```js
cons foo = `Hello ${world}` // Correct
cons foo = `Hello ${ world }` // Incorrect
```
- Use **single quotes** for strings except to avoid escaping.
```js
console.log('foo')
console.log("<div class='bar'>")
```
- No **unused** variables.
```js
const fn = (arg) => {
  const foo = 'bar'
}
```
- Add **space** after keywords.
```js
if (foo) {...} // Correct
if(foo) {...} // Incorrect
```
- Add **space** before a function declaration's parentheses.
```js
const fn (arg) {...} // Correct
const fn(arg) {...} // Incorrect
```
- Always use **=== or !==** for comparations.
```js
if (foo === 'bar') {...} // Correct
if (foo !== 'bar') {...} // Correct

if (foo == 'bar') {...} // Incorrect
if (foo != 'bar') {...} // Incorrect
```
- **Infix operators** must be spaced.
```js
const foo = 2 // Correct
const bar = 'hello' + 'world' // Correct

const foo=2 // Incorrect
const bar = 'hello'+'world' // Incorrect
```
- **Commas should have a space** after them.
```js
const foo = [1, 2, 3, 4, 5] // Correct
const bar = (arg1, arg2) {...} // Correct

const foo = [1,2,3,4,5] // Incorrect
const bar = (arg1,arg2) {...} // Incorrect
```
- Keep **else statements** on the same line as their curly braces.
```js
// Correct
if (foo) {
  //...
} else {
  //...
}
// Incorrect
if (foo) {
  //...
}
else {
  //...
}
```
- For **multi-line if statements,** use curly braces.
```js
// Correct
if (foo) 'bar'
if (foo) {
  return 'bar'
}
// Incorrect
if (foo)
  return 'bar'
```
- Always **handle the error** function.
```js
promise
  .then(success)
  .catch(error)
```
- **Multiple blank lines** not allowed.
```js
// Correct
const foo = 'bar'
const bar = 'hello' + 'world'

// Incorrect
const foo = 'bar'


const bar = 'hello' + 'world'
```
- For the **ternary operator** in a multi-line setting, place ? and : on their own lines.
```js
// Correct
const foo = bar ? 'hello' : 'world'
const foo = bar
  ? 'hello'
  : 'world'

// Incorrect
const foo = bar ?
  'hello' :
  'world'
```
- For **constanst and variable** declarations, write each one in its own statement.
```js
// Correct
const foo = 2
const bar = 4

// Incorrect
const foo = 2, bar = 4
const foo = 2,
      bar = 4
```
- Add **spaces** inside single line blocks.
```js
const foo = () => { return true } // Correct
const foo = () => {return true} // Incorrect
```
- Use **camelCase** when naming variables and functions.
```js
const helloWorld = () => { return true } // Correct
const helloWorld = 'bar' // Correct

const hello_world = () => { return true } // Incorrect
const hello_world = 'bar' // Incorrect
```
- Trailing **commas** not allowed.
```js
// Correct
const foo = {
  a: 1,
  b: 2
}

// Incorrect
const foo = {
  a: 1,
  b: 2,
}
```
- **Commas** must be places at the end of the current line.
```js
// Correct
const foo = {
  a: 1,
  b: 2
}

// Incorrect
const foo = {
  a: 1
  ,b: 2
}
```
- **Dot** should be on the same line as property.
```js
// Correct
promise()
  .then()

// Incorrect
promise().
  then()
```
- Files must en with a **newline.**
```js
// Correct
promise()
  .then()

// _____ end file

// Incorrect
promise().
  then()
// ____ end file
```
- **No space** between function identifiers and their invocations.
```js
foo('bar') // Correct
foo ('bar') // Incorrect
```
- Add **space** between colon and value in key value pairs .
```js
// Correct
const foo = {'bar': hello}

// Incorrect
const foo = {'bar' : 'hello'}
const foo = {'bar':'hello'}
```
- **Constructor names** must begin with capital letter.
```js
// Correct
const Animal = () => {}
const dog = new Animal()

// Incorrect
const animal = () => {}
const dog = new animal()
```
- Use a **single import** statement per module.
```js
// Correct
import { fn1, const1 } from 'module'

// Incorrect
import { const1 } from 'module'
import { const1 } from 'module'
```
- Only **throw** an Error object.
```js
throw new Error('error') // Correct
throw 'error' // Incorrect
```
- Initializing to **undefined** is not allowed.
```js
let foo // Correct
let foo = null // Correct

let foo = undefined// Incorrect
```
- **No ternary operators** when simpler alternatives exist.
```js
let foo = val || 'bar' // Correct
let foo = val ? val : 'bar' // Incorrect
```

# Custom Javascript rules
- Pass **named arguments** with an object instead an array.
```js
// Correct
const foo = ({arg1: '1', arg2: '2'}) => {}
foo(args)

// Incorrect
const foo = (arg1, arg2) => {}
foo(arg1, arg2)
```
- Use constants instead of **strings.**
```js
// Correct
const type = 'bar'
if (foo === type) {}

// Incorrect
if (foo === 'bar') {}
```
- Use **arrow syntax** instead of function.
```js
// Correct
const foo = () => {}

// Incorrect
function foo() {}
```
- **No use function syntax** in Vue script (methods, computed...).
```js
// Correct
computed: {
  foo () {
    return true
  }
}

// Incorrect
  computed: {
    foo: function () {
      return true
    }
  }
```
- Apply the following **script order** in .vue files.
```js
export default {
  name: 'base-component',
  mixins: [],
  computed: {},
  methods: {}
  data: () => {},
  // lifecycle hooks...
  beforeCreate () {}, 
  created () {},
  components: {}
}
```
- Add **a line break** to separate library imports from local imports.
```js
import Vue from 'vue'

import { products } from '@/utils/Constants'
```

# Custom HTML/Template rules
- **Use double quotes** for attributes except for avoid scaping.
```html
// Correct
<div class="foo"></div>
<div :class="foo === 'bar'"></div>

// Incorrect
<div class='foo'></div>
<div :class='foo === "bar"'></div>
```
- **Use shorthand** for v-bind and v-on.
```html
// Correct
<div :class="foo"></div>
<div @click="onClick"></div>

// Incorrect
<div v-bind:class="foo"></div>
<div v-on:click="onClick"></div>
```
- **Use alias** in import statements.
```js
import foo from '@/bar' // Correct
import foo from '../bar' // Incorrect
```
- Separate by a **line break** when an element has more than three attributes.
```html
// Correct
<div id="foo" class="foo" @click="onClick">
  Hello World
</div>
<div
  id="foo"
  class="foo"
  @blur="onBlur"
  @click="onClick">
  Hello World
</div>

// Incorrect
<div id="foo" class="foo" @blur="onBlur" @click="onClick">
  Hello World
</div>
```

# Custom CSS/SCSS rules

## Reference links
- // BEM Article
- // Unit measures

## Rules
- Use always **scss** lang.
```html
<style lang="scss">
  /* ... */
</style>
```
- Use always **snake-case** to define classes.
```css
.button-primary {} // Correct
.buttonPrimary {} // Incorrect
```
- **Do not use more than two levels** of nesting in scss.
```css
// Correct
.block {
  &__element {
    &--modifier {
    }
  }
}
// Incorrect
.block {
  &__element {
    &--modifier {
      .icon {
        &::before {
        }
      }
    }
  }
}
```
- Neves use **!important**, instead use the proper specificity selector.
```css
// Correct
div.first-class.second-class i{
  color: red;
}
// Incorrect
.first-class i {
  color: red!important;
}
```
- Never use **#id** as a css selector.
```css
.button-primary {} // Correct
#button-primary {} // Incorrect
```
- Priorize to use **rem** instead of px.
```css
// Correct
.foo {
  font-size: 2rem;
}
// Incorrect
.foo {
  font-size: 15px;
}
```
