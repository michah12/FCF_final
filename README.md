# Scentify 💜

A perfume recommendation website that actually helps you find fragrances you'll love.

## What it does

Scentify is basically Spotify but for perfumes (hence the name). You can search through thousands of perfumes, answer a quick questionnaire about your preferences, and get personalized recommendations. The more you use it, the better it gets at knowing your taste.

We built this because honestly, buying perfumes online is a nightmare. You can't smell them, the descriptions are all marketing nonsense, and you end up wasting money on stuff you hate. So we made something that uses real data and machine learning to actually help.

## Getting started

You need Python 3.7 or newer. Then just:

```bash
pip install -r requirements.txt
streamlit run scentify.py
```

That's it. Open your browser and you're good to go.

## How to use it

**Search** - Type in what you're looking for. Filter by gender, price, scent type, whatever. Click on a perfume to see all the details.

**Questionnaire** - Answer some questions about what you like. Takes like 2 minutes. We'll show you perfumes that match your vibe.

**Your Collection** - Save perfumes you own or like. The app learns from this and recommends new ones. The ML kicks in once you've added at least 2 perfumes.

## The tech stuff

- **Streamlit** for the UI (way easier than React, fight me)
- **Plotly** for the charts
- **scikit-learn** for the ML recommendations
- **Fragella API** for the perfume data (you need your own API key)

The recommendation system is pretty straightforward - it learns what accords, seasonality, and longevity you prefer based on your collection, then scores every other perfume in the database. Nothing fancy, but it works.

## API Key

You need a Fragella API key. Make a `.env` file in this folder with:

```
FRAGELLA_API_KEY=your_key_here
```

No key = no perfumes = sad times.

## The data folder

The app creates a `data` folder automatically to store:
- Your perfume collection
- Your interactions (what you clicked, viewed, etc.)
- The trained ML model
- Rankings

Don't delete this unless you want to start over.

## Who made this

Jil, Diego, Luis, Livio, and Micha

We're students who got tired of buying blind and decided to do something about it.

## Issues?

If something breaks, first check:
1. Is your API key valid?
2. Do you have internet?
3. Did you install all the requirements?

Still broken? The code's all in `scentify.py` - probably 90% of issues are from the API or missing dependencies.

---

Made with love (and probably too much coffee) ☕

