# KrishiConnect

KrishiConnect is a smart agriculture management system that helps farmers monitor their crops using IoT sensors, get AI-powered recommendations, and make data-driven decisions for better crop management.

## Features

- 📊 Real-time sensor data monitoring (temperature, humidity, soil moisture, light intensity)
- 🌱 AI-powered crop recommendations based on environmental conditions
- 🤖 Smart chatbot for agricultural queries
- 🗺️ Location-based insights and mapping
- 📈 Historical data visualization with charts
- 🔍 Plant disease detection and solutions

## Tech Stack

### Frontend

- React.js with Vite
- Material UI
- Chart.js for data visualization
- Leaflet for maps
- TailwindCSS for styling

### Backend

- Node.js with Express
- MongoDB for data storage
- Google's Generative AI (Gemini) for AI features
- Geolocation API integration

## Project Structure

```
krishiconnect/
├── client/               # Frontend React application
│   ├── src/             # Source code
│   ├── Dockerfile       # Frontend Docker configuration
│   └── docker-compose.yaml
│
└── server/              # Backend Node.js application
    ├── Dockerfile       # Backend Docker configuration
    └── docker-compose.yaml
```

## Prerequisites

- Node.js (v20 or later)
- Docker and Docker Compose
- MongoDB (if running locally without Docker)
- Google API Key (for Gemini AI)
- Geolocation API Key

## Environment Variables

Create `.env` files in both client and server directories:

### Server `.env`

```
MONGODB=your_mongodb_connection_string
GOOGLE_API_KEY=your_google_api_key
GEOLOCATION_API_KEY=your_geolocation_api_key
PORT=5100
```

### Client `.env`

```
VITE_API_URL=http://localhost:5100
```

## Running with Docker (Recommended)

1. Clone the repository:

```bash
git clone <repository-url>
cd krishiconnect
```

2. Start all services using Docker Compose:

```bash
docker-compose up --build
```

The application will be available at:

- Frontend: http://localhost
- Backend API: http://localhost:5100

## Development Setup

### Frontend

```bash
cd client
npm install
npm run dev
```

### Backend

```bash
cd server
npm install
node index.js
```

## API Endpoints

- `GET /api/sensor-data`: Get real-time sensor data and location information
- `POST /chatbot`: AI chatbot for agricultural queries
- `POST /disease`: Get plant disease information and solutions
- `POST /cropai`: Get crop recommendations based on sensor data

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Thanks to all contributors who have helped with the project
- Special thanks to the open-source community for the tools and libraries used in this project
