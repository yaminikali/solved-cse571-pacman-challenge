Download Link: https://assignmentchef.com/product/solved-cse571-pacman-challenge
<br>
In this project, you compete against another pacman agent. Your goal is to eat the other pacman before it eats you. Each agent has two possible states: normal and angry, depicted by a yellow and red pacman. Whenever both agents are in the same state, they can freely cross each other. If one is angry and the other is in its normal state, the angry agent will eat the normal agent and win the game.

To reach an angry state, you need to eat a capsule that allows you to maintain the angry state for some amount of time.

<h2>1.2         Your Task</h2>

In this project, you need to implement a pacman agent in <em>CompetitiveAgents.py</em>. In the current state, this file contains a simple agent that is controllable with your keyboard. Unless explicitly stated, you are not allowed to make changes to the other files related to the project. The most important function of your agent is <em>getAction(…)</em>, that provides you with the agents current perception of the world and requires you to return its next action. It will be called by the game to get your next action and needs to return one of the five actions (Stop, North, East, South, West).

Besides the mentioned restrictions, you can implement what ever you have learned in this years lecture (and beyond) to be victorious in this challenge.

You can test your agent on the two maps <em>competitive1 </em>(many loops) and <em>competitive2 </em>(many dead ends), or create your own map. You can set the map with the <em>-l </em>parameter when running pacman.py. Feel free to use numpy, scipy or tensorflow if you think your agent benefits from it.

<h2>1.3         Running the Code</h2>

Since the challenge requires two agents, you need to start two instances of pacman.py. Each pair needs one server and one client. After a game is resolved, both instances will shut down. Here is how to run the code:

<ul>

 <li>Server: python pacman.py -s</li>

 <li>Client: python pacman.py –remote ip 127.0.0.1</li>

</ul>

The remote ip is the IP of the computer on which the server is running. We encourage you to talk to other groups to test your agents. To do this, just set the IP to the address of the computer that runs the server.

<h2>1.4         The rules of the World</h2>

<ul>

 <li>Capsules are a never ending recourse that can be found at certain locations on the map. When ever you eat a capsule, another capsule will appear somewhere on the map.</li>

 <li>You will always know the layout of the map, but you will only have current information of the variable items (the other agent and capsules) within a radius of 12 fields around your agent. For debugging</li>

</ul>

1

CSE571: Artificial Intelligence                                                                                                                                    Fall 2017

purpose, we are always rendering the full state of the world on your screen, but the state that is offered to your agent is limited, as described above (you can simply print(observations) to see an ascii representation in your terminal).

<ul>

 <li>The agents will take a single action in an alternating manner. The servers agent will take the first action.</li>

 <li>We will observe how long your agent takes to start and to make a turn. Your agent should decide for its first action in under 30 seconds and all subsequent actions in under 3 seconds.</li>

 <li>Your agent needs to be some kind of rational agent to be allowed in the challenge (entirely random agents are not allowed).</li>

 <li>An agent is considered aggressive, whenever the variable ’angryTimer’ in its state is greater than 0.</li>

</ul>