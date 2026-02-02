# ClinicWay: Full-Stack Hospital Management System 🏥

This is a web application I built during my PG-DAC at C-DAC to solve the problem of crowded clinic waiting rooms. It replaces manual paper tokens with a digital queue management system.

## ⚙️ Core Functionality
The system handles the "Patient Lifecycle" in a clinic:
1. **Receptionist Dashboard:** Used to register new patients and assign them a token number.
2. **Doctor Dashboard:** Allows the doctor to see the live queue, view patient details, and mark consultations as "Completed."
3. **Live Queue Tracking:** Manages both online pre-booked appointments and on-spot walk-ins.

## 🛠️ Tech Stack
* **Backend:** Java, Spring Boot, Spring Data JPA
* **Database:** MySQL (Relational schema for patients and tokens)
* **Frontend:** HTML, CSS, JavaScript (React)
* **API Testing:** Postman

## 🧠 The "Engineering" Challenge: Atomic Tokens
Coming from a Mechanical background, I focused on the "process flow." The hardest part was ensuring that two patients don't get assigned the same Token ID if they register at the exact same millisecond. 
* I solved this by using **SQL constraints** and **Atomic increments** to ensure data integrity during concurrent bookings.

## 📁 Project Structure
* `/backend`: Contains the Spring Boot controllers, services, and repository layers.
* `/frontend`: Contains the UI components and API integration logic.

## 🚧 Known Issues & Future Scope
As this is a v1 prototype, there are a few things I am still working on:
* **Security:** I plan to add JWT (JSON Web Tokens) to secure doctor logins.
* **Notifications:** Adding an SMS/Email trigger when a patient's turn is next.
* **UI Polish:** Improving the mobile responsiveness for tablets.

---
**Note:** I built this to bridge the gap between my engineering logic and software development. It helped me master how data flows from a UI to a database.  
