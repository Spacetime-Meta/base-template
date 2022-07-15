# 👋 Welcome to the base template. Here is where creation starts!

After downloading the base template, you should find yourself with the following structure:
```
📦base-template
 ┣ 📜README.md
 ┣ 📜index.html
 ┗ 📂assets
    ┗ ⛰️terrain.glb
```


In this readme we will explain the following things:  

1. How to change the world. 
2. Line by line

## 1. How to change the world
on the **line 23**, you can see the path to a `.glb` file. Just change this path so it points to your terrain.
```javascript
url: "./assets/terrain.glb"
```

We recommend placing your own `.glb` or `.gltf` file in the asset folder of this project. 

## 2. Line by line of the `index.html` file

In this section we will cover the `index.html` file line by line. This is the main entry point into your world.

Most of these lines you will never have to touch and are the same for every single spacetime world. 

**line 6:**
```HTML
<title>Base Template</title>
```
Changing the content of this tag will change the title of your browser tab.

**line 8-10:**
```HTML
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100;400;700&family=Space+Mono&display=swap" rel="stylesheet">
  
```
These lines import the fonts and provide scaling information to the browser. You should not have to modify these lines.

**line 16:**
```HTML
<script src="https://www.spacetimemeta.io/sdk/v1/bundle.min.js"></script>
```
This line imports the spacetime sdk form the spacetime website, you should not have to change this.

**line 18 and 32:**
```HTML
<script type="module">
 // some code
</script>
```
These lines makes the beginning and the ned of the Javascript code that generate the content of your world

**Other lines**
```HTML
<!DOCTYPE html>
    <html lang="en">

        <head>
        </head>

        </body>
        </body>

    </html>
</html>
```
This is just the base structure of a html file. To lean more, go tot he w3school website.
