---
layout: default
---

# Welcome to the <u>Mo</u>bile <u>Man</u>ipulation <u>Tu</u>torial (MoManTu). 

This is the webpage for the tutorial in the (journal to be announced). Find the overview paper here (link to open access paper provided once it is accepted) and the detailed tutorial here (dito). 

The tutorial teaches how to program a mobile robot with a robot arm to do mobile manipulation. The example systems are a [Fetch](https://fetchrobotics.com/robotics-platforms/) robot and a [Clearpath Jaca](https://clearpathrobotics.com/jackal-small-unmanned-ground-vehicle/) with a [Kinova Jaco](https://www.kinovarobotics.com/en/products/gen2-robot) attached - see the image below.

![Branching](/imgs/robots.jpg)

The videos show the demo on a real and a simulated Fetch robot.

<video width="100%" controls>
  <source src="/videos/real_fetch_web.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<video width="100%" controls>
  <source src="/videos/sim_fetch_web.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

# Docker

The easiest way to get started with playing with the tutorial is to use the provided Docker image. 
    
To pull the docker image and run the demo use:

```bash
docker run --name momantu -i -t -p 6900:5900 -e RESOLUTION=1920x1080 yz16/momantu
```

Then open a VNC client (e.g. [RealVNC](https://www.realvnc.com/en/connect/download/viewer)) and connect to _127.0.0.1:6900_. The workspaces are located in the root folder and ready to use. 

## Run MoManTu

Launch the simulator and the MoManTu software by running this command in the terminal:

```bash
roslaunch fetch_sim demo.launch
```

The pose estimation module based on NOCS, which runs under a conda environment of Python 3.5.
Activate the environment and launch the object pose estimation module with:
```bash
conda activate NOCS #activate environment
source ~/nocs_ws/devel/setup.bash
roslaunch nocs_srv pose_estimation_server.launch
```

Finally, launch the flexbe_app and robot_server node to connect other modules and start the demo: 
```bash
roslaunch fetch_sim robot_service.launch
```

# Sources

# Getting Help

# Sensor Log



Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
