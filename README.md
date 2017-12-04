# Download-Egghead-Videos.md

Go to the egghead website, i.e. [Learn ES6 (ECMAScript 2015)](https://egghead.io/courses/learn-es6-ecmascript-2015)

run 

```js
$("a.flex.h-100.absolute.top-0.right-0.bottom-0.left-0" ).each(function( index, video ) {
  console.log(video.href);
});
```

You will get the following url_list

```text
https://egghead.io/lessons/javascript-arrow-function-in-es6
https://egghead.io/lessons/javascript-the-let-keyword-in-es6
https://egghead.io/lessons/javascript-default-values-for-function-parameters-in-es6
https://egghead.io/lessons/javascript-const-declarations-in-es6-es2015
https://egghead.io/lessons/javascript-shorthand-properties-in-es6
https://egghead.io/lessons/javascript-object-enhancements-in-es6
https://egghead.io/lessons/javascript-using-the-es6-spread-operator
https://egghead.io/lessons/javascript-use-template-literals-in-es6
https://egghead.io/lessons/javascript-destructuring-assignment-in-es6
https://egghead.io/lessons/ecmascript-6-es6-modules-es2015-import-and-export
https://egghead.io/lessons/javascript-converting-an-array-like-object-into-an-array-with-array-from
https://egghead.io/lessons/javascript-promises-with-es6
https://egghead.io/lessons/ecmascript-6-es6-es2015-generators
https://egghead.io/lessons/javascript-maps-and-weakmaps-with-es6
https://egghead.io/lessons/javascript-es6-parameter-object-destructuring-with-required-values
https://egghead.io/lessons/javascript-es6-rest-parameters
```

Steps:

1. Save as url_list.txt

2. `brew install youtube-dl`

3. `youtube-dl -a url_list.txt`


Run this rename script to get rid of the [Mojibake](https://en.wikipedia.org/wiki/Mojibake)

```bash
for i in *mp4; do
   mv "$i" "`echo $i | sed "s/#.*//"`"'.mp4';
done
```
