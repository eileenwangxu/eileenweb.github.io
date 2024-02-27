---
title: "Intelligent Frit Pattern Industrial Design Software for Vehicle Glass"
meta_title: ""
description: "this is meta description"
date: 2023-07-01T05:00:00Z
image: "/images/flower/flower1.png"
categories: ["Projects"]
author: "Team"
tags: ["Software design"]
draft: false
---
I am the main developer of the project. We proposed an automated design algorithm based on dynamic relaxation constraints, and reduced the design cycle from 2 weeks to 20 seconds. This work has been authenticated by Chinese Institute of Electronics.

### 1. Background
The periphery of a car's windshield is often printed with neatly arranged black dots, serving multiple purposes such as blocking sunlight, protecting the windshield, and enhancing the aesthetic appeal of the car's glass edges. With the advent of an era emphasizing product personalization, the aesthetic value of dot patterns has become a focus of increasing interest. To design more visually appealing dot arrangements, designers need to optimize the placement of these dots based on the basic requirements proposed by the original equipment manufacturers (OEMs). However, this manual filling method tends to have long cycles, with some designs undergoing revisions more than a dozen times, significantly reducing the efficiency of marketing departments.

{{<image src="images/flower/f1.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-2/3 img-fluid" title="image title"  webp="false" >}}
{{<image src="images/flower/f2.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-2/3 img-fluid" title="image title"  webp="false" >}}

Through discussions with engineers, it was identified that the inefficiency of manual methods primarily stems from: 
1. The excessive number of dots on a single piece of glass, resulting in prolonged design and revision cycles for designers; 
2. Manual operations can only adjust the size, position, and number of dots in localized areas, often failing to maintain the integrity of the pattern distribution; 
3. The complexity and variety of glass models make it difficult to directly summarize manual experience into algorithmic rules.

### 2. Method and results
To meet the demands for automated dot pattern printing, the design solution aims to address the following challenges:
1. Enhancing algorithmic versatility. Given the diverse designs and requirements of automotive glass, the design process of the algorithm should maximize its scalability.
2. Improving the user interface's ease of use. The user interface should be as simple as possible to operate, reducing the learning and usage costs for users.

In nature, there are many patterns with rich borders and natural arrangements, such as butterfly wings, mycelium of fungi, and leaves of the sensitive plant. Their formation is determined by a combination of spontaneous biological cell growth and external forces. Thus, we draw inspiration from these natural processes and consider using parametric design to simulate the growth of biological cells. With minimal external force constraints, this approach allows the dot patterns to autonomously find the most suitable positions and appropriate sizes for filling. 
{{<image src="images/flower/f3.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

Compared to manual filling and rule-based filling, our force-constrained algorithm has achieved a visual effect close to that of manual filling. It effectively avoids issues such as edge detachment and unnatural gradations in transition areas, which can occur with rule-based filling.
{{<image src="images/flower/image27.gif" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
{{<image src="images/flower/f5.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

Compared to traditional manual filling solutions, the force-constrained algorithm offers distinctive advantages. The conventional manual approach involves lengthy design cycles and relies heavily on the designer's experience. It lacks objective standards for evaluating more apparent visual defects, making revisions time-consuming and costly. In contrast, using a force-constrained algorithm for parametric design allows for the establishment of constraint objectives tailored to different visual requirements, followed by computational iterations.
