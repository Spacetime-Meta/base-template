# 👋 Welcome to the base template, where creation starts!

## Intro

*The goal of this base-template is to provide an easy start for creators to publish virtual environments using the [spacetime-sdk](https://github.com/Spacetime-Meta/spacetime-sdk). To simplify usage, it only contains client side code. This means you will need a hosting service of your choice to host your project.* 

After downloading the base template, you should find yourself with the following structure:
```
📦base-template
 ┣ 📜README.md
 ┣ 📜index.html
 ┗ 📂assets
    ┗ ⛰️terrain.glb
```

In this readme we will explain the following things:  

1. How to change the world for my custom 3D model. 
2. Line by line overview of the code

## 1. ⛰️ How to use my custom 3D model as the terrain.
To use your custom 3D model as the terrain of your virtual environment, you will first need it in the `.glb` format. Once your 3D model is in the right format, add it to the `📂assets` folder.

Finaly, on the **line 23**, you can see the path to a `.glb` file. Just change this path so it points to your terrain.

Example: if your new terrain is saved as `newCustomModel.glb`, you will change `url: "./assets/terrain.glb"` for `url: "./assets/newCustomModel.glb"`

We recommend placing your own `.glb` or `.gltf` file in the asset folder of this project. 

## 2. Line by line of the `index.html` file

In this section we will cover the `index.html` file line by line. This is the main entry point into your world.

Most of these lines you will never have to touch and are the same for every single spacetime world. 

**line 6:**
```HTML
<title>Base Template</title>
```
Changing the content of this tag will change the title of your browser tab.

**lines 8-10:**
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

**lines 18 and 32:**
```HTML
<script type="module">
 // some code
</script>
```
These lines makes the beginning and the ned of the Javascript code that generate the content of your world

**lines 21-25**
```javascript
const virtualEnvironment = new VirtualEnvironment({
    terrain: {
        url: "./assets/terrain.glb"
    }
});
```
This is where the action happens in these lines we create the vitual environment by passing a configuration to the constructor.
here, the configuration only says that the terrain should be loaded from an url. You can also save the config in a `.json` file and pass the url to that config.

**lines 28-32**
```javascript
 animate();
 function animate() {
     VIRTUAL_ENVIRONMENT.update();
     requestAnimationFrame(animate);
 }
```
These lines start the animation loop. The method `VIRTUAL_ENVIRONMENT.update();` will be called 60 times per second.

**Other lines**
This is just the base structure of a html file. To lean more, go to the [w3school](https://www.w3schools.com/) website.
