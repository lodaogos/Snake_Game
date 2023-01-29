# **Snake Game**
Learning html, javascript, and css by making a snake game. i followed Bro Code tutorial on [youtube](https://youtu.be/Je0B3nHhKmM) all credits to him. While playing around with the code, i managed to fix some bug i found in the code. The fixes will be shown below the game overview. I changed the game a little bit so that there is no border. Everytime the snake is touching the border of the game, it will automatically teleport the snake to the opposite of the border. Like the image below.
![image](https://user-images.githubusercontent.com/115076652/215307250-31e7ccda-0d8c-4e26-933e-eabb5ca6f9d9.png)


## **Game Overview**

### Game Start
The game will automatically start after you copy the html file path to the browser. You can move the snake by using arrows key. The objective is to eat the apple (the red block) and to get highest score as possible.
![image](https://user-images.githubusercontent.com/115076652/215306272-200b439d-698d-4c62-9785-5943e924f755.png)


### Playing The Game
Your snake will get bigger as you it more apple.
![image](https://user-images.githubusercontent.com/115076652/215306344-b65ec23f-d91c-4727-b5c2-b093baf4611c.png)


### Game Over
As your snake gets bigger, you should be careful to not eat yourself. If you do, the game over text will pop up and the game will stop. You can restart the game by pressing the reset button.
![image](https://user-images.githubusercontent.com/115076652/215306414-3d9a23dc-5e30-42b7-989b-7042031abad6.png)


## Some Bug I Found In The Bro Code Tutorial Snake Game Code
### Bug 1
Everytime you press reset, the speed of the snake increase. This has something to do with how the setTimout method works. In order to fix that, i created a global variable and assign the variable in the nextTick function. After that, i can clear it everytime the game reset.
![image](https://user-images.githubusercontent.com/115076652/215307005-dbf7a9dc-18cd-4046-a96a-0b102006b311.png)

![image](https://user-images.githubusercontent.com/115076652/215307058-da0a66cc-6e16-463a-8cb6-5a343576d15b.png)

![image](https://user-images.githubusercontent.com/115076652/215307013-e0748f70-24ce-4d2e-976b-b018476f3786.png)

### Bug 2 
Sometimes the food will spawn inside the snake body. In order to fix that, we simply need to check if the createFood function created the foodX and foodY coordinate inside the snake body. If it is, we call the createFood function again. This implementation is definitely not the greatest, there could be a worst case possibility where the createFood function keep spawning the food inside the snake body. But this works for now at least.
![image](https://user-images.githubusercontent.com/115076652/215307179-4b484923-47e2-4480-9bc1-1d2bf2845521.png)

![image](https://user-images.githubusercontent.com/115076652/215307185-1e1ebbfb-8f8f-4156-8bac-cbbb5de6ffd2.png)

### Bug 3 
You can actually press the button fast enough so that the game will think that the snake is eating itself (a bit hard to explain by words).
![image](https://user-images.githubusercontent.com/115076652/215307368-55918f41-53bf-4821-900b-389c4c9b776d.png)
In this image, the snake is going right. If you press down and then left fast enough. The game will actually think you are moving left.
![image](https://user-images.githubusercontent.com/115076652/215307445-3e2124f6-1fb0-4ccf-b933-6e8d9b6843cf.png)
I think this has something to do with how actionListener is instant and the game itself are programmed to run a check every 100 ms.

Well we can fix it by using some variable that will tell are we allowed to take input right now or not.
![image](https://user-images.githubusercontent.com/115076652/215307483-57788934-dca6-45ad-b04c-25a2a0e63e70.png)

![image](https://user-images.githubusercontent.com/115076652/215307486-7630818c-260d-411e-bf1e-0d34b88f547c.png)

![image](https://user-images.githubusercontent.com/115076652/215307492-1351b8d7-5b92-4fac-9a60-45c4feb0dffa.png)

This will fix the bug






