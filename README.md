# SimpleChat
A simple chat app with firebase.

## Spec

### Chatroom page
Chat with other user.

- Mainly handled by ChatActivity.
- Storing the Chatroom related state variables in Firebase with ChatroomModel.
  Including chatroomId, userIds, lastMessageTimestamp, lastMessageSenderId, lastMessage.
- Storing the ChatMessag related variables in Firebase with ChatMessageModel.
  Including message, senderId, timestamp.

## Other features

### Recent chatrooms page
List out the recent chatrooms. Click on any of them to enter the corresponding chatroom page.

- Mainly handled by ChatFragment, RecentChatRecyclerAdapter:

### Profile page
Check and change the user name and profile image here.

- Mainly handled by ProfileFragment.
- Using ImagePicker to choose image from device.
- Storing the image in Firebase cloud storage.

### Search user page
Allow us to find the user we have never chatted with and initiate a chatroom with them.

- Mainly handled by SearchUserActivity.
- Retreiving other users' profile from Firebase.

### Log in page
Use phone number and OTP as the authentication.

- Mainly handled by Login*Activity.
- Enter phone number => Enter OTP => Set user name

### Notification
If other send message to you while the APP is closed, the app would send notification.
We can click on the notification and directly open the Chatroom page.

- Mainly handled by ChatActivity.
- Using OkHttpClient to send request to https://fcm.googleapis.com/fcm/send




