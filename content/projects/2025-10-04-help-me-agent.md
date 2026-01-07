---
title: "HelpMe Agent"
summary: "a simple customer service AI chatbot built with LangGraph"
tags: ["ML/AI"]
showTags: true
date: 2025-10-04
---

This project implements a customer service AI chatbot built with LangGraph that can answer frequently asked questions, analyze customer reviews, and request human assistance when needed.

### GitHub repo

[lilyzhouZYJ/help_me_agent](https://github.com/lilyzhouZYJ/help_me_agent)

### Features

- FAQ answering: answers customer questions using a FAQ database
- Customer reviews analysis: analyzes customer reviews using semantic search and LLM-powered classification
- Human-in-the-loop: automatically forwards complex questions to human support via email

### Example usage

```
Welcome
Customer Service AI Chatbot
Ask me anything! Type 'quit' to exit.

You: What are your business hours?

Bot: We are open Monday through Friday from 9:00 AM to 6:00 PM EST, and Saturday from 10:00 AM to 4:00 PM EST. We are closed on Sundays and major holidays.

You: How do customers feel about your wireless headphones?

Bot: Based on customer reviews, customers have mixed feelings about our wireless headphones. The reviews show ratings ranging from 2/5 to 5/5 stars. Positive feedback highlights excellent sound quality, great noise cancellation, and long battery life. However, some customers have reported issues with connection drops, poor sound quality, and discomfort during extended use. The overall sentiment appears to be generally positive, with most reviews being 4-5 stars, but there are some valid concerns about reliability and comfort.

You: Can you help me with a custom software development project?

Bot: I'm sorry, but I don't have enough information to answer your question. 

I've forwarded your inquiry to our human support team at lzhouzyj@gmail.com, and they will get back to you as soon as possible. 

Is there anything else I can help you with based on our frequently asked questions?
```