# **Snake Game**
Learning html, javascript, and css by making a snake game. i followed BroCode tutorial on [youtube](https://youtu.be/Je0B3nHhKmM) all credits to him. While playing around with the code, i managed to fix some bug i found in the code. The fixes will be shown below the game overview. 

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


## Some Bug I Found
### Bug 1
Everytime you press reset, the speed of the snake increase. This has something to do with how the setTimout method works. In order to fix that, i created a global variable so that i can clear it everytime the game reset.
![image](https://user-images.githubusercontent.com/115076652/215307005-dbf7a9dc-18cd-4046-a96a-0b102006b311.png)
![image](https://user-images.githubusercontent.com/115076652/215307013-e0748f70-24ce-4d2e-976b-b018476f3786.png)




