# When AI Meets Finance (AstraQuant): LLM-Driven Stock Trading in Realistic Simulation

Can AI agents actually behave like real investors when markets react to things like macro trends, policy shifts, earnings, or global events? These external signals shape trading decisions every day, and they matter a lot when you care about returns.

AstraQuant is my attempt at answering that. It is a multi agent trading simulator powered by large language models, built to study how investors respond to real market conditions. With AstraQuant, you can test how different external factors influence trading behavior and profitability, and analyze how agents react across scenarios.

A key detail: AstraQuant is designed to avoid test data leakage. The agents do not get prior knowledge of the evaluation period, so their decisions reflect only what is realistically available at the time.

I evaluate multiple LLMs inside this framework and place them in a trading setup that closely mirrors real world environments. The results highlight how external signals shape market activity, price movement, and trading styles. The work also looks at how agents behave when they operate without prior knowledge of the data they trade on.

Overall, the takeaways from AstraQuant help inform how LLMs might be used for real investing workflows like trading insights and stock recommendation.



The trading simulation runs in four phases: **Initial Phase**, **Trading Phase**, **Post Trading Phase**, and **Special Events Phase**. Daily and quarterly events happen during the Post Trading Phase, while Special Events are random and applied on a random trading day.

## Quick Start

#### Environment

conda create --name AstraQuant python=3.9
conda activate AstraQuant

git clone https://github.com/dhh1995/PromptCoder
cd PromptCoder
pip install -e .
cd ..

git clone <This Github Project>
cd AstraQuant
pip install -r requirements.txt

#### API Keys

Use GPT models as the agent LLM:

export OPENAI_API_KEY=YOUR_OPENAI_API_KEY

Use Gemini as the agent LLM:

export GOOGLE_API_KEY=YOUR_GEMINI_API_KEY

#### Run a simulation

Pick a base LLM and start:

python main.py --model MODEL_NAME

By default, the system uses gemini-pro.

#### About `procoder`

This project uses PromptCoder:
https://github.com/dhh1995/PromptCoder.git
Install it before running AstraQuant.
