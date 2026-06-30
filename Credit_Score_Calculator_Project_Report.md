# A PROJECT REPORT ON
## "Design and Development of a Web-Based Credit Score Calculator and Financial Health Analyzer"

**Submitted in partial fulfillment of the requirements for the award of the degree of**
### BACHELOR OF TECHNOLOGY
**In**
**DEPARTMENT OF COMPUTER SCIENCE ENGINEERING**
**&**
**DEPARTMENT OF COMPUTER SCIENCE AND INFORMATION TECHNOLOGY**

**By**
* **BATTULA MANASWINI** : 2420080029
* **SURYADEVARA NITEESH** : 2420030178
* **MACHARLA SAI SRUJAN** : 2420030256

**Under the Esteemed Guidance of**
* **Dr Yerragudipadu Subbarayudu** (Assistant Professor)
* Department of Computer Science and Engineering

---

## DECLARATION
We hereby declare that the Project Report entitled **"Design and Development of a Web-Based Credit Score Calculator and Financial Health Analyzer"** is a record of bonafide work done and submitted by us in partial fulfillment of the requirements for the award of B. Tech in Computer Science and Engineering (or) Computer Science and Information Technology to the K L University. The results embodied in this report have not been copied from any other departments/University/Institute.

* **BATTULA MANASWINI** – 2420080029
* **SURYADEVARA NITEESH** – 2420030178
* **MACHARLA SAI SRUJAN** – 2420030256

---

## CERTIFICATE
This is to certify that the mini project based report entitled **"Design and Development of a Web-Based Credit Score Calculator and Financial Health Analyzer"** is a bonafide work done and submitted by **BATTULA MANASWINI** - 2420080029, **SURYADEVARA NITEESH** - 2420030178, **MACHARLA SAI SRUJAN** - 2420030256 in partial fulfillment of the requirements for the award of the degree of **BACHELOR OF TECHNOLOGY** in Department of Computer Science Engineering, K L (Deemed to be University), during the academic year **2024-2025**.

* **Signature of the Guide**
* **Signature of the Course Coordinator**
* **Signature of the HOD**

---

## ACKNOWLEDGEMENT
The success in this project would not have been possible but for the timely help and guidance rendered by many people. Our wish to express my sincere thanks to all those who has assisted us in one way or the other for the completion of my project.

Our greatest appreciation to my Course Coordinator **Dr Yerragudipadu Subbarayudu**, and my guide **Dr Yerragudipadu Subbarayudu**, Department of Computer Science which cannot be expressed in words for his/her tremendous support, encouragement and guidance for this project.

We express our gratitude to **Dr. P Venkateshwara Rao** (CSE) / **Dr. Kaja Shareef** (CSIT), Head of the Department for Computer Science Engineering / Department for Computer Science and Information Technology for providing us with adequate facilities, ways and means by which we are able to complete this project-based Lab.

We thank all the members of teaching and non-teaching staff members, and also who have assisted me directly or indirectly for successful completion of this project. Finally, I sincerely thank my parents, friends and classmates for their kind help and cooperation during my work.

* **BATTULA MANASWINI** – 2420080029
* **SURYADEVARA NITEESH** – 2420030178
* **MACHARLA SAI SRUJAN** – 2420030256

---

## ABSTRACT
Credit scoring is a fundamental component of the modern financial ecosystem, determining an individual's eligibility for loans, credit cards, and interest rates. However, understanding credit scores and the factors that influence them remains a challenge for many consumers due to complex formulas and a lack of transparent, interactive tools. To address this, our project focuses on the **Design and Development of a Web-Based Credit Score Calculator and Financial Health Analyzer**. 

Our core aim is to implement a responsive, user-friendly single-page application (SPA) built using React.js, HTML5, CSS3, and JavaScript, which allows users to estimate their credit score dynamically and receive actionable feedback on their financial health. The platform is structured around key financial modules: Monthly Income evaluation, Repayment History (total EMIs and late payments), Credit Card Utilization (credit limit and used amount), and Credit Mix (active loans). It features real-time validation, a deterministic scoring engine (ranging from 300 to 900), and dynamic UI rendering of personalized financial recommendations. Additionally, the system employs localized state persistence via browser local storage to maintain user sessions seamlessly. Built with scalability and modern frontend architectures in mind, this project demonstrates a reliable and practical tool for financial literacy and decision-making.

---

## INDEX

| S. No. | Chapters | Topics |
|---|---|---|
| 1 | **Introduction** | 1.1 Background of the project <br> 1.2 Problem statement <br> 1.3 Scope of the project <br> 1.4 Objective(s) <br> 1.5 Importance of the application <br> 1.6 Target users/audience |
| 2 | **System Requirements** | 2.1 Hardware requirements <br> 2.2 Software requirements <br> 2.3 Development tools and frameworks |
| 3 | **Technology Stack** | 3.1 Front-end (React.js, HTML/CSS, Vanilla JS) <br> 3.2 State Management and Local Storage <br> 3.3 Version Control (Git, GitHub) |
| 4 | **System Architecture** | 4.1 High-level architecture diagram <br> 4.2 Description of each layer (frontend, logic, storage) |
| 5 | **Design** | 5.1 Data Flow Diagrams <br> 5.2 Form Layout Schema |
| 6 | **Implementation** | 6.1 Module-wise implementation <br> 6.2 Frontend logic and UI rendering <br> 6.3 State Persistence logic |
| 7 | **Features** | 7.1 List of main features <br> 7.2 How each feature works |
| 8 | **Testing** | 8.1 Functional testing and validation <br> 8.2 Test cases and results |
| 9 | **Deployment** | 9.1 Local setup and development server <br> 9.2 Build and deployment pipeline |
| 10 | **Challenges & Limitations** | 10.1 Issues faced during development <br> 10.2 Solutions applied <br> 10.3 Current limitations |
| 11 | **Future Enhancements** | 11.1 Planned features <br> 11.2 Possible integrations or optimizations |
| 12 | **Conclusion** | 12.1 Summary of the project <br> 12.2 What was achieved <br> 12.3 Skills learned |
| 13 | **References** | Books, tutorials, documentation sites used |
| 14 | **Appendices** | Sample code snippets |

---

## CHAPTER 1: INTRODUCTION

### 1.1 Background of the Project
Personal finance management is increasingly critical in today's credit-driven economy. A credit score, such as the CIBIL score in India, acts as a primary representation of an individual's financial discipline and creditworthiness. Financial institutions rely on these scores to assess risk before extending loans or credit cards. Historically, individuals had to rely on periodic, official credit reports which could be hard to interpret or cause "hard inquiries" that lower the score. Developing an interactive, privacy-respecting estimation tool allows users to understand how their daily financial decisions (e.g., credit card spending, late EMI payments, and active loan portfolios) impact their overall credit score.

### 1.2 Problem Statement
Existing credit score checking services suffer from several key issues:
1. **Privacy Concerns:** Most platforms require sharing sensitive details like PAN, SSN, or bank logins and often share user data with third-party advertisers.
2. **Lack of Interactivity:** Users cannot simulate different scenarios (e.g., "What happens if I pay off a loan?" or "What happens if I limit my credit card spending?").
3. **Complex Interfaces:** Standard reports are filled with complex jargon and offer no simple, direct explanations of the credit-affecting factors.
There is a clear need for a client-side, interactive calculator that dynamically models credit scores based on standard scoring criteria while protecting user privacy.

### 1.3 Scope of the Project
The scope of this project includes designing and developing a fully responsive web application that:
1. Simulates user authentication using lightweight browser local storage.
2. Collects key financial variables via form inputs (Income, total EMIs, late payments, credit limit, usage, active loans).
3. Executes a client-side, deterministic scoring algorithm outputting an estimated credit score between 300 and 900.
4. Generates dynamic, educational reasons highlighting the credit-lowering factors.

### 1.4 Objectives of the Project
* **To design and develop** an intuitive, responsive frontend interface using React.js and CSS3.
* **To implement** form validation pipelines that prevent mathematically impossible input combinations (e.g., late payments exceeding total EMIs).
* **To formulate** a credit scoring algorithm based on industry standards (repayment history, credit utilization, income capability, and credit mix).
* **To ensure** zero-cost, serverless state persistence using HTML5 LocalStorage.

### 1.5 Importance of the Application
This application serves as an educational tool for financial literacy. By visualizing the impact of late payments and high credit utilization, users gain actionable insights into how to improve their real credit scores. It enables risk-free scenarios simulation without generating hard pulls on the user's bureau file.

### 1.6 Target Users / Audience
* **General Consumers:** Individuals looking to estimate their credit score before applying for formal loans.
* **Young Professionals:** Tech-savvy users beginning their credit journey.
* **Students:** Learners seeking to understand the mechanisms of debt, EMIs, and credit utilization.

---

## CHAPTER 2: SYSTEM REQUIREMENTS

### 2.1 Hardware Requirements
* **Developer Environment:** Intel Core i5 or AMD Ryzen 5 processor, minimum 8 GB RAM, and solid-state storage (SSD) for fast build times.
* **Client Environment:** Any desktop, tablet, or smartphone with a dual-core processor and at least 2 GB RAM.

### 2.2 Software Requirements
* **Operating System:** Windows 10/11, macOS, or Ubuntu Linux.
* **Runtime Environment:** Node.js (version 18.x LTS recommended) and npm.
* **Web Browser:** Google Chrome, Mozilla Firefox, Microsoft Edge, or Safari with JavaScript enabled.

### 2.3 Development Tools and Frameworks
* **IDE:** Visual Studio Code (VS Code) with extensions for ESLint and React.
* **Framework:** React.js (via Vite scaffolding) for a component-based structure.
* **Styling:** Custom Vanilla CSS for modular, high-fidelity styles.
* **Version Control:** Git version control system hosted on GitHub.

---

## CHAPTER 3: TECHNOLOGY STACK

### 3.1 Front-End Design
The frontend architecture utilizes React.js for component rendering and state management. The user interface is structured using semantic HTML5 elements (`<form>`, `<section>`, `<input>`, `<button>`) and styled with vanilla CSS3. Grid layouts and flexbox are employed to ensure the layout adapts seamlessly to mobile, tablet, and desktop screens. 

### 3.2 State Management & Local Storage
Rather than using heavy database engines, this serverless calculator achieves state persistence using the web browser's native **LocalStorage API**. When a user logs in, their profile (`userName` and `userContact`) is stored locally, allowing session persistence across browser reloads.

### 3.3 Version Control
* **Git:** Used for tracking local code revisions.
* **GitHub:** Serves as the cloud repository hosting service, facilitating easy version management and codebase safety.

---

## CHAPTER 4: SYSTEM ARCHITECTURE

### 4.1 High-Level Architecture Diagram
The application follows a client-side layered architecture representing the separation of concerns:

```
+-------------------------------------------------------------+
|                      User Browser                           |
+-------------------------------------------------------------+
                               |
                               v
+-------------------------------------------------------------+
|        Presentation Layer (React Login & Dashboard)         |
+-------------------------------------------------------------+
                               |
                               v
+-------------------------------------------------------------+
|        Validation & Business Logic Layer (Scoring Engine)   |
+-------------------------------------------------------------+
                               |
                               v
+-------------------------------------------------------------+
|             Data Persistence Layer (LocalStorage)            |
+-------------------------------------------------------------+
```

### 4.2 Description of Each Layer
1. **Presentation Layer:** Contains React pages ([Login.jsx](file:///C:/Users/user/OneDrive/Desktop/FEDF/credit-score-react/src/pages/Login.jsx) and [Dashboard.jsx](file:///C:/Users/user/OneDrive/Desktop/FEDF/credit-score-react/src/pages/Dashboard.jsx)) that capture user inputs and render outputs.
2. **Validation & Business Logic Layer:** Validates the constraints (e.g., ensuring used credit is not larger than the limit) and computes the estimated credit score (300 to 900) dynamically using conditional scoring factors.
3. **Data Persistence Layer:** Uses browser local storage to persist basic session metadata.

---

## CHAPTER 5: DESIGN

### 5.1 Data Flow Diagram
The data flows sequentially through the application:
1. **User Details Entry:** User registers name and phone number on the login screen.
2. **Session Storage:** Registration updates the browser's `localStorage` state.
3. **Dynamic Redirect:** User is navigated to the dashboard.
4. **Calculations Trigger:** Inputs are fed to the JavaScript calculator function.
5. **UI Updates:** DOM is updated with the score, rating category (Poor, Average, Good, Excellent), and detailed financial advice list.

### 5.2 Form Layout Schema
The input forms consist of structured input groups, each bound to a specific validation criterion:
* **Monthly Income:** Numerical field.
* **Total EMIs:** Numerical field, representing total cycles.
* **Late EMI Payments:** Numerical field, restricted by total EMIs.
* **Credit Limit:** Total spending capacity.
* **Used Credit:** Spending level, capped by credit limit.
* **Active Loans:** Active debt count.

---

## CHAPTER 6: IMPLEMENTATION

### 6.1 Module-Wise Implementation
* **Login Module:** Captures user profile and contact number. Integrates validation on the phone number input (expects 10 digits).
* **Credit Scoring Module:** Calculates the credit score based on 4 primary pillars:
  * **Income Pillar (Weight ~17%):** High income adds up to 150 points.
  * **Repayment History Pillar (Weight ~28%):** Timely repayments add up to 250 points.
  * **Credit Utilization Pillar (Weight ~20%):** Lower utilization ratios add up to 180 points.
  * **Credit Mix and Volume (Weight ~13%):** Balanced credit lines add up to 120 points.
* **Feedback System Module:** Appends actionable suggestions to an array and renders them dynamically as bullet points.

### 6.2 Frontend Logic & UI Rendering
The application handles user interaction via React state hooks:
* `useState` tracks values of income, EMIs, late payments, limits, usage, loans, score, and reasons.
* `useEffect` fetches persisted session profiles on component mount.

### 6.3 State Persistence Logic
Session storage is updated imperatively upon form submissions:
```javascript
localStorage.setItem("userName", name);
localStorage.setItem("userContact", contact);
```

---

## CHAPTER 7: FEATURES

### 7.1 List of Main Features
1. **No Hard Pull Risk:** Totally simulation-based, protecting the user's real credit record.
2. **Client-Side Validation:** Inline validation prompts for math errors (e.g., late payments > total EMIs).
3. **Dynamic Feedback Engine:** Generates specific credit health advice based on exact user inputs.
4. **Clean Session Resumption:** Local storage remembers user profiles on reload.

### 7.2 How Each Feature Works
* **Login Submission:** Saves user profile locally and updates dashboard header greetings.
* **Score Calculation:** Processes inputs to output a credit rating (300 to 900).
* **Dynamic Styling:** Modifies CSS attributes dynamically to present clean progress updates.

---

## CHAPTER 8: TESTING

### 8.1 Functional Testing and Validation
Testing focused on edge cases, mathematical constraints, and input constraints.

### 8.2 Test Cases and Results

| Test Case | Description | Input Data | Expected Output | Actual Output | Status |
|---|---|---|---|---|---|
| TC-01 | Normal Calculations | Income: 60,000 <br> EMIs: 10 <br> Late: 0 <br> Limit: 10,000 <br> Used: 2,000 <br> Loans: 1 | Score: 780 <br> Rating: Excellent | Score: 780 <br> Rating: Excellent | **PASS** |
| TC-02 | Input validation: Late payments exceed EMIs | EMIs: 5 <br> Late Payments: 8 | Alert: "Late payments cannot exceed total EMIs" | Alert shown, calculation blocked | **PASS** |
| TC-03 | Input validation: Used credit exceeds credit limit | Limit: 5,000 <br> Used Credit: 6,000 | Alert: "Used credit cannot exceed total credit limit" | Alert shown, calculation blocked | **PASS** |
| TC-04 | High credit risk profile | Income: 12,000 <br> EMIs: 10 <br> Late: 9 <br> Limit: 10,000 <br> Used: 9,000 <br> Loans: 6 | Score: 360 <br> Rating: Poor <br> Multiple suggestions shown | Score: 360 <br> Rating: Poor <br> Suggestions shown | **PASS** |

---

## CHAPTER 9: DEPLOYMENT

### 9.1 Local Setup and Development Server
To launch the React project locally, the development team follows these steps:
1. Navigate to the project subdirectory:
   ```bash
   cd C:\Users\user\OneDrive\Desktop\FEDF\credit-score-react
   ```
2. Install node dependencies:
   ```bash
   npm install
   ```
3. Run the Vite development server:
   ```bash
   npm run dev
   ```
4. Access the server URL locally (usually `http://localhost:5173`).

### 9.2 Build and Deployment Pipeline
To output clean, static production bundles, Vite compile scripts are executed:
```bash
npm run build
```
The compiled files in the `dist` directory are ready to be hosted on serverless platforms such as Netlify, Vercel, or AWS S3 buckets.

---

## CHAPTER 10: CHALLENGES & LIMITATIONS

### 10.1 Issues Faced During Development
* **State Syncing:** Keeping user values clean during form resets.
* **Input Constraints:** Managing input forms where string values could corrupt calculations (resolved by parsing all numeric inputs through `Number()`).

### 10.2 Solutions Applied
* Integrated defensive checks and validation dialogs before executing calculations.
* Standardized form styling to match clean design principles.

### 10.3 Current Limitations
1. **Estimate Only:** The score is a simulated value and does not reflect real-time credit bureau data.
2. **Local Storage Dependancy:** Clear-cache actions erase user profiles.

---

## CHAPTER 11: FUTURE ENHANCEMENTS

### 11.1 Planned Features
* **Interactive Score Simulator:** Sliders allowing users to see credit-improvement forecasts in real time.
* **Data Visualizations:** Visual gauges and charts to show credit-influencing factors.

### 11.2 Possible Integrations
* **Bank API Integration:** Fetching actual financial metadata via Open Banking APIs.
* **Bureau API Connectivity:** Accessing real-time updates from Experian or CIBIL.

---

## CHAPTER 12: CONCLUSION

### 12.1 Summary of the Project
The Web-Based Credit Score Calculator provides a clean, privacy-centric alternative to standard credit-checking portals. It allows individuals to estimate scores dynamically and learn the variables influencing their ratings without lowering their actual scores.

### 12.2 What Was Achieved
The project successfully delivers:
1. A modular React application with responsive inputs and clean pages.
2. An interactive scoring model calculating rating ranges between 300 and 900.
3. Localized session caching using HTML5 localStorage features.

### 12.3 Skills Learned
* **Full-stack concepts:** Developing client-side single-page applications.
* **Form validation:** Managing edge-case input handling in React state.
* **Responsive web styling:** Using Flexbox and media queries.

---

## CHAPTER 13: REFERENCES
1. Pressman, R. S. (2019). *Software Engineering: A Practitioner's Approach*. McGraw-Hill.
2. React Documentation - React State and Hooks. Retrieved from [react.dev](https://react.dev).
3. CIBIL Scoring Methodologies and Criteria. Retrieved from [cibil.com](https://www.cibil.com).
4. MDN Web Docs - LocalStorage API. Retrieved from [developer.mozilla.org](https://developer.mozilla.org).

---

## CHAPTER 14: APPENDICES

### Sample Code Snippet (Score Calculation Engine)
```javascript
const calculateScore = () => {
  if (Number(latePayments) > Number(totalEmi)) {
    alert("Late payments cannot exceed total EMIs");
    return;
  }
  if (Number(usedCredit) > Number(creditLimit)) {
    alert("Used credit cannot exceed credit limit");
    return;
  }

  let creditScore = 300;
  let feedback = [];

  if (income > 100000) {
    creditScore += 150;
  } else if (income > 50000) {
    creditScore += 100;
  } else {
    creditScore += 50;
    feedback.push("Low income affects score.");
  }

  const repayment = ((totalEmi - latePayments) / totalEmi) * 100;
  if (repayment >= 95) {
    creditScore += 250;
  } else if (repayment >= 80) {
    creditScore += 180;
    feedback.push("Some late payments found.");
  } else {
    creditScore += 80;
    feedback.push("Poor repayment history.");
  }

  const usage = (usedCredit / creditLimit) * 100;
  if (usage < 30) {
    creditScore += 180;
  } else if (usage < 75) {
    creditScore += 80;
    feedback.push("High credit utilization.");
  }

  if (loans === 0) {
    creditScore += 120;
  } else if (loans > 5) {
    creditScore -= 20;
    feedback.push("Too many active loans.");
  }

  if (creditScore > 900) creditScore = 900;
  // ...
};
```
