# Local Insights Agent  
A hyperlocal, context-aware AI module designed for multi-agent travel planning systems.  
This agent enriches travel recommendations with local insights, cultural notes, weather suitability, crowd levels, hidden gems, and safety information.

---

## 🌍 Overview

The **Local Insights Agent** provides real-time, locally relevant information about destinations and activities.  
It acts as an intelligent assistant within a larger agentic ecosystem that may include:

- Hidden Gems Agent  
- Itinerary Agent  
- Budget Agent  
- Travel & Accommodation Agent  

Its goal is to help travelers make better decisions by offering rich local knowledge — similar to advice from someone who lives in that destination.

---

## 🎯 Responsibilities

The agent:
- Receives destination + travel details  
- Enhances each activity with deep local intelligence  
- Suggests best time of day & season to visit  
- Identifies safety risks  
- Provides crowd expectations  
- Adds nearby food recommendations  
- Offers localized cultural notes & micro-tips  
- Generates a structured JSON output for integration  

It does **not**:
- Create full itineraries  
- Calculate total budgets  
- Perform bookings  
- Replace other agents’ tasks  

---

## 📥 Input Format (Schema)

Expected JSON input:

```json
{
  "user_id": "string",
  "location": {
    "city": "string",
    "lat": number,
    "lng": number
  },
  "date_time": "YYYY-MM-DDTHH:MM:SS+05:30",
  "trip_dates": {
    "start": "YYYY-MM-DD",
    "end": "YYYY-MM-DD"
  },
  "interests": ["string"],
  "budget_level": "low | mid | high",
  "current_itinerary_slot": {
    "day": number,
    "start_time": "HH:MM",
    "end_time": "HH:MM"
  },
  "risk_tolerance": "low | medium | high"
}
