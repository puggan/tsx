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
