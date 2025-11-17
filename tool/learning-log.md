# Tool Learning Log

## Tool: **Godot**

## Project: **"Sneaky Snacks"**

---

### 9/29/25:
* First thing I did was download Godot and import it into github. I did this by creating a new project on Godot then using Github desktop to add the project folder into a new repository and published it to github. Then I cloned the Godot repo into my Freedom Project folder in my IDE. I watch the video ["Godot 4 - How to use GitHub in less than 3 mins"](https://www.youtube.com/watch?v=qT8ut3EaIpM&t=4s) by CTG on Youtube to do this.

Now I need to start learning how to use Godot. I watched this [video](https://www.youtube.com/watch?v=G64gMZdWPv4) by nikich which is only part one of his Godot beginner tutorial.

First I learned the concept of scenes and nodes. Scenes are like a container to hold nodes. Nodes are the things stored in the scene. For example you can have a scene to represent a player character which would holds nodes for the appearnce of the character or the animations for it.

##### Example from video
![alt text](imgs/ll1_1.png)

Speaking of characters I learned how to make a basic character.

First I created a new scene called main and then added a child node called player.

![alt text](imgs/ll1_2.png)

Then I created a asset folder and pasted an image that would represent the player charcter. I created a new sprite node as a child of the player node and assigned the image to it.

![alt text](imgs/ll1_3.png)

Now we have to write script to make the player move. But first I needed to learn GDscript.

GDscript is a programming language made for Godot and is similar to Python.

First I learned how to make variables and functions. Variables are used to store data and functions are used to group code together to be reused later.

```java
func _hello_world()->void: // void means this function does not return anything
    var my_variable = "Hello World" // Creates var
    print(my_variable) // prints var to console
```

The output of this code would be "Hello World" printed to the console.

It's also good to specify the type of data a variable will hold.

For numbers you can use int or float. Int is for whole numbers and float is for decimal numbers. And for words you can use String.

```Java
func _hello_world()->void: /
    var my_variable:String = "Hello World"
    print(my_variable)
```

Example of function with parameters and return type

```Java
func sum_numbers(num1:int, num2:int)->int: // the stuff in the () are parameters and the ->int means this function returns an int
	return num1 + num2

var result = sum_numbers(5, 10) // result will be 15

print(result)
```
How this works is when you call the function sum_numbers and pass in two numbers, it will add them together and return the result.

Now we will get the player model to move to the right side

First we need to understand how movement works on a 2d plane. On the x axis, moving right increases the x value and moving left decreases it. On the y axis it's different from what we learn in math class, moving down increases the y value and moving up decreases it.

![alt text](imgs/ll1_4.png)

To move the player to the right I would have to increase the x value of the player node.

```Java
func _physics_process(delta: float) -> void:
	position.x+=50*delta // move right 50 pixels per second
    // same as position.x = position.x + 50*delta
```
The _physics_process is a built in function that runs every frame. The delta parameter is the time it took to complete the last frame. This is used to make sure the movement is consistent regardless of the frame rate.

The position variable is a built in variable that holds the position of the node. So by increasing the x value of the position variable, we are moving the player to the right.

If we wanted to move the player down we would increase the y value of the position variable.

```Java
func _physics_process(delta: float) -> void:
    position.y+=50*delta
```

![alt text](imgs/ll1_5.png)

For today I just got some exposure to Godot and learned how to use GDScript to make a basic character model move. Later on I will explore more ways to use Godot.

### 11/1/25

For today I just learned how to put text or labels into my scene.

First I clicked this `+` button at the top left to add a new node.

![alt text](imgs/ll2_1.png)

Then I searched for "Label" and added it to my scene as a child of the main node.

![alt text](imgs/ll2_2.png)

Now I can change the text of the label by selecting it and changing the "Text" property in the inspector on the right. For this I just changed it to "Hello World".

I also moved the label by clicking and dragging it in the scene view.

![alt text](imgs/ll2_3.png)

Lastly I changed the color of the text to green by editing the `Theme Property font_color` in the inspector.

![alt text](imgs/ll2_4.png)

Today I didn't get to do too much and just learned how to add text to my scene. Hopefully I could explore some cooler features like building the background of a game or maybe having user input to move the player around.

11/11/2025
First I downloaded this starter [assest pack](https://github.com/gdquest-demos/godot-3-beginner-2d-platformer/releases/tag/1.1.0) for  2D platformer game.

### X/X/XX:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
