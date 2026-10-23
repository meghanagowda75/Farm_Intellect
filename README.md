# 🌱 Farm Intellect – AI-Powered Smart Farming Platform

Farm Intellect is an AI-powered smart farming application designed to help farmers make informed agricultural decisions using artificial intelligence, weather information, crop recommendations, market price predictions, and other digital farming tools.

The platform brings multiple farming-related features together in one application to support crop planning, farm management, agricultural information sharing, and data-driven decision-making.

## 📌 Project Overview

Agriculture depends on several changing factors, including weather conditions, soil characteristics, crop selection, market prices, and farming practices. Making decisions without reliable information can lead to lower productivity and financial losses.

Farm Intellect aims to address these challenges through a unified application that provides AI-assisted recommendations and useful farming tools through an accessible user interface.

### 🎯 Objectives

- Provide AI-assisted crop recommendations.
- Display weather information for selected locations.
- Support market price forecasting.
- Assist farmers with crop rotation planning.
- Estimate agricultural carbon footprints.
- Provide digital tools for smart irrigation and farm management.
- Enable communication and knowledge sharing among farmers.
- Support different user roles through user management features.
- Bring essential smart farming features together in one application.

## ✨ Features

### 🌾 1. AI-Powered Crop Recommendations

- Provides crop recommendations using AI-assisted processing.
- Supports agricultural decision-making.
- Uses the available input data to generate recommendations.
- Integrates with the backend AI functionality.

### 🌦️ 2. Weather Information

- Retrieves weather information for supported locations.
- Helps farmers consider current weather conditions when planning farming activities.
- Integrates with weather data services where configured.
- Supports location-based weather information.

### 📈 3. Market Price Prediction

- Provides AI-assisted agricultural market price forecasts.
- Supports selected crops, including wheat, rice, maize, soybean, onion, and cotton.
- Allows users to request predictions through the application interface.
- Presents forecast information to help users understand potential market trends.

*Predictions are estimates and should not be treated as guaranteed future market prices.*

### 🔄 4. Crop Rotation Optimizer

- Supports crop rotation planning.
- Helps users explore alternative crop sequences.
- Integrates with the AI backend where the relevant endpoint is configured and available.

### 🌍 5. Carbon Footprint Calculator

- Helps estimate the environmental footprint associated with farming activities.
- Provides a dedicated interface for entering agricultural information.
- Supports AI-assisted recommendations where configured.

### 💧 6. Smart Irrigation

- Provides a dedicated feature for smart irrigation support.
- Can use available weather information to help inform irrigation decisions.
- Supports the broader goal of efficient water management.

### 👨‍🌾 7. Farmer Collaboration Hub

- Provides a space for farmer interaction and knowledge sharing.
- Supports agricultural discussions and collaboration.
- Helps users exchange farming experiences and information.

### 👥 8. User Management

- Provides an administrative interface for viewing platform users.
- Supports user roles such as Farmer, Merchant, Expert, and Admin.
- Includes user search and role-management interface functionality.

### 🗣️ 9. Multilingual Voice Assistant

- Provides an interface for multilingual and voice-based assistance.
- Is designed to make agricultural information more accessible to users with different language preferences.

### 📱 10. Application Interface

- Provides a unified interface for accessing the platform's farming features.
- Uses reusable React components and a responsive UI approach.
- Organizes features into dedicated pages and components.
- Includes navigation and interface elements for different platform functions.

## 🛠️ Technology Stack

### Frontend
- React
- TypeScript
- Vite
- Tailwind CSS
- Reusable UI components
- Lucide React icons

### Backend
- Node.js
- Express.js
- REST API architecture
- JavaScript ES modules

### Artificial Intelligence
- Google Gemini API
- AI-assisted recommendations and prediction workflows

### Database and Authentication
- Prisma-based database integration where configured
- Application authentication and user-management logic
- Mock authentication and local application data for development where external services are not configured

### External Integrations
- Weather data services where configured
- Google Gemini API for supported AI functionality

> **Note:** Farm Intellect does not use Supabase in this project version. Actual database, authentication, and external-service functionality depends on the configuration available in the project environment.

## 🏗️ System Architecture

Farm Intellect follows a frontend–backend architecture.

```text
                 FARM INTELLECT
                       |
          +------------+------------+
          |                         |
     Frontend                  Application UI
   React + TypeScript          Navigation
          |                    Feature Pages
          |                    User Interface
          |
       REST APIs
          |
          v
      Node.js + Express
          |
     +----+-------------------+
     |            |            |
     v            v            v
   AI Logic    Weather      Data Layer
     |          Service     (Configured DB)
     |
     v
  Google Gemini API
     |
     v
 Recommendations and
 AI-Assisted Predictions
```

The frontend communicates with the backend through API requests. The backend processes requests and connects to configured AI, weather, and data services.

## 📂 Project Structure

The main project structure is organized as follows. Individual files and directories may differ depending on the current project version.

```text
Farm_Intellect/
│
├── src/
│   ├── components/
│   │   ├── features/
│   │   ├── layout/
│   │   └── ui/
│   │
│   ├── contexts/
│   ├── lib/
│   ├── pages/
│   └── ...
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── middleware/
│   │   ├── routes/
│   │   ├── services/
│   │   └── server.js
│   │
│   ├── package.json
│   └── ...
│
├── public/
├── android/
├── package.json
├── .gitignore
└── README.md
```

The `android/` directory contains Android application-related project files, if included in the checked-out project. The main React application and backend are maintained in their respective source directories.

## ⚙️ Installation and Setup

### Prerequisites

Install the following tools before running the project:

- Node.js and npm
- Git
- A code editor such as Visual Studio Code
- A Google Gemini API key for AI functionality
- Any database required by the configured backend

### 1. Clone the Repository

```bash
git clone https://github.com/meghanagowda75/Farm_Intellect.git
cd Farm_Intellect
```

### 2. Install Frontend Dependencies

From the project root:

```bash
npm install
```

### 3. Install Backend Dependencies

```bash
cd backend
npm install
```

Return to the project root when needed:

```bash
cd ..
```

### 4. Configure Environment Variables

Create a backend `.env` file inside the `backend/` directory and add the environment variables required by your local setup.

Example:

```env
PORT=3001
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=gemini-2.5-flash
```

Add the database connection variable only if your configured database requires it. Use the variable name expected by the project's database configuration.

**Important:** Replace the example API key with your own key. Never commit actual API keys, passwords, or other secrets to GitHub.

### 5. Start the Backend

Open a terminal:

```bash
cd backend
npm run dev
```

The backend is expected to run on port `3001` when configured with the example above.

### 6. Start the Frontend

Open a second terminal in the project root:

```bash
npm run dev
```

Open the local URL displayed by Vite in the terminal.

If a command is unavailable, check the corresponding `package.json` scripts and use the command defined by the project.

## 🔑 Environment Configuration

The application may require the following configuration, depending on the features being used.

| Variable | Purpose |
|---|---|
| `PORT` | Backend server port |
| `GEMINI_API_KEY` | Authentication for Google Gemini API requests |
| `GEMINI_MODEL` | Gemini model used by the backend |
| `DATABASE_URL` | Database connection string, if required by the configured database |
| `VITE_API_BASE_URL` | Optional frontend API base URL |

Do not publish private environment files. Keep only safe example values in `.env.example`.

## 🔌 API Integration

The backend exposes REST API routes for application functionality. The exact routes available depend on the current backend implementation.

Potential API areas include:

- AI-assisted agricultural recommendations
- Market price prediction
- Crop rotation planning
- Yield prediction
- Weather information
- User and application data management

Frontend API requests are configured through the application's API utility. In development, the frontend may use `http://localhost:3001` as the backend base URL.

Only endpoints actually registered by the backend can be used successfully. If an endpoint is unavailable, verify its route registration and required configuration before using it in the frontend.

## 🔐 Security Considerations

- Store API keys in environment variables.
- Do not commit `.env` files or private credentials.
- Validate incoming API requests.
- Apply authentication and authorization to protected operations.
- Restrict administrative operations to authorized users.
- Avoid exposing private user information in API responses.
- Use appropriate production database and deployment security settings.

Development mock authentication should not be treated as production-grade authentication.

## 🧪 Testing and Validation

The project can be tested by checking the following areas:

1. Frontend startup and navigation.
2. Backend startup and API connectivity.
3. AI feature responses with valid configuration.
4. Weather retrieval for supported locations.
5. Market prediction requests and displayed results.
6. User interface behavior and role-management functionality.
7. Error handling when a service or API is unavailable.
8. Responsive behavior across supported screen sizes.

Run tests using the scripts defined in the root or backend `package.json`, if available.

## 🚀 Future Enhancements

Possible future improvements include:

- Integration with verified agricultural market data sources.
- More accurate and transparent crop price forecasting.
- Improved crop recommendations using soil and regional agricultural data.
- Integration with soil sensors and IoT-based irrigation devices.
- Additional regional languages and voice support.
- Stronger production authentication and role-based authorization.
- Improved mobile application integration.
- Expanded automated testing and deployment workflows.
- More detailed farming analytics and reports.

These are potential enhancements, not claims that every item is already implemented.

## 🤝 Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Implement and test your changes.
4. Commit your changes with a descriptive message.
5. Submit a pull request.

## 👩‍💻 Developer

**Meghana B M**

GitHub: [meghanagowda75](https://github.com/meghanagowda75)

Project Repository: [Farm_Intellect](https://github.com/meghanagowda75/Farm_Intellect)

## 📄 License

Add the appropriate license for this project before distributing or reusing the source code. Until a license is specified in the repository, reuse permissions should not be assumed.

## 🙏 Acknowledgments

- Open-source developers and maintainers of the technologies used in the project.
- Google Gemini for AI capabilities where configured.
- Providers of weather information used by the application.
- The agricultural community, whose needs inspire smart farming solutions.

---

**Farm Intellect — Bringing AI and digital technology together to support smarter farming.**
