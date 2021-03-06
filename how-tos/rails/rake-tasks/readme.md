# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Custom Rake Tasks

<img src="http://cdn.meme.am/instances/400x/58907263.jpg">

## Why?

"Rake enables you to define a set of tasks and the dependencies between them in a file, and then have the right thing happen when you run any given task. Each task may be either one of the built-in types, or a block of your own Ruby code. It was originally created to handle software build processes, but the combination of convenience and flexibility that it provides has made it the standard method of job automation for Ruby projects." --Stuart Ellis

* Creating custom rake tasks help companies and developers better automate activities that are needed to improve the maintenance and performance of a website.

## How?

1. To check all of the rake tasks available to you in the Terminal:

```cli
rake -T
```

2. To create a custom task file, you can go into your Terminal and run:

```cli
touch lib/tasks/<FILE NAME>.rake
```
**Note:  You will want to name the file with .rake in order to allow Rails to look for it.  You will be able to write all of your code using standard Ruby conventions**

3. You will see a custom task written with these three elements:

  * A description
  * The name that identifies the task
  * The code to be executed by the task

```rb
desc "Rocky looks for Adrian after facing Creed"
task :yo_adrian => :environment do
  puts "Yo Adrian! I did it!!!"
end
```

4. To run this task you can simply type:

```cli
rake yo_adrian
```

which should output:

```cli
Yo Adrian! I did it!!!
```

You can add as many tasks as you want into the same file. Doing so will help with your organization of the code.

## Demo

Note: Feel free to watch a demo of how to implement a custom rake task. The resources below will be a definitive guide for you as you begin to construct your own tasks in your applications.

**Let's imagine that we have a database of users.  Some users have expired accounts while others don't.  We need to create a task that will send an alert regarding expired accounts.**

### Resources

* <a href="http://www.stuartellis.eu/articles/rake/" target="_blank">Using Rake to Automate Tasks</a>
* <a href="http://edelpero.svbtle.com/everything-you-always-wanted-to-know-about-writing-good-rake-tasks-but-were-afraid-to-ask" target="_blank">Everything You Always Wanted to Know About Writing Good Rake Tasks</a>
* <a href="https://www.youtube.com/watch?v=RS1juns_Sj0" target="_blank">RailsCasts - Custom Rake Tasks</a>
* <a href="https://www.youtube.com/watch?v=B1E6dyRZWdg" target="_blank">How to create a Rails Rake Task</a>
