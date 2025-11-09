# Entry 1
##### 11/3/25

### Context
In my APCSA class we started to work on our Freedom Project. For the Freedom Project I had to choose a tool to help me create whatever I wanted.

### Idea
For my Freedom Project I want to make a game where the objective is to sneak snacks into your room without getting caught by your parents. The player would have to sneakily get to the kitchen but there will be things that make noise to alert the parents like creaky floor boards or grabbing the snack. If the parents touch your character model or maybe if they see you, you lose. This game is inspired by my own experience of getting snacks late at night without waking up my parents.

The tool I chose to use was [Godot](https://godotengine.org/) because it's a powerful game engine that allows for 2D and 3D game development, and it's free and open-source.

I also considered using [Unity](https://unity.com/), but I think Godot seems more beginner-friendly for my first game project, and also I won't have acess to all of Unity's features without a paid subscription.

### Learning my tool

First thing I did was download Godot and import it into github. I did this by creating a new project on Godot then using Github desktop to add the project folder into a new repository and published it to github. Then I cloned the Godot repo into my Freedom Project folder in my IDE. I watch the video ["Godot 4 - How to use GitHub in less than 3 mins"](https://www.youtube.com/watch?v=qT8ut3EaIpM&t=4s) by CTG on Youtube to do this.

Now I need to start learning how to use Godot. I watched this [video](https://www.youtube.com/watch?v=G64gMZdWPv4) by nikich which is only part one of his Godot beginner tutorial.

First I learned the concept of scenes and nodes. Scenes are like a container to hold nodes. Nodes are the things stored in the scene. For example you can have a scene to represent a player character which would holds nodes for the appearnce of the character or the animations for it.

##### Example from video
![alt text](../tool/imgs/ll1_1.png)

Speaking of characters I learned how to make a basic character.

First I created a new scene called main and then added a child node called player.

![alt text](../tool/imgs/ll1_2.png)

Then I created a asset folder and pasted an image that would represent the player charcter. I created a new sprite node as a child of the player node and assigned the image to it.

![alt text](../tool/imgs/ll1_3.png)

Now we have to write script to make the player move. But first I needed to learn GDscript.

`GDscript` is a programming language made for Godot and is similar to Python.

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

![alt text](../tool/imgs/ll1_4.png)

To move the player to the right I would have to increase the x value of the player node.

```Java
func _physics_process(delta: float) -> void:
    position.x+=50*delta // move right 50 pixels per second
    // same as position.x = position.x + 50*delta
```
The `_physics_process` is a built in function that runs every frame. The delta parameter is the time it took to complete the last frame. This is used to make sure the movement is consistent regardless of the frame rate.

The position variable is a built in variable that holds the position of the node. So by increasing the x value of the position variable, we are moving the player to the right.

If we wanted to move the player down we would increase the y value of the position variable.

```Java
func _physics_process(delta: float) -> void:
    position.y+=50*delta
```

![alt text](../tool/imgs/ll1_5.png)

For now I just got some exposure to Godot and learned how to use GDScript to make a basic character model move. Later on I will explore more ways to use Godot.

My tinking can be found in my learning log [here](../tool/learning-log.md).

### Engineering Design Process

#### Define the Problem
I want to make a game where the objective is to sneak snacks into your room without getting caught by your parents.

#### Brainstorm Solutions
* I found a game engine called Godot that I can use to make my game.
* I learned the basics of Godot and GDScript to make a basic character model move.
* I will continue to learn more about Godot and GDScript

I will still continue to brainstorm more solutions as I learn more about Godot and GDScript. Once I have a better understanding of the tool I can start to plan out the game design.

### Skills

#### Creativity
I knew I wanted to make a game for my Freedom Project but I had to come up with a unique idea. I thought about what kind of game I would like to play and came up with the idea of sneaking snacks into your room without getting caught by your parents. This idea came up randomly while I was ironically getting a late night snack.

#### How to learn
This will be a skill that I will use throughout the entire Freedom Project. I will have to learn how to use Godot and GDScript to make my game. For now I learned by watching a tutorial video on Youtube and following along. I learned that the best way to learn is by doing.

### Next Steps
My next steps are just to continue learning about Godot and considering how to implement my game idea. There's still a lot of things I need to learn about Godot before I start any planning for the game design.
[Next](entry02.md)

[Home](../README.md)
