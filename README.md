# HappyParents - AI Parenting Assistant & Vaccine Tracker

**An MVP for first-time parents to get AI-powered parenting advice and track their child's vaccinations.**

---

## 🎯 Product Overview

### The Problem
1. New parents lack accessible, immediate guidance for common parenting questions
2. Vaccination tracking is fragmented across paper records and basic apps
3. No integrated solution combines knowledge access with health record management

### The Solution
HappyParents provides:
- **AI Chat Assistant**: Instant, evidence-based parenting advice powered by Claude
- **Vaccination Tracker**: Simple, visual tracking of immunization schedules
- **Zero Setup**: Works immediately in any browser, no account required

---

## 🚀 Quick Start (5 minutes)

### Option 1: GitHub Pages (Recommended for Testing)
1. **Fork this repository** or create a new repo
2. **Upload `index.html`** to your repository
3. Go to **Settings → Pages**
4. Set source to **main branch** and **/ (root)**
5. Your app will be live at `https://yourusername.github.io/happyparents`

### Option 2: Local Development
```bash
# No build needed! Just open the file
open index.html
# or
python -m http.server 8000
# Then visit: http://localhost:8000
```

### Option 3: Deploy to Vercel/Netlify
1. Drag and drop `index.html` into Vercel or Netlify
2. Deploy in seconds

---

## 🔑 Getting Your API Key

1. Visit [console.anthropic.com](https://console.anthropic.com/)
2. Sign up or log in
3. Navigate to **API Keys**
4. Create a new key
5. Copy and paste into the app when prompted

**Cost**: Claude Sonnet 4 costs approximately $0.003 per conversation message. For MVP testing with 10 users having 20 conversations each = ~$0.60 total.

---

## 📋 Features

### MVP (Current Version)
- ✅ AI chat powered by Claude Sonnet 4
- ✅ Multi-child vaccination tracking
- ✅ Indian vaccination schedule (UIP-compliant)
- ✅ Progress visualization
- ✅ Local data persistence (no server needed)
- ✅ Mobile responsive design
- ✅ Zero dependencies (single HTML file)

### Roadmap (Post-MVP)
- 🔲 Export vaccination record as PDF
- 🔲 Push notifications for upcoming vaccines
- 🔲 Multiple country vaccine schedules
- 🔲 Milestone tracking (motor, cognitive, social)
- 🔲 Growth charts
- 🔲 Multi-device sync (requires backend)
- 🔲 Community Q&A
- 🔲 Doctor integration via FHIR

---

## 🏗️ Technical Architecture

### Stack Decisions
- **Single HTML file**: Fastest path to deployment, zero build complexity
- **No backend**: Reduces cost and complexity for MVP
- **localStorage**: Sufficient for single-user testing
- **Claude API**: Best-in-class conversational AI for nuanced parenting advice
- **Vanilla JS**: No framework = faster learning, smaller bundle

### Data Flow
```
User Input → Claude API → Response → localStorage → UI Update
```

### Data Storage (localStorage)
```javascript
{
  anthropic_api_key: "sk-ant-...",
  children: [
    {
      id: 1234567890,
      name: "Emma",
      dob: "2025-01-15",
      vaccines: [
        {
          name: "BCG",
          dueAtMonths: 0,
          completed: true,
          completedDate: "2025-01-15T10:30:00Z"
        }
      ]
    }
  ],
  chat_history: [
    { role: "user", content: "How do I..." },
    { role: "assistant", content: "You can..." }
  ]
}
```

---

## 🎨 Design Principles

1. **Trust through polish**: Parents need to trust health info → professional UI
2. **Progressive disclosure**: Show 5 vaccines, hide the rest → reduce overwhelm
3. **Zero learning curve**: No tutorials needed, intuitive on first use
4. **Mobile-first**: 70% of parents are on mobile during night feedings
5. **Offline-capable**: Works without internet after first load

---

## 🤝 Contributing

This is an MVP for validation. If you want to contribute:

1. **User research**: Interview parents, share findings
2. **Bug fixes**: Open issues with repro steps
3. **Feature ideas**: Describe the problem, not the solution
4. **Internationalization**: Add vaccine schedules for other countries

---

## 📚 Learning Resources

**If you want to learn while building:**
- [Claude API Docs](https://docs.anthropic.com/)
- [Vaccination Schedules](https://www.who.int/immunization/schedules)
- [Product Management for Engineers](https://github.com/ProductHired/pm-for-engineers)

---

## 📞 Support & Feedback

- **Issues**: Open a GitHub issue
- **Ideas**: Start a discussion
- **Questions**: Email or Discord (add your contact)

---

## 📄 License

MIT License - use this however you want! If you build a startup from this, send us a postcard 😊

---

## 🙏 Acknowledgments

- Anthropic for Claude API
- WHO for vaccine schedule data
- First-time parents everywhere who inspired this

---

**Built with ❤️ for sleep-deprived parents**
