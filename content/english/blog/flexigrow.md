---
title: "FlexiGrow: LLM GPT4-based Intelligent Deformable Plant Pet"
meta_title: ""
description: "this is meta description"
date: 2023-12-01T05:00:00Z
image: "/images/grow/10.jpg"
categories: ["Projects"]
author: "Team"
tags: ["Product design"]
draft: false
---

Recognizing the growing trend of individuals desiring companionship but lacking the time and effort to care for traditional pets, there is an increasing interest in plants as suitable substitutes. Similar to animals, plants require water, food, and sunlight to thrive and grow, prompting our initiative to create an intelligent 'pet plant pot'. We seek to cater to the evolving needs of plants throughout their life cycle, fostering a more convenient and fulfilling indoor gardening experience.

{{< video src="images/growvideo.mp4" width="100%" height="auto" autoplay="false" loop="false" muted="false" controls="true" class="rounded-lg" >}}


### 1. Design Process

#### 1.1 Ideation
{{<image src="images/grow/idea.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

#### 1.2 Prototypes
##### *Expandable Structure*
{{<image src="images/grow/process.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
The expandability of the left structure is limited to a single dimension. As it extends horizontally, its vertical height diminishes, posing a drawback for its suitability as a plant pot. The right structure has the capability to expand in both vertical and horizontal directions. Additionally, its reduced need for folding simplifies the task of finding a suitable material for its construction.

##### *Material*
{{<image src="images/grow/3.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
Initially, we conducted experiments with cardboard and chipboard, utilizing a laser cutter to score the pattern and facilitate folding. However, the challenge arose when attempting to create folding marks on both sides of the cardboard and ensuring precise alignment in two directions simultaneously. This complexity made the folding process arduous and increased the risk of breakage. Subsequently, we explored 3D printing, but encountered issues as the folding marks consistently cracked after several attempts.

{{<image src="images/grow/4.jpeg" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
Subsequently, we opted to experiment with attaching the triangular pieces to a piece of fabric using glue. We affixed the pieces to a sheet of paper, and then pinned them up to assess the effectiveness of this approach.
{{<image src="images/grow/6.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-2/3 img-fluid" title="image title"  webp="false" >}}
{{<image src="images/grow/7.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-2/3 img-fluid" title="image title"  webp="false" >}}

##### *Overall Form*

Before designing our mobile plant pet, we identified several design requirements:
1. It can carry the deformable pot, and can adapt to different pot sizes;
2. It is leakable and can receive water;
3. Adding a wheeled base to create a mobile garden;
4. It has a hanging rope so users can pull around when hanging out;
5. The top can place a mobile phone, and the mobile phone screen can show the expressions, the camera can accurately capture the plant.

{{<image src="images/grow/5.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

Then, we started brainstorming ideas and solutions to achieve all of them. Given that our pet needs to have long necks to carry the phone, we came up with multiple ideas for huskies, giraffes, flamingos, small dinosaurs, etc., and did some quick prototype iterations with cardboard. In the process, we and the teachers all thought that the appearance of the animal and the flower pot was inconsistent, lacking unity, and we felt that they were two separate designs. Therefore, in the end, we chose to use the image of a dinosaur, and at the same time added a triangular decorative pattern, which is consistent with the flower pot in color and form.

{{<image src="images/grow/9.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

After the general shape was determined, we designed and iterated on the details. The position and angle of the mobile phone, the shape of the dinosaur, the position and size of the deformable pot, the fixed wheel, the movable design of the tail, and so on. We encountered many difficulties but solved them again and again.

{{<image src="images/grow/8.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}

In all, this approach transforms the flower pot into a pet-like companion that can be 'walked' around and brings a touch of humor and creativity to everyday gardening activities. The mobility of the pots allows for easy adjustment to ensure optimal light exposure, addressing issues of insufficient sunlight, and moving plants to different locations can promote better growth and health by providing varied environmental conditions.


### 2.Daily Care AI System

FlexiGrow has an advanced AI-powered plant care system. The system is based on cutting edge LLM GPT4 and a powerful image processing model and the overall working flow is:

{{<image src="images/grow/18.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-2/3 img-fluid" title="image title"  webp="false" >}}

We build a interface page after in-context learning to use for demo and will be integrated into hardware in the future. And all information it needed is just a picture of plant. Within seconds, FlexiGrow performs an image analysis and generates intelligent recommendations based on advanced AI models.

{{<image src="images/grow/14.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="w-2/3 img-fluid" title="image title"  webp="false" >}}

After input the image, FlexiGrow firstly accurately identifies the plant species. Following this, the system evaluates the current health of the plant and the advice for this plant which includes suggestions on watering, lighting, and soil care, specific to the type of plant in question. Lastly, FlexiGrow enriches your plant-care experience with fun facts, adding joy to your interaction with your green companions. 

And the status could be expressed by the pet with different emotions! With the help of LLM, it has a remarkable precision on predicting species and advice, surpassing the capabilities of most humans.

{{<image src="images/grow/15.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
{{<image src="images/grow/16.png" caption="" alt="alter-text" height="" width="" position="center" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}