# 🚀 Flutter Gemini Chat - Smart Scroll Challenge

This project is a solution to the Gemini Chat UI challenge. The core focus was to implement a professional, "human-like" auto-scroll behavior for streaming responses, ensuring a seamless user experience.

## 🌐 Live Demo
You can try the live application here:
[👉 Click to open Live Demo](https://mahmoudmohameddev1.github.io/chat-scroll-challenge/)

---

## 🛠️ Solutions Implemented
I have successfully addressed all 4 required scenarios using a custom `ScrollController` logic combined with `NotificationListener`:

1.  **Smart Auto-Scroll**: The view automatically scrolls to the bottom as long as the user is not manually inspecting previous messages.
2.  **Manual Scroll Detection**: Auto-scroll pauses instantly if the user scrolls up (manual intervention).
3.  **Forced Reset on Send**: Sending a new message resets the scroll state and forces a jump to the bottom to focus on the new conversation.
4.  **Auto-Resume**: If the user manually scrolls back to the bottom while a stream is active, the auto-scroll resumes automatically.

## 🏗️ Technical Highlights
- **Threshold Logic**: Used a 100px threshold to determine if the user is "at the bottom" to prevent jerky scroll behavior.
- **Scroll Direction Awareness**: Implemented `NotificationListener<UserScrollNotification>` to distinguish between system-driven and user-driven scrolling.
- **Smooth UX**: Used `Curves.easeOut` with a 250ms duration for all programmatic scrolls to mimic premium chat apps like Telegram.

---

## 📹 Scenario Recordings (Proof of Work)
| Scenario | Description | Link |
| :--- | :--- | :--- |
| **Scenario 1** | Basic Auto-Scroll during stream | [https://drive.google.com/file/d/1VEzoN0icV-bPhqCZD1HrCkxDwCBQ-O32/view](#) |
| **Scenario 2** | Pause on Manual Scroll | [https://drive.google.com/file/d/15eRb4ty4-phCqLIIvivH81aixa_BMfnt/view](#) |
| **Scenario 3** | Force Scroll on Send | [https://drive.google.com/file/d/1Ijk8SGqRoDxVA-6-BQ4oze-Tjs8ZZ8oS/view](#) |
| **Scenario 4** | Resume Auto-Scroll | [https://drive.google.com/file/d/1-13vQjrZwRIEJ6JLOQ-Xmg12YbyBv_dt/view](#) |


---

## 🚀 How to Run Locally
1. Clone the repo: `git clone [https://github.com/mahmoudmohameddev1/chat-scroll-challenge]`
2. Install dependencies: `flutter pub get`
3. Run the app: `flutter run`
4. Enter your Gemini API Key in the UI to start chatting.