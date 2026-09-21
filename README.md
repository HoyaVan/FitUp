# FitUp App (Comp 2800 - BBY29)

**Live Demo:** [https://fitupapp.onrender.com](https://fitupapp.onrender.com)
**Testing Plan:** [Google Sheets Link](https://docs.google.com/spreadsheets/d/10ylqpRkL9dYpFuuqNc5xzxkXSeOpcru4Y1LLDA1xn7o/edit#gid=394496370)

> **Empower your fitness journey with FitUp!** A smart, AI-driven app offering personalized tasks, real-time progress updates, and nutrition recommendations to help you achieve your goals alongside friends.

## 📖 About The Project

FitUp is designed for users across all fitness levels, from beginners to advanced professionals. We motivate users to exercise by assigning suitable, achievable tasks personalized to their interests and fitness levels. To make fitness fun, users earn points by completing tasks, which can be used to compete with friends on the leaderboard or make purchases in the Point Shop.

**Key Features & AI Integration:**
* **AI Chat:** Built-in speech recognition allows for seamless communication with an AI assistant.
* **Smart Planning:** Generates personalized training and diet plans.
* **Pose Detection:** Real-time feedback using pose detection technology to help correct form and posture, enhancing workout performance.
* **Smart UI:** Optimized for iPhone 14 Pro Max screen sizes to deliver a premium user experience.

---

## 👥 The Team

| Name | Contact Email |
| :--- | :--- |
| **Declan Joyce** | declan.daniel.joyce@gmail.com |
| **Davin Higo** | davinhigo@gmail.com |
| **John Guo** | johnguoyh@gmail.com |
| **Linh Hoang** | linhoang.ce@gmail.com |
| **Yuho Lim** | dbgh7894@gmail.com |

---

## 💻 Tech Stack & Resources

| Category | Technologies & Tools |
| :--- | :--- |
| **Frontend** | HTML, CSS, JavaScript, Bootstrap 5.0, THREE.js, Blender, Tensorflow MoveNet |
| **Backend** | Node.js |
| **BaaS & APIs** | MongoDB, Cloudinary, Google Speech APIs, Google Maps API, GroqCloud |
| **AI Models** | Groq (Mistral AI) for Chatbot, Tensorflow for Body Tracking, ChatGPT (Dev assistance) |

**Asset Acknowledgements:**
* **Leaderboard Design:** [MalunariDev Codepen](https://codepen.io/MalunariDev/pen/RweGGxx)
* **Main Icons:** [Strange Icons](https://www.strangeicons.com/)
* **CSS Loading Animation:** [CSS Loaders](https://css-loaders.com/dots/)
* **Exercise Source (Bench Press):** [Fitness Programmer](https://fitnessprogramer.com/exercise/bench-press/?pw=75448)

---

## 🚀 Getting Started

### Prerequisites
Before running the application, ensure you have an `.env` file in the root directory. You will need a Google Maps API key for the community features. 

Required environment variables:
`GROQ_API_KEY`, `PORT`, `MONGODB_SESSION_SECRET`, `NODE_SESSION_SECRET`, `MONGO_URI`, `APP_PASSWORD`, `APP_EMAIL`, `GOOGLE_API_KEY`, `CLOUDINARY_CLOUD_NAME`, `CLOUDINARY_API_KEY`, `CLOUDINARY_API_SECRET`

### Installation
1. Download or clone the project folder.
2. Open a terminal and navigate to the root directory.
3. Install dependencies and start the server:
```bash
npm i
node index.js
```

---

## 📱 How to Use

* **Account Management:** Start by signing up or logging in from the landing page. Forgot your password? Use the "Reset Email" option. Once logged in, you can update your profile picture, username, email, and password, or view your rank progress.
* **Task Management:** The main page displays your personalized tasks. Click on a task to view details, mark it as done to earn points, or reroll it if you want a different challenge.
* **Point Shop & Leaderboard:** Spend your earned in-app currency in the shop on task rerolls or gift cards. Compete on the leaderboard to reach the top 5 for additional rewards!
* **AI Features:** Ask the AI chatbot questions using text or voice. Get a personalized workout recommendation via a body scan, and use the AI camera to get coached on proper workout posture.
* **Community:** Visit the community page to share updates and view posts from other users.

> **🎮 Easter Egg:** On the landing, login, or signup pages, input the famous Konami code using your arrow keys: `Up, Up, Down, Down, Left, Right, Left, Right, B, A`. If entered correctly with no other inputs, Mario will jump across your screen!

---

## 🛠️ Known Bugs & Limitations

* **Navigation Buttons:** Some navigation buttons may not be fully functional yet; they are currently implemented to represent the concept and enhance UI design.
* **AI Chat Limitations:** We kept the AI implementation simple (no custom dataset training). Due to project scope limitations, we could not implement long-term chat history storage.

---

## 🔮 Future Roadmap

* **MoveNet Training:** Further train the MoveNet model for pose detection to provide even more accurate real-time feedback on user posture and form during exercises.
* **Advanced AI Tasks:** Allow AI to fully generate dynamic, on-the-fly tasks based strictly on fluctuating user fitness levels and real-time interests.
* **Accessibility Enhancements:** Implement comprehensive Text-to-Speech audio streaming for the chat and workout recommendations to better assist users with vision impairments or those who prefer hands-free guidance while working out.

---

## 📁 File Structure

```text
│   .env
│   .gitignore
│   databaseConnection.js
│   index.js
│   package.json
│   README.md
│   utils.js
│
├───.vs
│   │   ProjectSettings.json
│   │   slnx.sqlite
│   │   VSWorkspaceState.json
│   │
│   └───BBY-29
│       ├───config
│       │       applicationhost.config
│       │
│       ├───FileContentIndex
│       │       4289698b-b92c-42df-9ca9-12259ee516ac.vsidx
│       │       5d0b990f-d8d4-4b08-9da9-b637923eae58.vsidx
│       │       95b680c3-3183-424d-94d0-4192e2929250.vsidx
│       │
│       └───v17
│               .wsuo
│               DocumentLayout.json
│
├───html
│       ai-training-camera-feed.html
│       ai-training-female-body-scan-result.html
│       ai-training-female-body-scan.html
│       ai-training-male-body-scan-result.html
│       ai-training-male-body-scan.html
│       ai-training-questions.html
│       ai-training-recommendation.html
│       ai-training-scan-request.html
│       aichat-loading.html
│       aichat-log.html
│       body-motion-capture.html
│       map.html
│
├───img
│   │   [Various Image, GIF, MP4, and MP3 files]
│   │
│   └───text-to-speech-audios
│           [Various MP3 output files]
│
├───scripts
│       ai-training-camera-feed.js
│       ai-training-female-body-scan-result.js
│       ai-training-female-body-scan.js
│       ai-training-male-body-scan-result.js
│       ai-training-male-body-scan.js
│       ai-training-questions.js
│       ai-training-recommendation.js
│       ai-training-scan-request.js
│       aichat-loading.js
│       aichat-log.js
│       audio-streaming.js
│       authentication.js
│       body-motion-capture.js
│       dietTasks.js
│       fitTasks.js
│       main.js
│       map.js
│       speech-to-text.js
│
├───styles
│       [Various CSS files]
│
└───views
    │   403.ejs
    │   404.ejs
    │   admin.ejs
    │   changeEmail.ejs
    │   changePassword.ejs
    │   changeUsername.ejs
    │   community.ejs
    │   communityPost.ejs
    │   dietTasks.ejs
    │   fitTasks.ejs
    │   index.ejs
    │   login.ejs
    │   main.ejs
    │   profile.ejs
    │   rankProgress.ejs
    │   reset-email.ejs
    │   reset-password.ejs
    │   shop.ejs
    │   signup.ejs
    │
    └───templates
            easteregg.ejs
            end.ejs
            footer.ejs
            header.ejs
            headerOld.ejs
            image.ejs
            item.ejs
            taskFooter.ejs
            user.ejs
```
