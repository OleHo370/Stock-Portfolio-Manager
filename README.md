One month ago, I wanted to investigate a simple problem: where you’ll often see people trying to find volatile, high-risk stocks with the highest returns, instead, I wanted to see if it was possible to create a risk-free portfolio that preserves your initial investment. 

Goal: 𝗪𝗶𝘁𝗵 𝗮𝗻 𝗶𝗻𝗶𝘁𝗶𝗮𝗹 $𝟭,𝟬𝟬𝟬,𝟬𝟬𝟬 𝗶𝗻𝘃𝗲𝘀𝘁𝗺𝗲𝗻𝘁, 𝗰𝗿𝗲𝗮𝘁𝗲 𝗮 𝗽𝗼𝗿𝘁𝗳𝗼𝗹𝗶𝗼 𝗼𝗳 𝟮𝟱 𝘀𝘁𝗼𝗰𝗸𝘀 𝘄𝗵𝗼𝘀𝗲 𝘃𝗮𝗹𝘂𝗲 𝘀𝘁𝗮𝘆𝘀 𝗮𝘀 𝗰𝗹𝗼𝘀𝗲 𝘁𝗼 $𝟭,𝟬𝟬𝟬,𝟬𝟬𝟬 𝗶𝗻 𝗮𝗯𝘀𝗼𝗹𝘂𝘁𝗲 𝘃𝗮𝗹𝘂𝗲 𝗼𝘃𝗲𝗿 𝘁𝗶𝗺𝗲 𝗮𝘀 𝗽𝗼𝘀𝘀𝗶𝗯𝗹𝗲 (𝘇𝗲𝗿𝗼 𝗿𝗲𝘁𝘂𝗿𝗻𝘀), 𝗲𝗻𝘀𝘂𝗿𝗶𝗻𝗴 𝗹𝗼𝘄 𝘃𝗼𝗹𝗮𝘁𝗶𝗹𝗶𝘁𝘆 𝗮𝗻𝗱 𝗿𝗶𝘀𝗸. 

Using 𝗣𝘆𝘁𝗵𝗼𝗻, 𝗣𝗮𝗻𝗱𝗮𝘀, 𝗡𝘂𝗺𝗣𝘆, 𝗠𝗮𝘁𝗽𝗹𝗼𝘁𝗹𝗶𝗯, 𝗮𝗻𝗱 𝗬𝗙𝗶𝗻𝗮𝗻𝗰𝗲 𝗔𝗣𝗜, we built an algorithm that:
• Parses CSV files with 𝟭,𝟬𝟬𝟬+ random stock tickers, with the code being able to analyze a sample file of 𝟮𝟬𝟬 𝘁𝗶𝗰𝗸𝗲𝗿𝘀 𝘄𝗶𝘁𝗵𝗶𝗻 𝟮 𝗺𝗶𝗻𝘂𝘁𝗲𝘀
• Removes invalid tickers, stocks with low trading volumes, and non-US/Canadian companies
• Evaluates each stock based on quantitative metrics, including 𝗕𝗲𝘁𝗮, 𝗘𝘅𝗽𝗲𝗰𝘁𝗲𝗱 𝗠𝗼𝗻𝘁𝗵𝗹𝘆 𝗥𝗲𝘁𝘂𝗿𝗻𝘀, 𝗮𝗻𝗱 𝗦𝘁𝗮𝗻𝗱𝗮𝗿𝗱 𝗗𝗲𝘃𝗶𝗮𝘁𝗶𝗼𝗻
• Compiles these metrics into a safety score and ranks the stocks from highest to lowest
• Implements a 𝗴𝗿𝗲𝗲𝗱𝘆 𝗮𝗹𝗴𝗼𝗿𝗶𝘁𝗵𝗺 that adds one stock into the portfolio at a time, choosing stocks with 𝗹𝗼𝘄 𝗮𝘃𝗲𝗿𝗮𝗴𝗲 𝗰𝗼𝗿𝗿𝗲𝗹𝗮𝘁𝗶𝗼𝗻 with other stocks in the portfolio to reduce risk clustering
• Tracks and chooses stocks from a variety of sectors to improve 𝗱𝗶𝘃𝗲𝗿𝘀𝗶𝗳𝗶𝗰𝗮𝘁𝗶𝗼𝗻

I simulated a $1,000,000 portfolio of the 25 stocks that the portfolio creator picked for one month (December 6th, 2025 to January 6th, 2026), and here are the results:
• Final portfolio value of $𝟭,𝟬𝟬𝟯,𝟯𝟲𝟴.𝟴𝟯 and 𝟬.𝟯𝟰% return; very close to our goal of $1,000,000 and 0% returns
• Daily volatility of 𝟬.𝟱𝟲𝟳𝟬% and an annualized volatility of 𝟵%. For reference, the S&P 500 has an annualized volatility of 15-20%, so our model beats out the S&P 500 in terms of reducing risk.
<img width="2048" height="1084" alt="image" src="https://github.com/user-attachments/assets/2ccc9973-c877-4ed7-90f9-1cdd02aac5b8" />
<img width="2048" height="988" alt="image" src="https://github.com/user-attachments/assets/5c303f85-c2cb-46ee-8419-fcfc23a20518" />
<img width="1992" height="1170" alt="image" src="https://github.com/user-attachments/assets/49384151-375d-48eb-a80d-5ee53c75f198" />
<img width="2033" height="1174" alt="image" src="https://github.com/user-attachments/assets/030d04ba-a7bc-47bf-80a8-19433e320263" />
