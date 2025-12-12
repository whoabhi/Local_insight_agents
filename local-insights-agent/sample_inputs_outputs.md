# Sample Inputs & Outputs
This document contains example requests and responses for the Local Insights Agent.
Use these examples for testing and integration.

Note:
For the full JSON output format, refer to README.md → Output Schema.

---

## TEST CASE 1: Sunny Afternoon (Jaipur)

### Input JSON
{
  "user_id":"sampleA",
  "location":{"city":"Jaipur","lat":26.9124,"lng":75.7873},
  "date_time":"2026-03-07T15:00:00+05:30",
  "trip_dates":{"start":"2026-03-06","end":"2026-03-09"},
  "interests":["culture","photography"],
  "budget_level":"mid",
  "current_itinerary_slot":{"day":2,"start_time":"14:00","end_time":"18:00"},
  "risk_tolerance":"medium"
}

### Output JSON (sample)
{
  "recommendations":[
    {
      "id":"rec_1",
      "title":"Albert Hall Museum",
      "type":"cultural",
      "best_time":"16:00-18:00",
      "best_season":"October–March",
      "why":"Great late-afternoon light for photos and nearby crafts stalls.",
      "weather_ok":"yes",
      "crowd_level":"medium",
      "estimated_time":"1–2 hours",
      "estimated_cost":"₹100",
      "safety_note":null,
      "local_tip":"Try the famous nearby lassi.",
      "food_nearby":["Lassiwala","Handicraft Street Snacks"],
      "booking_link":null,
      "score":88,
      "confidence":0.88
    }
  ],
  "summary":"Albert Hall is ideal for late-afternoon photography with local crafts.",
  "data_issues":[]
}

---

## TEST CASE 2: Rainy Morning (Shimla)

### Input JSON
{
  "user_id":"sampleB",
  "location":{"city":"Shimla","lat":31.1048,"lng":77.1734},
  "date_time":"2026-06-12T09:00:00+05:30",
  "trip_dates":{"start":"2026-06-12","end":"2026-06-15"},
  "interests":["nature","food"],
  "budget_level":"low",
  "current_itinerary_slot":{"day":1,"start_time":"08:00","end_time":"12:00"},
  "risk_tolerance":"low"
}

### Output JSON (sample)
{
  "recommendations":[
    {
      "id":"rec_1",
      "title":"Indian Institute of Advanced Study",
      "type":"indoor",
      "best_time":"10:00-12:00",
      "best_season":"All year",
      "why":"Indoor attraction ideal during rain with rich architecture.",
      "weather_ok":"no",
      "crowd_level":"low",
      "estimated_time":"1–2 hours",
      "estimated_cost":"₹50",
      "safety_note":"Avoid slippery hillside paths.",
      "local_tip":"Carry a compact umbrella.",
      "food_nearby":["Mall Road Cafés"],
      "booking_link":null,
      "score":80,
      "confidence":0.80
    }
  ],
  "summary":"Indoor museum suits rainy morning; avoid slippery outdoors.",
  "data_issues":[]
}

---

## TEST CASE 3: Night Safety Scenario (Kolkata)

### Input JSON
{
  "user_id":"sampleC",
  "location":{"city":"Kolkata","lat":22.5726,"lng":88.3639},
  "date_time":"2026-12-24T21:30:00+05:30",
  "trip_dates":{"start":"2026-12-24","end":"2026-12-26"},
  "interests":["food","nightlife"],
  "budget_level":"mid",
  "current_itinerary_slot":{"day":1,"start_time":"20:00","end_time":"23:59"},
  "risk_tolerance":"low"
}

### Output JSON (sample)
{
  "recommendations":[
    {
      "id":"rec_1",
      "title":"Park Street Restaurants",
      "type":"food",
      "best_time":"20:00-23:00",
      "best_season":"December–February",
      "why":"Well-lit area with food options suitable for safe night outings.",
      "weather_ok":"yes",
      "crowd_level":"medium",
      "estimated_time":"1–2 hours",
      "estimated_cost":"mid",
      "safety_note":"Avoid isolated lanes after 11 PM.",
      "local_tip":"Use prepaid rides for return.",
      "food_nearby":["Flurys","Peter Cat"],
      "booking_link":null,
      "score":82,
      "confidence":0.82
    }
  ],
  "summary":"Park Street provides a safe, well-lit night dining experience.",
  "data_issues":[]
}

---

## END OF TEST CASES
These examples help developers understand:
- Expected agent behavior  
- JSON structure and keys  
- Safety and weather handling  
- Scoring and confidence logic  

Refer to README.md for full schema rules.
