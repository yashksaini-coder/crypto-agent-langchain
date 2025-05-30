`pip install -r requirements.txt`
`python main.py`


Sample input:
```json
{
  "query": "how is monalisa doing?",
  "min_articles": 3,
  "additional_context": {
    "token_data": {
      "token_name": "MONALISA",
      "current_price_usd": 0.052599,
      "market_cap": "$2.60K",
      "liquidity": "$4.88K",
      "total_supply": "1000M",
      "performance": {
        "1h": "0%",
        "6h": "0%",
        "24h": "+5%"
      },
      "trading_metrics": {
        "transactions": 4,
        "volume": "$48",
        "buys": 2,
        "sells": 2,
        "buy_volume": "$43",
        "sell_volume": "$6"
      },
      "recent_trades": [
        {
          "type": "BUY",
          "age": "5h",
          "amount": "993K",
          "total_sol": "0.0200",
          "total_usd": "$2.66",
          "maker": "RRD1oj"
        },
        {
          "type": "BUY",
          "age": "5h",
          "amount": "15M",
          "total_sol": "0.29985",
          "total_usd": "$39.85",
          "maker": "5S6tDv"
        },
        {
          "type": "SELL",
          "age": "6h",
          "amount": "797K",
          "total_sol": "0.0155",
          "total_usd": "$2.04",
          "maker": "bvATGU"
        },
        {
          "type": "SELL",
          "age": "11h",
          "amount": "1M",
          "total_sol": "0.0289",
          "total_usd": "$3.82",
          "maker": "xw61Fn"
        },
        {
          "type": "SELL",
          "age": "1d",
          "amount": "91K",
          "total_sol": "0.0018",
          "total_usd": "$0.21",
          "maker": "FV2pGg"
        }
      ]
    }
  }
}
```


sample output:
```json
{
  "query": "how is monalisa doing?",
  "answer": "Okay, let's dive into how MONALISA is doing. Currently, it's priced at $0.052599, with a market cap of $2.60K and liquidity of $4.88K. Looking at the recent performance, it's flat over the last hour and 6 hours, but it's up 5% in the last 24 hours. Trading activity shows 4 transactions, with a total volume of $48, split evenly between buys and sells. The buy volume is slightly higher at $43 compared to the sell volume of $6. Recent trades include a couple of buys totaling around $42.51 and sells totaling around $5.86. Overall, the data suggests a micro-cap token with very low liquidity and trading volume. The tweets are a mixed bag, with some users promoting 'MONALISAChallenge' events and others mentioning it in the context of other tokens or memes. One tweet even references a Solana token, $Giza, alongside #jhope_MONALISA, indicating some association with the challenge.",
  "sentiment": "Neutral",
  "context": "Shows community engagement and marketing efforts around the token, potentially driving awareness. Indicates the token is being discussed in the context of other crypto opportunities and trends, though not necessarily driving value. Positions the token within the meme coin space, which can influence its volatility and appeal.",
  "trending_topics": [
    "MONALISAChallenge",
    "Micro-cap token",
    "Low Liquidity",
    "Social Media Engagement",
    "jhope_MONALISA"
  ],
  "articles": [
    {
      "title": "Tweet by @Solcaller1",
      "summary": "Solana token $Giza just locked in a massive 355.91x gain! 🌕🚀\n\nStarted at a $2.20k market cap, and  to $783k 👇\n\nCome to my TG channel so you don't miss more opportunities. 💵\n\n#TolakRUUTNI #jhope_MONALISA #Crypto #LYKN #Solana #Memecoins #Trump #薬屋のひとりごと #Altcoins https://pbs.twimg.com/media/Gmlv1V-aEAIc4Tq.jpg\n\nQuoting @Solcaller1: Highlighted solana token $Giza at $2.2k Mcap in my private TG Channel.\n\n#TolakRUUTNI #JHOPE #SB19 #Solana #memecoins #CryptoPump #AltcoinsPump #Degen #PakistanCricket #LYKN https://pbs.twimg.com/media/GmlvjTXWAAAM2TQ.jpg",
      "media": null,
      "link": "https://twitter.com/Solcaller1/status/1903175351863590989",
      "authors": null,
      "published": "Fri Mar 21 20:02:17 +0000 2025",
      "category": "Social Media",
      "subCategory": "Twitter",
      "language": null,
      "timeZone": null
    },
    {
      "title": "Tweet by @taesoothe",
      "summary": "#MONALISAChallenge event for a special gift for 50 people 👀 and they accept not only tiktok but all major platforms, shorts, reels, and so... very nice https://video.twimg.com/ext_tw_video/1902966658055995392/pu/vid/avc1/320x568/b07XQA5kkUQZ8nfQ.mp4?tag=12\n\nQuoting @bts_bighit: [공지] j-hope 'MONA LISA' Dance Challenge EVENT 안내 (+ENG/JPN/CHN) \n\n🔗 https://weverse.io/bts/notice/25787\n\n#jhope #제이홉 #jhope_MONALISA #MONALISAChallenge",
      "media": null,
      "link": "https://twitter.com/taesoothe/status/1902966692256325986",
      "authors": null,
      "published": "Fri Mar 21 06:13:09 +0000 2025",
      "category": "Social Media",
      "subCategory": "Twitter",
      "language": null,
      "timeZone": null
    },
    {
      "title": "Tweet by @CharizardTokenX",
      "summary": "$CHAR\n\nDo you like the new Charalisa?\n\nDa Vinci would’ve been impressed..\n\n#charizard\n#memecoin\n#crypto\n#trump\n#elon\n#tate\n#michaelsaylor\n#monalisa https://pbs.twimg.com/media/GluMFmTXsAAqqja.jpg",
      "media": null,
      "link": "https://twitter.com/CharizardTokenX/status/1899265700453073147",
      "authors": null,
      "published": "Tue Mar 11 01:06:44 +0000 2025",
      "category": "Social Media",
      "subCategory": "Twitter",
      "language": null,
      "timeZone": null
    }
  ],
  "article_analysis": [
    {
      "title": "Tweet by @taesoothe",
      "key_points": "Highlights the #MONALISAChallenge event across various social media platforms.",
      "significance": "Shows community engagement and marketing efforts around the token, potentially driving awareness."
    },
    {
      "title": "Tweet by @Solcaller1",
      "key_points": "Mentions #jhope_MONALISA alongside a Solana token $Giza.",
      "significance": "Indicates the token is being discussed in the context of other crypto opportunities and trends, though not necessarily driving value."
    },
    {
      "title": "Tweet by @CharizardTokenX",
      "key_points": "References 'Charalisa' and includes hashtags like #memecoin and #crypto.",
      "significance": "Positions the token within the meme coin space, which can influence its volatility and appeal."
    }
  ],
  "processed_at": "2025-04-13T14:31:58.453665"
}
```
