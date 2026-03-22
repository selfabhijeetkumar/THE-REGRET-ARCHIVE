# ✦ The Regret Archive
### *A Living Museum of Human Regret*

> *"Every regret is a lesson whispered by time. Here, they find a home among the stars."*

![The Regret Archive](https://img.shields.io/badge/Status-Live-gold?style=for-the-badge&color=c9a96e)
![HTML](https://img.shields.io/badge/HTML-Pure-orange?style=for-the-badge&logo=html5)
![Three.js](https://img.shields.io/badge/Three.js-3D-black?style=for-the-badge&logo=three.js)
![Supabase](https://img.shields.io/badge/Supabase-Database-green?style=for-the-badge&logo=supabase)
![Gemini AI](https://img.shields.io/badge/Gemini-AI-blue?style=for-the-badge&logo=google)

---

## 🌌 What Is This?

**The Regret Archive** is a dark, cinematic, emotionally powerful web experience where people anonymously submit their biggest life regrets. Google Gemini AI categorizes and reflects on each submission, and they are visualized as a **living 3D galaxy of human emotion.**

This is not just a website. It is a **digital cathedral** — a sacred space where human vulnerability becomes art.

---

## ✨ Features

- 🌌 **Interactive 3D Galaxy** — Every regret becomes a glowing orb in space. Hover to read it. Click to feel it.
- 🤖 **AI Reflections** — Google Gemini AI analyzes each regret and generates a poetic, compassionate response
- 🎨 **Cinematic Design** — Dark luxury aesthetic with gold accents, glassmorphism cards, and Three.js animations
- 📝 **Anonymous Submissions** — No account needed. No name. No trace. Just truth.
- 🏛️ **Living Wall** — Masonry grid of real regrets with category filters
- 📊 **Personal Dashboard** — Stats, category breakdown, and your personal mini galaxy
- 🌍 **World Regret Map** — See where pain lives across the globe
- 💌 **Daily Reflection Prompts** — A new question every day to inspire deeper thinking
- 🃏 **Shareable Cards** — Generate beautiful image cards to share your regret on social media

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Pure HTML/CSS/JS** | Single file, no frameworks, no build tools |
| **Three.js** | 3D galaxy visualization and particle systems |
| **GSAP + ScrollTrigger** | Cinematic scroll animations |
| **Supabase** | Database and real-time backend |
| **Google Gemini AI** | Regret analysis and reflection generation |
| **Chart.js** | Dashboard charts and visualizations |

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/selfabhijeetkumar/the-regret-archive.git
cd the-regret-archive
```

### 2. Set up Supabase
1. Go to [supabase.com](https://supabase.com) and create a free project
2. Run this SQL in your Supabase SQL Editor:

```sql
CREATE TABLE regrets (
  id uuid DEFAULT gen_random_uuid() PRIMARY KEY,
  regret_text text NOT NULL,
  age_group text,
  country text,
  category text NOT NULL,
  ai_reflection text NOT NULL,
  ai_teaching text NOT NULL,
  is_public boolean DEFAULT false,
  created_at timestamptz DEFAULT now()
);

ALTER TABLE regrets ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Allow anonymous inserts" ON regrets
  FOR INSERT TO anon WITH CHECK (true);

CREATE POLICY "Allow public reads" ON regrets
  FOR SELECT TO anon USING (true);
```

### 3. Get your free Gemini API Key
1. Go to [aistudio.google.com](https://aistudio.google.com)
2. Click **"Get API Key"** → Create new key (free, no credit card)

### 4. Add your keys
Open `index.html` and fill in your keys at the top:

```javascript
const CONFIG = {
  SUPABASE_URL: 'YOUR_SUPABASE_URL',
  SUPABASE_ANON_KEY: 'YOUR_SUPABASE_ANON_KEY',
  GEMINI_API_KEY: 'YOUR_GEMINI_API_KEY',
};
```

### 5. Open in browser
```
Just open index.html in any browser. Done. 🌌
```

---

## 📁 Project Structure

```
the-regret-archive/
│
└── index.html          ← The entire app (HTML + CSS + JS)
```

Yes. The **entire application** is one single HTML file. No npm. No build tools. No frameworks. Pure web.

---

## 🎨 Design System

| Element | Value |
|---|---|
| Background | `#080808` |
| Gold Accent | `#c9a96e` |
| Warm White | `#f0ebe0` |
| Heading Font | DM Serif Display |
| Body Font | Inter |
| Card Style | Glassmorphism |

### Category Colors
| Category | Color |
|---|---|
| Love | `#e74c6f` |
| Career | `#4ca6e7` |
| Family | `#6fe74c` |
| Courage | `#e7a84c` |
| Money | `#9b59b6` |
| Time | `#c084fc` |
| Identity | `#f97316` |

---

## 🌐 Deploy for Free

### Netlify (Easiest)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop `index.html`
3. Get a live link instantly ✅

### GitHub Pages
1. Go to your repo Settings
2. Pages → Deploy from main branch
3. Live at: `https://selfabhijeetkumar.github.io/the-regret-archive`

---

## 💡 How It Works

```
User types regret
      ↓
Gemini AI analyzes it
      ↓
Returns: category + reflection + teaching
      ↓
Saved to Supabase database
      ↓
Appears as glowing bubble in 3D galaxy
      ↓
Added to the Living Wall
      ↓
Contributes to the collective human story
```

---

## 🔒 Privacy

- **Zero personal data collected** — no names, no emails, no accounts
- All submissions are completely anonymous
- IP addresses are never stored
- You cannot trace any regret back to any person

---

## 🤝 Contributing

This is an open project. If you want to contribute:

1. Fork the repo
2. Make your changes in `index.html`
3. Submit a pull request

Ideas welcome — especially for new visualization modes, AI improvements, or performance optimizations.

---

## 📸 Screenshots

> *Add your screenshots here after deployment*

---

## 👤 Author

**Abhijeet Kumar**
- GitHub: [@selfabhijeetkumar](https://github.com/selfabhijeetkumar)
- LinkedIn: [Abhijeet Kumar](https://linkedin.com/in/selfabhijeetkumar)

---

## ⭐ Support

If this project moved you, made you think, or helped you feel less alone —

**Give it a star ⭐ on GitHub.**

That's all the support needed.

---

## 📜 License

MIT License — free to use, modify, and share.

---

<div align="center">

*"We are all walking collections of the paths not taken,*
*the words not spoken, the chances not seized."*

**— The Regret Archive**

</div>
