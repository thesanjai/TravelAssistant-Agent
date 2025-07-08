# 🌍 AI-Powered Travel Planner

Plan your dream trip with AI! This interactive Streamlit application provides personalized recommendations for flights, hotels, restaurants, and activities based on your travel preferences and style.

![Travel Planner](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![AI](https://img.shields.io/badge/AI-Powered-brightgreen?style=for-the-badge)

---

## ✨ Features

🔍 **Smart Flight Search** - Find the cheapest flight options using SerpAPI integration  
🤖 **AI Destination Research** - Get comprehensive insights on climate, culture, attractions, and safety  
🏨 **Hotel & Restaurant Finder** - Discover top-rated accommodations and dining options  
📅 **Personalized Itinerary** - Receive detailed, day-by-day travel plans tailored to your interests  
🎒 **Packing Checklist** - Interactive sidebar to organize your travel essentials  
💼 **Travel Essentials** - Quick access to visa, insurance, and currency information  
🎭 **Multiple Travel Themes** - Couple getaway, family vacation, adventure trip, or solo exploration  

---

## 🚀 Quick Start

### Prerequisites

- **Python 3.9+** installed on your system
- **pip** package manager
- **Git** (optional, for cloning)

### 1. Get the Project

**Option A: Clone the repository**
```bash
git clone https://github.com/thesanjai/TravelAssistant-Agent.git
cd TravelAssistant-Agent
```

**Option B: Download ZIP**
Download and extract the project files to your desired directory.

### 2. Set Up Virtual Environment

**Ubuntu/Linux/macOS:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Get API Keys

#### SerpAPI Key
1. Visit [serpapi.com](https://serpapi.com)
2. Sign up for a free account
3. Navigate to your dashboard
4. Copy your API key

#### Google Gemini API Key
1. Go to [Google AI Studio](https://aistudio.google.com/)
2. Sign in with your Google account
3. Create a new API key in your project
4. Copy and securely store your API key

### 5. Configure Environment Variables

Create a `.env` file in your project root:

```env
SERPAPI_KEY=your_serpapi_key_here
GOOGLE_API_KEY=your_google_gemini_api_key_here
```

**⚠️ Important:** Never commit your `.env` file to version control!

### 6. Run the Application

```bash
streamlit run app.py
```

The app will automatically open in your default browser at `http://localhost:8501`

---

## 🛠 Requirements

### System Requirements
- **Operating System:** Windows, macOS, or Linux (Ubuntu recommended)
- **Python:** Version 3.9 or higher
- **Memory:** At least 2GB RAM
- **Internet:** Stable connection for API calls

### Python Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| streamlit | >=1.28.0 | Web application framework |
| google-search-results | >=2.4.2 | SerpAPI integration |
| agno | >=1.1.0 | AI agent framework |
| requests | >=2.31.0 | HTTP requests |
| pandas | >=2.0.0 | Data manipulation |
| python-dotenv | >=1.0.0 | Environment variable management |

See `requirements.txt` for the complete list with exact versions.

---

## 📖 Usage Guide

### Basic Workflow

1. **Enter Travel Details**
   - Departure city (IATA code, e.g., BOM for Mumbai)
   - Destination (IATA code, e.g., DEL for Delhi)
   - Travel dates
   - Trip duration (1-14 days)

2. **Select Preferences**
   - Travel theme (Couple, Family, Adventure, Solo)
   - Activities you enjoy
   - Budget level (Economy, Standard, Luxury)
   - Flight class and hotel rating

3. **Generate Your Plan**
   - Click "🚀 Generate Travel Plan"
   - Wait for AI agents to research and plan
   - Review your personalized itinerary

### Travel Themes

- **💑 Couple Getaway:** Romantic destinations and intimate experiences
- **👨‍👩‍👧‍👦 Family Vacation:** Kid-friendly activities and family accommodations
- **🏔️ Adventure Trip:** Outdoor activities and thrilling experiences
- **🧳 Solo Exploration:** Independent travel with cultural immersion

### IATA Code Examples

| City | IATA Code |
|------|-----------|
| Mumbai | BOM |
| Delhi | DEL |
| New York | JFK |
| London | LHR |
| Tokyo | NRT |
| Paris | CDG |

---

## 🗂 Project Structure

```
TravelAssistant-Agent/
│
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── .env                  # Environment variables (not in repo)
├── .env.template         # Template for environment setup
├── .gitignore           # Git ignore rules
├── README.md            # This file
├── setup.sh             # Automated setup script (Linux/macOS)
└── assets/              # Static assets (if any)
    └── images/
```

---

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `SERPAPI_KEY` | Your SerpAPI key for flight and search data | Yes |
| `GOOGLE_API_KEY` | Your Google Gemini API key for AI functionality | Yes |

### Customization Options

You can modify the following in the code:
- Default cities and IATA codes
- Travel themes and preferences
- UI styling and colors
- Agent instructions and behavior

---

## ❓ Troubleshooting

### Common Issues

**"streamlit: command not found"**
```bash
# Make sure Streamlit is installed and your virtual environment is active
pip install streamlit
source venv/bin/activate  # Linux/macOS
# or
venv\Scripts\activate   # Windows
```

**API Key Errors**
- Verify your API keys are correctly set in `.env`
- Check your API quotas and limits
- Ensure keys are not expired

**Module Import Errors**
```bash
# Reinstall dependencies
pip install -r requirements.txt --force-reinstall
```

**Port Already in Use**
```bash
# Use a different port
streamlit run app.py --server.port 8502
```

### Ubuntu-Specific Issues

**PATH Issues with pip packages:**
```bash
# Add local bin to PATH
export PATH=$PATH:~/.local/bin
echo 'export PATH=$PATH:~/.local/bin' >> ~/.bashrc
source ~/.bashrc
```

**Permission Issues:**
```bash
# Use user installation
pip install --user -r requirements.txt
```

---

## 🔒 Security & Best Practices

### API Key Security
- ✅ Store API keys in `.env` file
- ✅ Add `.env` to `.gitignore`
- ✅ Use environment variables in production
- ❌ Never hardcode API keys in source code
- ❌ Never commit API keys to version control

### Development Best Practices
- Use virtual environments for isolation
- Keep dependencies updated
- Follow Python PEP 8 style guidelines
- Test your application before deployment

---

## 🚀 Deployment

### Local Development
The app runs locally on `http://localhost:8501` by default.

### Streamlit Cloud (Recommended)
1. Push your code to GitHub (without `.env` file)
2. Connect your GitHub repo to [Streamlit Cloud](https://streamlit.io/cloud)
3. Add secrets in Streamlit Cloud dashboard
4. Deploy with one click

### Other Platforms
- **Heroku:** Use Heroku buildpacks for Python
- **Docker:** Create a Dockerfile for containerization
- **AWS/GCP:** Deploy using cloud-specific services

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow existing code style
- Add comments for complex logic
- Update documentation for new features
- Test your changes thoroughly

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 AI Travel Planner

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgements

- **[Streamlit](https://streamlit.io/)** - Amazing framework for building web apps
- **[SerpAPI](https://serpapi.com/)** - Reliable search API service
- **[Google Gemini](https://aistudio.google.com/)** - Powerful AI capabilities
- **[Agno Framework](https://pypi.org/project/agno/)** - AI agent orchestration
- **Open Source Community** - For inspiration and support

---

## 📞 Support

Need help? Here are your options:

- **📖 Documentation:** Check this README first
- **🐛 Issues:** [Open an issue on GitHub](https://github.com/yourusername/TravelAssistant-Agent/issues)
- **💬 Discussions:** [Join our discussions](https://github.com/yourusername/TravelAssistant-Agent/discussions)
- **📧 Email:** contact@yourproject.com

---

## 🗺 Roadmap

### Upcoming Features
- [ ] Multi-language support
- [ ] Weather integration
- [ ] Currency converter
- [ ] Offline mode for saved itineraries
- [ ] Social sharing capabilities
- [ ] Mobile app version

### Future Enhancements
- [ ] Real-time price alerts
- [ ] Group travel planning
- [ ] Travel expense tracking
- [ ] Photo gallery integration
- [ ] Review and rating system

---

**Happy travels! ✈️ Start planning your next adventure today!**

---

*Made with ❤️ by the AI Travel Planner Team*
