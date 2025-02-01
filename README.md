# 🏥 Epitrack

**Epitrack** is an open-source web and mobile application for managing and tracking epilepsy episodes and medication.  
It allows patients and healthcare professionals to log, monitor, and analyze epileptic seizures in a structured way.

## 🚀 Features

- 📌 User authentication and profile management
- 📊 Seizure logging and history tracking
- 💊 Medication reminders and schedule
- 📈 Reports and data export (PDF/CSV)
- 🌐 Web (React) and Mobile (React Native) versions
- 🔐 Secure backend powered by Node.js

## 🛠 Tech Stack

- **Frontend:** React (Web) / React Native (Mobile)
- **Backend:** Node.js (NestJS) + PostgreSQL
- **Auth:** JWT-based authentication
- **Styling:** TailwindCSS
- **Testing:** Vitest
- **License:** [AGPLv3](LICENSE)

## 📦 Installation

### **1️⃣ Clone the repository**
```sh
git clone https://github.com/luismattos/epitrack.git
cd epitrack
```

### **2️⃣ Install dependencies**
```sh
cd backend && npm install
cd ../frontend && npm install
```

### **3️⃣ Set up environment variables**
Copy the `.env.example` file in both backend and frontend and configure it.

### **4️⃣ Run the project**
#### Backend:
```sh
cd backend
npm run start
```
#### Frontend:
```sh
cd frontend
npm run dev
```

## 🤝 Contributing

We welcome contributions! Read the [Contributing Guide](CONTRIBUTING.md) to get started.

## 📜 License

Epitrack is licensed under the **GNU AGPLv3**. See the full [LICENSE](LICENSE) for details.
