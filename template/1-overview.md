# Overview

### Elevator pitch

ActualIA is an LLM powered news digest system that analyzes a user's defined news feeds and provides timely, relevant summaries of the day's main events as a personalized podcast, every morning, straight to their headphones.

ActualIA knows what you're interested in, and won't mention any news that isn't relevant to you; if a story caught your eye, you can delve deeper into it, inspect the source and form your own opinion.

An article in a newspaper piques your interest, but you want more context around it? Maybe in your native language? Point your phone's camera at it, and let your customized press team give you the bullet points you need to fully understand it.

---

### In-depth description

ActualIA aims to become the user's main way of interacting with the news. It allows users to define their main news sources (Google News, RSS Feeds, Telegram channels), and their main interests, and from that it centralizes, filters and summarizes the inputs autonomously, succinctly and precisely.

Our product is extensible in many different ways, such as integrating new news sources, different customization options or features altogether, but the core of the app, an AI powered central news hub, remains the same, untouched through iterations and additions. We value the summary generation and reading as the core feature of the MVP, with OCR article inspection as an additional interesting feature.

The app is developed entirely by us, and makes extensive use of interaction with the OpenAI GPT API in order to generate the transcript, and the TTS API for the voice that reads it. Additionally, hard state management and user authentication are taken care of by Supabase, an open-source, self-hostable *backend cloud computing service*. The flexibility it allows over its proprietary counterpart, Firebase, is why it has been chosen by our group.

Our plan is to eventually have an MVP with a account management and an optional paid plan, locking some of the core features (audio generation, for example). The MVP would target both the iOS and Android platforms. For the even farther future, it could be interesting to study ways of detaching from the OpenAI ecosystem, leveraging the RPC nature of our interactions with their model. We could potentially introduce new over-the-counter LLM solutions or custom, in house ones.
