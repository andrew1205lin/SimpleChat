# SimpleChat
A simple chat app with firebase.

## Spec

### Chatroom page
Chat with other user.

![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/bfc6b64a-c57d-435e-b5a2-057659939384)

- Mainly handled by ChatActivity.
- Storing the Chatroom related state variables in Firebase with ChatroomModel.
  Including chatroomId, userIds, lastMessageTimestamp, lastMessageSenderId, lastMessage.
- Storing the ChatMessag related variables in Firebase with ChatMessageModel.
  Including message, senderId, timestamp.


## Other features

### Recent chatrooms page
List out the recent chatrooms. Click on any of them to enter the corresponding chatroom page.

![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/07d7e433-998c-41e1-a06a-f3d5f84daa2a)

- Mainly handled by ChatFragment, RecentChatRecyclerAdapter:

### Profile page
Check and change the user name and profile image here.

![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/ec2056e0-9157-4c7c-b3c0-9922d2065489)

- Mainly handled by ProfileFragment.
- Using ImagePicker to choose image from device.
- Storing the image in Firebase cloud storage.



### Search user page
Allow us to find the user we have never chatted with and initiate a chatroom with them.

![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/b93f40ab-8afa-414f-9a6c-8339ab97c45e)

- Mainly handled by SearchUserActivity.
- Retreiving other users' profile from Firebase.

### Log in page
Use phone number and OTP as the authentication.

![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/6c52d8f1-4dc8-4944-b88c-b7916ddfa28a)
![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/40adba02-87eb-4592-9b05-a3be63432420)
![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/f4dfa5eb-a13e-4b2d-b4a5-cee7d4607be3)


- Mainly handled by Login*Activity.
- Enter phone number => Enter OTP => Set user name

### Notification
If other send message to you while the APP is closed, the app would send notification.
We can click on the notification and directly open the Chatroom page.

![image](https://github.com/andrew1205lin/SimpleChat/assets/61780524/142ff081-6ac0-4917-8fb4-647508cf0b01)

- Mainly handled by ChatActivity.
- Using OkHttpClient to send request to https://fcm.googleapis.com/fcm/send




