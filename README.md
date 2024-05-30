# Useage
1. Compile the jsx.ts and your tsx files
2. Load both compiled files in the document, ex:
```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Test 1</title>
        <script src="jsx.js"></script>
        <script src="test1.js"></script>
    </head>
    <body>
        <h1>Test 1</h1>
    </body>
</html>
```

# Typesctip Options
```
{
  "compilerOptions": {
    "jsx": "react",
    "jsxFactory": "JsxFactory.createElement",
    "jsxFragmentFactory": "JsxFactory.Fragment"
  }
}
```

# Supported functionality
## Plain jsx
```
document.body.appendChild(<p id="hw">Hellow World</p>);
```
## Arrays
```
const lis = [];
lis.push(<li>A</li>);
lis.push(<li>B</li>);
lis.push(<li>C</li>);
document.body.appendChild(<ul>{lis}</ul>);
```
## Fragments
```
const list = ['A', 'B', 'C'];
document.body.appendChild(list.map(row => <><span>{row}</span><br/></>));
```
# classes
```
document.body.appendChild(<span class="a b c">A</span>);
document.body.appendChild(<span class={['a', 'b', 'c']}>A</span>);
document.body.appendChild(<span class={{a: true, b: false, c: true}}>A</span>);
```
# Listners
```
document.body.appendChild(<input onblur={event => alert(event.currentTarget.value)} />);
```
