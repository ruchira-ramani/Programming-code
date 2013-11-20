Programming-code
================

Aquarium Game 
Logo icon
Project 1: The Aquarium Game

This is CSE 335 Project 1. This project is a team project. There are some features your team is responsible for and some you are responsible for individually, though you should work together on interfaces. Your team should select a Step 3 solution by any one of the team members as a starting point for Project 1.

The team assignments are available on the course home page. Each team is assigned a name. Your team will be referred to by that name, i.e. Dory or Mrs. Puff. Your team name is to be include on the project web page and displayed on the project screen somewhere. You might want to consider the team name as an inspiration for your project.

There are two parts.

Part 1 is due Tuesday, October 1, 2013 **revised**
Part 2 is due Wednesday, October 16 2013 **revised**

I suggest reading this entire assignment. Your team should start discussing ideas for the game as soon as possible.

You must use SVN or GIT for source code management. Every student in CSE gets an SVN repository and a GIT repository of their own, automatically. See SVN Server for Students for details on how to use it. I have an available SVN tutorial page that is well suited to this project. If I get time, I'll create one for GIT. GIT is more complex to set up and use, but is also more powerful.

Part 1 - General Features

Part 1 is straight implementation. You are responsible for the general features as a group and individual features for each member of your group.

Notice: You have just over one week following the completion of Step 3 to complete Part 1 of the project. Each Step 3 solution must be coded individually, but you may work together on how to solve these additional requirements.

I have created the following pages that may be useful for this project:

Geometry of Scrolling
Mathematics Between Two Things
Iterators Can Be Dangerous
Dealing with Time
The CReporter Class
General Features - Team Responsibility

General features are things that the team is responsible for as a unit. You can divide the work on these features any way you like.

1. Implement scrolling. The graphics below should appear on the screen in the lower left corner and stay there even if you resize the screen. When in normal mode, your program should work exactly as it does now. When the hand is clicked on, it should go into hand-based scrolling mode. The image should change to nav2.png. Clicking on the hand again should switch back to normal mode. When in hand-based scrolling mode, clicking on the image should cause it to grab and drag. Do not let the edge of the aquarium enter the picture. In other words, if the window is 1000 pixels wide and the image is 2560 pixels wide, the possible horizontal offsets to scroll left would be 0 to 1560. You cannot drag the image so it is drawn to the right of 0 and you cannot drag is so it is drawn to the left of -1560. This is a normal behavior. You can drag, but it stops dragging when it cannot be dragged anymore.

Only the aquarium (including any fish and decor items) scrolls, not any user interface elements you may add to the screen. You should not use the scrolling features of wxWidgets. Implement your own scrolling strategy. You are free to change the parameter to functions in CItem and you will almost certainly have to.

nav1.png	nav1.png	 Normal mode navigation image
nav2.png	nav2.png	 Hand-based scrolling mode navigation image

Do not implement scrolling by changing your data. By this, I mean don't change the x,y location of an item to implement scrolling. This is a bad idea, since it changes the data to accomplish a change in the view. And, I guarantee you won't get it to work. There's too many complications involved..
In order for scrolling to be interesting, change the background image to this one. It is 2560 pixels wide. Right-click and choose Save As.. to save the file to you system.

backgroundW.png

 Collapse Expand for some suggestions about scrolling

2. Add support for the Visitor pattern for all fish and decor items. Do not try to move existing, working functionality to the Visitor pattern. It is worth changing the Count Beta Fish option as a test that this is working.

3. Create a web page and indicate on that page the team members, your individual responsibilities, and all instructions and user interface decisions.

The web page should be hosted by the CSE department servers and available as a URL. The department provides a page: Creating a Web Page with details.

4. Include an aquarium file when you turn your project part 1 in with at least 50 items.

5. Include on your web page a short preliminary description of how your Part 2 game will work. This need be only a few paragraphs, but is meant to indicate you have an early design. We reserve the right to indicate if we feel a proposed game is either too simple or too difficult (often the latter). Include a README file in your project with the address of your web page.

Turn in Part 1 via Handin. Only turn in one copy for one member of your group. Do not turn it in 3 times.

If your group has only two members

Due to drops, no-shows, and other factors, some groups may drop down to only two members. If that is that case, rather than trying to reshuffles groups to gain members, your shorted group will have decreased responsibilities:

You are not required to implement scrolling.
You should select only two individual features.
For part 2, we will expect a simpler game than we would for a larger group.
Please clearly indicate that your group had only two members in your web page.

Individual Features

Each team is responsible for completing items selected from Predators, Prey, Breeding, Environment,Treasure Chest, and Reporting. One team member should be assigned to each of these features.

You are responsible for one of the four per group member. If you have three group members, you do three options here, not all four. So, a group of three could choose to do Predators, Prey, Breeding and not do 
Treasure Chest, Environment and Reporting. Predators and Prey must be together. If a group member chooses one, some other group member must choose the other.

Notice: There are overlaps among the different features. You will have to work together to solve these problems. You will probably have to add some new fish.

Notice: we will penalize for redundant code. Many of these tasks are best completed using either base classes or the visitor pattern.

Predators

Make two fish in your aquarium predators. A predator is always on the lookout for prey. If a predator overlaps a prey, the prey is eaten and disappears from the screen. Predators should be trying to swim towards prey. If there are more than one prey, they have to choose which they swim to. The behaviors of your two predators must be different in some way. Perhaps one is very fast and the other is slower. Maybe they prefer a certain prey.

Prey

Make two fish in your aquarium prey. Prey is always trying to evade predators. If a predator overlaps prey, it is eaten and disappears from the screen. The behaviors of your two prey must be different in some way. Perhaps one is very fast and the other is slower. Maybe they prefer to school for safety.

Breeding

Two of the fish in your aquarium are capable of breeding. For these fish there must be a male and a female. Breeding fish have a period when they are not interested, then they become interested. Interested fish are attracted to other interested fish of the same type. When they overlap, the have done the deed and now the female will be pregnant. After a suitable gestation period, new fish of that type appear. How many is up to you.

Environment

You are responsible for the aquarium. Add a Care menu with options Feed and Clean. Fish grow hungry over time. When you select Feed, they are fed and will no longer be hungry. If you don't feed them eventually they die. Likewise, the aquarium gets dirty over time. When the Clean menu option is selected, it is cleaned. 
Here are three additional background images. They represent Dirty, Dirtier, and Filthy. As the aquarium gets dirtier, use the appropriate image for the background.

backgroundW1.png

backgroundW2.png

backgroundW3.png

Treasure Chest

Implement an animated treasure chest. Below are five images that can be played in sequence to create an animation:





Right click on each and do a Save As... to save the images. The treasure check should stay closed for a little while, then open using the five images.Air bubbles should then rise to the top of the tank. Stay open for a short period of time, then close, again using the five images. Here is an image for the air bubbles:



I highly recommend that you make a single class for this problem (maybe a second class for the bubbles). Do not try to swap out items for the animation. It is much easier just to tell the existing object to use a new image. Be sure you understand how the images work in CItem.

Reporting

Our tank owner is very interested in how his fish are doing. So, he want to get periodic reports. Every 30 seconds, a report should be generated that indicates:

How many of each fish type there are.
How dirty the aquarium currently is
How long it has been since the last time the fish were fed.
Are there any pregnant fish?
How many predators and prey are there?
Item 2 and 3 only applies if someone in your group is doing Environment. Item 4 only applies if someone in your group is doing breeding. Item 5 only applies if someone in your group is doing predators and prey. This part must be completed using the Visitor pattern.

If you are doing the Reporting task, use the CReporter class I have provided to display the report.

Part 2

Make me a game. Devise some strategy for the evolution of your aquarium over time. The game must have strategies for the items you chose to include. As an example, more fish may mean you have to feed more often. Maybe you are trying to balance breeding against predation. You must devise a scoring strategy so you can have a current score for your aquarium. Your should be able to list a set of rules and keep some running score on the screen of your aquarium state. If you want to, you can replace items over time with other items. Come up with your own graphics. Be creative.

You may have your aquarium game be interactive if you like, perhaps requiring clicks on the mouse to scare away predators or move fish around or you can make it a pure simulation, where you start it running and it evolves on its own over time.

In your game, each person is responsible for the code in their part. If Predators needs to ask a question of Prey, the person in charge of Prey must implement the code to answer the question. You should immediately address communications among your classes.

Consider putting your game play and strategies into a class. Do not put this code in CFrame or CAquarium.

In your final game you may remove or replace any of the behaviors from Step 3 if you wish.

Your web page must be updated by the completion of Part 2.

Notes

You are welcome to add your own graphics to the game. You are welcome to change the interface in the game. I would recommend focusing on the interaction in your game rather than significant changes in the interface, though.

Since wxImage will throw warnings of many valid images, add this line as the first line of code in CApp::OnInit():

wxLog::SetActiveTarget(new wxLogStream());
You can find information about the double-click event in the wxWidgets documentation for wxMouseEvent.

Because of the way we are using wxWidgets, it is not possible for your program to use the keyboard for arrow keys or any other commands other than as menu accelerators. You can use the menu accelerators for controls, though. For example, if I add "\tA" to the About box menu option, pressing the letter A will bring up that about box. Here's an example:

	menuFile->Append(ID_About, L"&About\tA");
Unfortunately, this will not work in a wxFrame for the arrow keys. But, you can use just about any other key this way and the arrow keys if prefixed by CTRL-, ALT-, or SHIFT-. I do recommend that you keep your interface to the mouse, though.

You may restructure how the aquarium is stored in any way you like for Part 2. Please retain the existing simple structure for Part 1.

Several tasks ask you to determine if items have overlapped. An acceptable simple way to check for overlap is to check if the center of each item is hitting the other item. This will not be true until there is significant overlap, but this behavior actually works better for this assignment.

 Logo iconCSE 335 Home Page
