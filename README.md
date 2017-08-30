# D3 v4 Randomly Generated Graph

A basic bar chart with randomly generated json data.

```
var data = [];
var space = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz";
var spaceLength = space.length;
makedata();

function makedata() {
  var obj = {};

  for (var i = 0; i < spaceLength; i++) {
    obj = {};
    value = Math.floor(Math.random() * 500);
    rand = Math.floor(Math.random() * space.length)
    name = space.charAt(rand);
    obj["name"] = name;
    obj["val"] = value;
    data.push(obj);
    space = space.slice(0, rand) + space.slice(rand + 1, space.length)
  }
}
```

Demo: [gh-pages](https://shanegibney.github.io/d3RandomlyGeneratedBarChart/)

<img width="818" alt="screen shot 2017-08-30 at 19 26 19" src="https://user-images.githubusercontent.com/17167992/29888536-2fcf7556-8db9-11e7-843b-27e5c481b193.png">
