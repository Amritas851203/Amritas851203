Thursday 11:09 PM
Pasted markdown(1).md
File
mera ye nhi chal raha muje  ye sahi karna h baki kuch chedna nhi h le mera code or sahi karke de 
nhi aaya yaha kuch
Today 12:30 AM
ye mere streak galat kyu dekha raha h 4 din ki ho gaee

Haan, ab screenshot se samajh aa gaya. Aapki 4-day streak GitHub profile par ho sakti hai, lekin Streak Stats card abhi 1 dikha raha hai. Iska common reason timezone mismatch hai—especially India (IST, UTC+5:30) mein late-night commits ke saath. Streak Stats documentation mein timezone parameter specifically diya hua hai, aur GitHub community mein UTC-vs-local-time mismatch ko documented limitation bataya gaya hai.

Aapke screenshot mein current date 22 Sep hai, aur card Sep 20 tak hi current streak dikha raha hai. Isliye pehle timezone fix karte hain.

Bas ye ek line change karo

Aapke README ki current streak line:

<img
  src="https://streak-stats.demolab.com/?user=Amritas851203&theme=midnight-purple&background=0d0722&ring=A970FF&fire=7C4DFF&currStreakLabel=A970FF&sideLabels=b39ddb&border=4a2080&dates=8e8e93"
  width="70%"
  alt="GitHub Streak"
/>

isko exactly isse replace karo:

<img
  src="https://streak-stats.demolab.com/?user=Amritas851203&theme=midnight-purple&background=0d0722&ring=A970FF&fire=7C4DFF&currStreakLabel=A970FF&sideLabels=b39ddb&border=4a2080&dates=8e8e93&timezone=Asia%2FKolkata"
  width="70%"
  alt="GitHub Streak"
/>

Bas &timezone=Asia%2FKolkata add kiya hai. Baaki kuch nahi badla.

Ek aur important cheez

GitHub contribution ko Streak Stats mein reflect hone mein up to 24 hours lag sakte hain.

Aur agar aapne Sep 21 aur Sep 22 ko code push kiya hai, GitHub contribution graph mein dono days green hone chahiye. Streak Stats phir un contributions ko calculate karega.

Abhi ye line change karke commit/push karo. Phir mujhe screenshot bhejna. Agar phir bhi 1 aa raha hua, main next exact fix bataungi—README ke baaki section ko bilkul touch nahi karenge.

Pasted markdown(2).md
File
esme dekhke ees part ko sahi kar ki ye time ke sath badle

Haan. Maine aapke current uploaded README ko dekha. Abhi is section mein sirf Streak Stats aur Snake hai.

Agar aapka goal hai ki aap jaise-jaise GitHub par daily contribution karein, streak automatically 1 → 2 → 3 → 4... hoti rahe, to current Streak URL mein India timezone add karna chahiye. Streak Stats officially timezone=Asia/Kolkata support karta hai.

Aap bas ye poora section replace karo
## 📊 GitHub Profile Stats

<div align="center">

<!-- GitHub Streak - Updates from GitHub contributions -->
<img
  src="https://streak-stats.demolab.com/?user=Amritas851203&theme=midnight-purple&background=0d0722&ring=A970FF&fire=7C4DFF&currStreakLabel=A970FF&sideLabels=b39ddb&border=4a2080&dates=8e8e93&hide_border=false&timezone=Asia%2FKolkata"
  width="70%"
  alt="GitHub Streak"
/>

<br/><br/>

<!-- Contribution Snake -->
<img
  src="https://raw.githubusercontent.com/Amritas851203/Amritas851203/output/github-snake-dark.svg"
  width="96%"
  alt="Contribution Snake"
/>

</div>

<br/>
Isse kya hoga?
Aaj contribution kiya → current streak update hogi.
Kal bhi contribution kiya → streak increase hogi.
4 consecutive days contribution → current streak 4 show karegi.
timezone=Asia/Kolkata ki wajah se India ke local day ke according calculation hogi.
Longest streak bhi automatically calculate hoti rahegi.
Aapka purple design same rahega.
Baaki README ko bilkul touch nahi karna.

⚠️ Ek genuine point: ye necessarily commit karte hi same second update nahi hoga. Streak Stats caching ki wajah se latest contribution reflect hone mein kuch hours lag sakte hain.

Aur Snake alag cheez hai—woh tabhi update hoga jab aapke repository mein GitHub Action us SVG ko regenerate karega. Sirf README URL se snake automatically regenerate nahi hota.

Isliye pehle upar wala section paste karke push karo. Aapki actual streak ke liye main issue ab timezone=Asia%2FKolkata wala fix hai.

kon si line se kon si tak?

Haan, aapke current code ke exact line numbers ke according:

👉 Line 261 se Line 279 tak poora section delete karo.

Yaani:

Start yahan se:

## 📊 GitHub Profile Stats

Aur delete karke yahan tak:

</div>

Jo Line 261–279 wala पूरा block hai, uski jagah maine jo replacement code diya tha woh paste kar do.

Baaki Line 280 ke baad kuch mat chhedna.

yrr mera ees line ka phale ka code de 

Haan yrr 😄 Line 261 se pehle wala code chahiye na. Ye raha exactly aapke current code ka, kuch change nahi kiya:

---

## ✨ Journey & Milestones

<div align="center">

| 🗓️ Year | 🚀 Milestone |
|:-------:|:------------|
| **2024** | 🎓 Joined B.Tech IT @ GGSIPU Delhi — where the journey began |
| ↓ | |
| **2025** | 💡 Fell in love with Full Stack Development |
| ↓ | |
| **2025** | 🚀 Founded GraphEra — Design meets Technology Startup |
| ↓ | |
| **2026** | 🏢 Full Stack Dev Intern @ Edubuk — Real-world impact |
| ↓ | |
| **2026** | 🌟 Community Builder — Helping peers grow in tech |
| ↓ | |
| **→ Now** | 🔮 Building production systems · Seeking SDE opportunities |

</div>
<br/>

## 📊 GitHub Profile Stats

Yaani ## 📊 GitHub Profile Stats se just pehle tak aapka original code yehi hai.

Agar aap Stats section replace kar rahi ho, to upar wala code bilkul same rehne do aur sirf ## 📊 GitHub Profile Stats ke neeche wala part change karo.

<div align="center">

<img src="https://raw.githubusercontent.com/Amritas851203/Amritas851203/main/banneramrita.jpeg" width="100%" alt="Amrita Singh Banner"/> <br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=26&duration=3000&pause=1000&color=A970FF&center=true&vCenter=true&width=700&lines=Hi+There%2C+I'm+Amrita+Singh+%F0%9F%91%8B;Full+Stack+Developer+%7C+Founder+%40+GraphEra;B.Tech+IT+%40+GGSIPU%2C+Delhi;Building+Products+That+Matter+%E2%9C%A8" alt="Typing SVG" />

<br/><br/>

<img src="https://komarev.com/ghpvc/?username=Amritas851203&color=A970FF&style=for-the-badge&label=PROFILE+VIEWS"/> &nbsp; <img src="https://img.shields.io/badge/dynamic/json?url=https://api.github.com/users/Amritas851203&label=FOLLOWERS&query=followers&color=7C4DFF&style=for-the-badge&logo=github&logoColor=white"/>

</div>

<br/>

<div align="center"><svg width="100%" height="6" viewBox="0 0 1000 6" xmlns="http://www.w3.org/2000/svg"> <defs> <linearGradient id="g1" x1="0%" y1="0%" x2="100%" y2="0%"> <stop offset="0%" stop-color="#0a0015"/> <stop offset="50%" stop-color="#A970FF"/> <stop offset="100%" stop-color="#0a0015"/> </linearGradient> </defs> <rect width="1000" height="6" rx="3" fill="url(#g1)"/> </svg></div>

💜 About Me

<table width="100%" border="0" cellpadding="0" cellspacing="0"> <tr> <td width="52%" valign="top">

Name:      Amrita Singh
Role:      Full Stack Developer & Intern @ Edubuk
Status:    Founder @ GraphEra | B.Tech IT @ GGSIPU
Mission:   Building products that create real impact
Location:  Delhi, India 🇮🇳
Open To:   SDE Roles · Internships · Collaborations

</td> <td width="4%"></td> <td width="44%" valign="top">

🎯 Currently Focused On:
   Mastering Full Stack Dev &
   Building Real-World Products

📚 Currently Learning:
   Advanced React · Backend
   Architecture · System Design

⚡ Fun Fact:
   I design as much as I code!
   Pixels & code are my world.

</td> </tr> </table>

<br/>

🛠️ Tech Arsenal

<div align="center">

<table width="88%" border="1" cellpadding="14" cellspacing="0" style="border-collapse:collapse; border-color:#4a2080;">

<tr> <td align="center" width="130" bgcolor="#0d0722"><b><font color="#A970FF">🖥️ Languages</font></b></td> <td bgcolor="#0d0722"> <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white"/> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/> <img src="https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/> </td> </tr>

<tr> <td align="center" bgcolor="#0d0722"><b><font color="#A970FF">⚛️ Frontend</font></b></td> <td bgcolor="#0d0722"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/> <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white"/> </td> </tr>

<tr> <td align="center" bgcolor="#0d0722"><b><font color="#A970FF">⚙️ Backend</font></b></td> <td bgcolor="#0d0722"> <img src="https://img.shields.io/badge/Node.js-43853D?style=flat-square&logo=node.js&logoColor=white"/> <img src="https://img.shields.io/badge/Express.js-404D59?style=flat-square&logo=express&logoColor=white"/> </td> </tr>

<tr> <td align="center" bgcolor="#0d0722"><b><font color="#A970FF">🗄️ Database</font></b></td> <td bgcolor="#0d0722"> <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> </td> </tr>

<tr> <td align="center" bgcolor="#0d0722"><b><font color="#A970FF">🔧 Tools & Design</font></b></td> <td bgcolor="#0d0722"> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/> <img src="https://img.shields.io/badge/VS_Code-0078D4?style=flat-square&logo=visualstudiocode&logoColor=white"/> <img src="https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white"/> </td> </tr>

</table>

</div>

<br/>

🚀 Featured Projects

<table width="100%" border="0" cellspacing="10" cellpadding="0"> <tr> <td width="49%" valign="top" bgcolor="#0d0722" style="border: 1.5px solid #4a2080; border-radius: 14px; padding: 20px;">

📈 Real-Time Stock Screener

Advanced stock analysis platform with live charts, TradingView-style indicators, and smart filters. Built for precision investors.






</td> <td width="2%"></td> <td width="49%" valign="top" bgcolor="#0d0722" style="border: 1.5px solid #4a2080; border-radius: 14px; padding: 20px;">

🏢 Smart Complaint Portal

Campus management system enabling students & faculty to raise, track, and resolve grievances in real-time with admin dashboards.





</td> </tr>

<tr><td colspan="3" height="10"></td></tr>

<tr> <td width="49%" valign="top" bgcolor="#0d0722" style="border: 1.5px solid #4a2080; border-radius: 14px; padding: 20px;">

🔮 GraphEra Website

Official website for my design-focused creative tech startup. Clean, bold, and built to convert visitors into clients.






</td> <td width="2%"></td> <td width="49%" valign="top" bgcolor="#0d0722" style="border: 1.5px solid #4a2080; border-radius: 14px; padding: 20px;">

💼 Personal Finance Tracker

Expense management dashboard with spending insights, category analysis, and monthly trend visualization for smarter decisions.





</td> </tr>

<tr><td colspan="3" height="10"></td></tr>

<tr> <td width="49%" valign="top" bgcolor="#0d0722" style="border: 1.5px solid #4a2080; border-radius: 14px; padding: 20px;">

🤖 AI Resume Analyzer

NLP-powered tool that reads your resume, identifies gaps, and generates specific improvement suggestions to land more interviews.






</td> <td width="2%"></td> <td width="49%" valign="top" bgcolor="#0d0722" style="border: 1.5px solid #4a2080; border-radius: 14px; padding: 20px;">

👤 Developer Portfolio

Personal portfolio to showcase projects, skills, and story. Designed with animation-first approach and responsive across all devices.






</td> </tr> </table>

<br/>

🎯 Current Focus

<div align="center">


	Area	Status	Details
☕	DSA	
	Java · Problem Patterns
⚙️	Backend Engineering	
	REST APIs · Auth · DBs
🌐	Full Stack Builds	
	End-to-end products
🧠	System Design	
	HLD · LLD
🤝	Open Source	
	Contributing to projects
🚀	Product — GraphEra	
	Building & scaling

</div>

<br/>

✨ Journey & Milestones

<div align="center">

🗓️ Year	🚀 Milestone
2024	🎓 Joined B.Tech IT @ GGSIPU Delhi — where the journey began
↓	

2025	💡 Fell in love with Full Stack Development
↓	

2025	🚀 Founded GraphEra — Design meets Technology Startup
↓	

2026	🏢 Full Stack Dev Intern @ Edubuk — Real-world impact
↓	

2026	🌟 Community Builder — Helping peers grow in tech
↓	

→ Now	🔮 Building production systems · Seeking SDE opportunities

</div> <br/>

📊 GitHub Profile Stats

<div align="center">

<!-- Streak: current + longest -->

<img src="https://streak-stats.demolab.com/?user=Amritas851203&theme=midnight-purple&background=0d0722&ring=A970FF&fire=7C4DFF&currStreakLabel=A970FF&sideLabels=b39ddb&border=4a2080&dates=8e8e93&hide_border=false" width="70%" alt="GitHub Streak" />

<br/><br/>

<!-- Contribution snake -->

<img src="https://raw.githubusercontent.com/Amritas851203/Amritas851203/output/github-snake-dark.svg" width="96%" alt="Contribution Snake" />

</div>

🌌 Amrita Singh Ecosystem

<div align="center">

<img src="https://raw.githubusercontent.com/Amritas851203/Amritas851203/main/ecosystem.svg" width="100%"/>

</div>

<br/>

💬 Developer Philosophy

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Georgia&style=italic&size=20&duration=4000&pause=2000&color=A970FF&center=true&vCenter=true&width=780&lines=%E2%80%9CTechnology+becomes+meaningful+when+it+solves+real+problems.%E2%80%9D;%E2%80%9CBuild+with+intention.+Ship+with+purpose.%E2%80%9D;%E2%80%9CCode+is+craft.+Products+are+stories.%E2%80%9D" alt="Philosophy"/>

</div>

<br/>

🔗 Connect With Me

<div align="center">

<br/>


 

 

 



<br/><br/>

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=120&section=footer&text=Thanks+for+visiting+✨&fontSize=22&fontColor=A970FF&animation=twinkling&fontAlignY=70" width="100%"/>

<br/>

✦ Made with 💜 by Amrita Singh · Building impact, one commit at a time ✦

</div>

Close
