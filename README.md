

![image](https://user-images.githubusercontent.com/82111543/217303951-9051f2db-fa18-413d-8f09-2a98c8943b0a.png)

<img width="1175" alt="PHIlosophers" src="https://user-images.githubusercontent.com/82111543/218946249-ca9dd1ea-e2f1-4939-aaa7-52d107a35f30.png">


This project taught us about how to use threads using the classic example of the dining philosophers. We had to write a program that would allow the philosophers to eat, sleep and think in a cycle. To eat a philosopher requires two forks (chopsticks). Each philosopher is a thread . To protect any data that may be accessed by more than one philosopher we had to use mutexes. This prevents data races. To avoid dying philosophers we used scheduling. If the number of philosophers is even ; odd and even philosophers can take turns. Here to prevent deadlock we made sure each philosopher took the fork(chopstick) with the lower number first so both the first and the last philosopher reach for the first chopstick and only check for the next (second chopstick for philosopher one and last chopstick for  the last philosopher) if they are able to acquire the first chopstick. Similarly the other philosophers do not look for a second fork if they can't get the first one they need preventing a deadlock. We also need to deal with greedy philosophers by making sure the same philosopher doesn't eat again just after it already ate. For this I used an array that stored the ID of the last philosopher that used the fork and made sure that philosopher could not take that fork again until another philosopher had used it first.
See the video of how the philosophers continue to eat, sleep and think without dieing.


https://user-images.githubusercontent.com/82111543/221136170-87157e92-cace-479a-b47f-efb10e7866da.mov

