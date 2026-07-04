# IntelliTrip — AI-Powered Multi-Agent Travel Planner

IntelliTrip is a premium, responsive web application that generates practical, budget-aware, and highly detailed travel itineraries. The project is built using a modern **Multi-Agent AI Pipeline** on the backend and a futuristic **Glassmorphic Dashboard UI** on the frontend.

---

## 🌟 Key Features

- **Multi-Agent Coordination (LangGraph)**:
  - **Flight Agent**: Resolves origin and destination locations to IATA codes, searches live flight data via AviationStack API.
  - **Hotel Agent**: Gathers local lodging recommendations and accommodation insights using Tavily Search.
  - **Itinerary Agent**: Consolidates flights and hotels into a structured day-by-day travel schedule.
  - **Final Agent**: Generates the final output response, including Trip Summaries, Budgets, and Recommendations.
- **Premium Glassmorphic UI**: Combines design ethics from VisionOS, Linear, and Vercel. Includes interactive custom particle background canvases, smooth scrolling, button ripple triggers, and responsive layouts.
- **Persistent Memory**: Connects to a PostgreSQL database on Render to store conversation states and checkpointer logs, allowing persistent context between multiple travel planner runs.
- **Exporting Options**: Export your finalized travel plan instantly to a high-quality PDF or copy it directly to your clipboard.

---

## 🛠️ Technology Stack

### Backend
- **Core**: FastAPI, Python 3.12
- **Agent Framework**: LangGraph, LangChain
- **LLM Provider**: Groq Cloud (Llama-3.3-70b-versatile)
- **Database**: PostgreSQL (via `psycopg` and `PostgresSaver` checkpointer memory)
- **External Integration**: Tavily API (Hotels), AviationStack API (Live Flight Status)

### Frontend
- **Interface**: HTML5 (Semantic), Vanilla CSS3, Vanilla JavaScript
- **Plugins**: `marked.js` (Markdown parsing), `html2pdf.js` (PDF generation)

---

## ⚙️ Installation & Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/aditya-students/IntelliTrip---MultiAgent-Travel-Planner.git
   cd "IntelliTrip Multi-Agent Travel Planner"
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the root directory of the project and populate it with your credentials:
   ```env
   GROQ_API_KEY=your_groq_api_key
   AVIATIONSTACK_API_KEY=your_aviationstack_key
   TAVILY_API_KEY=your_tavily_key
   DATABASE_URL=postgresql://user:pass@host/db
   DEFAULT_ORIGIN_IATA=USA
   ```

4. **Run the Application**:
   ```bash
   python app.py
   ```
   Open your browser and navigate to **[http://127.0.0.1:8000](http://127.0.0.1:8000)**.

---

## 📄 License

This project is licensed under the MIT License.