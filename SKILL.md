
# ai-trip-planner

Plan trips with AI 鈥� research destinations, build day-by-day itineraries, add events to Google Calendar, find flights and hotels, create packing lists, and export full travel plans. Supports vacation planning, Disney World trips, road trips, international travel, and budget travel.

## When to Use

Use when the user wants to:
- Plan a trip or vacation (any destination)
- Generate a day-by-day travel itinerary
- Research a destination (best time to visit, top attractions, local tips)
- Sync a trip itinerary to Google Calendar
- Create a packing list for a trip
- Plan a Disney World / theme park trip
- Build a road trip route with stops
- Find flights, hotels, or restaurants for a trip
- Create a trip budget breakdown

## Inputs Required

Ask the user for:
1. **Destination(s)** 鈥� city, country, or region (e.g. "Tokyo", "Italy road trip", "Disney World Orlando")
2. **Travel dates** 鈥� departure and return dates (or "flexible" with preferred month)
3. **Number of travelers** 鈥� solo, couple, family (ages of kids), group
4. **Budget level** 鈥� budget / mid-range / luxury (or specific dollar amount)
5. **Interests** (optional): food, culture, adventure, relaxation, nightlife, family activities, shopping, nature
6. **Must-see items** (optional): specific attractions, restaurants, or experiences they already know they want
7. **Departure city** (for flight search)
8. **Special requirements** (optional): dietary restrictions, accessibility needs, pet-friendly

## Workflow Steps

### Step 1: Destination Research

1. Search Google for "[destination] travel guide 2026"
2. Search "[destination] best time to visit"
3. Search "[destination] top things to do"
4. Search Reddit: "[destination] travel tips site:reddit.com"
5. Search "[destination] hidden gems locals recommend"

Compile research into structured brief:
- **Best time to visit** and current weather for their dates
- **Top 15-20 attractions** ranked by popularity and user reviews
- **Neighborhood guide** 鈥� where to stay, eat, explore by area
- **Local tips** 鈥� transportation, tipping, cultural norms, safety
- **Budget estimates** 鈥� average daily cost for meals, transport, activities
- **Events during travel dates** 鈥� festivals, holidays, seasonal activities

### Step 2: Build Day-by-Day Itinerary

Create a detailed itinerary with this structure for each day:

```
DAY [X] 鈥� [Theme/Area Focus] 鈥� [Date]

MORNING (8:00 AM - 12:00 PM)
- 8:00 AM: [Activity] 鈥� [Location] 鈥� [Duration] 鈥� [Cost estimate]
  Notes: [Tips 鈥� e.g. "arrive early to avoid lines", "book tickets online in advance"]
- 10:00 AM: [Activity] 鈥� [Location] 鈥� [Duration] 鈥� [Cost estimate]

LUNCH (12:00 PM - 1:30 PM)
- [Restaurant recommendation] 鈥� [Cuisine type] 鈥� [Price range] 鈥� [Must-try dish]
  Alternative: [Budget/dietary alternative]

AFTERNOON (1:30 PM - 6:00 PM)
- 2:00 PM: [Activity] 鈥� [Location] 鈥� [Duration] 鈥� [Cost estimate]
- 4:00 PM: [Activity or free time] 鈥� [Suggestion]

DINNER (7:00 PM - 9:00 PM)
- [Restaurant recommendation] 鈥� [Cuisine type] 鈥� [Price range]
  Alternative: [Option 2]

EVENING (optional)
- [Nightlife / show / sunset spot suggestion]

TRANSPORT: [How to get between locations 鈥� walk, subway, taxi estimate]
DAY BUDGET: $[estimated total for the day]
```

**Itinerary principles:**
- Group activities by geographic proximity 鈥� minimize transit time
- Alternate high-energy activities with rest/downtime
- Include 1-2 "buffer" slots per day for spontaneous exploration
- Morning activities at popular attractions (fewer crowds)
- Restaurant recommendations should include 1 upscale + 1 budget option
- Include realistic transit times between locations

### Step 3: Disney World / Theme Park Special Module

If destination includes Disney World, Universal, or major theme parks:

1. **Park strategy**: Which parks on which days (based on crowd calendars)
2. **Lightning Lane / Genie+ strategy**: Which rides to prioritize for paid skip-the-line
3. **Rope drop plan**: Arrive 30 min before park opening, first 3 rides to hit
4. **Dining reservations**: Book 60 days in advance 鈥� list must-book restaurants
5. **Rest day schedule**: Pool day or Disney Springs between park days
6. **Budget breakdown**: Tickets + dining plan vs. pay-as-you-go comparison
7. **Kid-specific tips**: Rider swap, baby care centers, character meet schedules
8. Search TouringPlans.com and Disney forums for current wait time patterns

### Step 4: Sync to Google Calendar

For each day of the itinerary, create Google Calendar events:

- **Event title**: "[Activity Name] 鈥� [Location]"
- **Time**: start and end time as specified in itinerary
- **Location**: full address for Google Maps integration
- **Description**: include tips, booking links, cost estimate, and alternatives
- **Color-coding** by type:
  - Activities/Sightseeing: blue
  - Meals/Restaurants: green
  - Transport/Transit: gray
  - Free time/Rest: yellow

Also create:
- An all-day event for each travel day with the day's theme
- Flight events with departure/arrival times and confirmation numbers (if provided)
- Hotel check-in/check-out events

### Step 5: Create Supporting Documents

**Packing List** (in Google Sheet or text):
- Organized by category: Clothing, Toiletries, Electronics, Documents, Medications, Misc
- Customized for destination weather and activities
- Checkbox column for tracking
- Include often-forgotten items: adapter plugs, portable charger, sunscreen, copies of passport

**Budget Tracker** (Google Sheet):
- Pre-filled with estimated costs from itinerary
- Categories: Flights, Hotels, Activities, Food, Transport, Shopping, Emergency Fund
- Columns: Item | Estimated Cost | Actual Cost | Difference
- Summary row with totals and budget remaining
- Per-person and total cost views for group trips

**Booking Checklist** (Google Sheet):
- List of everything that needs to be booked in advance
- Columns: Item | Book By Date | Booking Link | Confirmation # | Status
- Sorted by urgency (book soonest first)
- Items like: flights, hotels, restaurant reservations, museum tickets, tours, car rental, travel insurance

### Step 6: Flight and Hotel Research (Optional)

If user wants flight/hotel suggestions:
1. Search Google Flights for "[departure] to [destination]" on their dates
2. Note top 3-5 options with prices, airlines, layovers
3. Search Google Hotels or Booking.com for accommodation
4. Recommend by budget tier:
   - Budget: hostels, Airbnb, budget hotels
   - Mid-range: 3-4 star hotels, well-reviewed Airbnbs
   - Luxury: 5-star hotels, boutique properties
5. Include neighborhood recommendation for where to stay

## Template Library

When user asks for "trip planner template" or wants a blank framework:

### Weekend Getaway (2-3 days)
- Day 1: Arrival + neighborhood exploration + dinner
- Day 2: Full day of activities + lunch at local favorite
- Day 3: Morning activity + departure

### One-Week Vacation (7 days)
- Day 1: Arrival, settle in, neighborhood walk, light dinner
- Day 2-3: Major attractions and landmarks
- Day 4: Day trip or off-the-beaten-path exploration
- Day 5: Cultural experience (museum, cooking class, local market)
- Day 6: Relaxation + shopping + farewell dinner
- Day 7: Last morning activity + departure

### Disney World 5-Day Plan
- Day 1: Magic Kingdom (rope drop, fireworks)
- Day 2: EPCOT (World Showcase, evening show)
- Day 3: Rest day 鈥� pool, Disney Springs shopping
- Day 4: Hollywood Studios (Rise of Resistance, Tower of Terror)
- Day 5: Animal Kingdom morning + departure afternoon

### Road Trip Template
- For each stop: Drive time from previous stop, gas estimate, top 2-3 things to do, recommended meal stop, overnight accommodation

## Quality Standards

- All restaurant and attraction recommendations must be based on actual web research, not fabricated names
- Transit time estimates must be realistic 鈥� verify with Google Maps
- Budget estimates should be specific dollar amounts, not vague ranges
- Disney/theme park advice must reference current ticket prices and policies (search live)
- Calendar events must have correct time zones for the destination
- Packing lists must be customized for the actual destination weather and activities 鈥� no generic lists
- Include booking deadlines and advance-notice requirements (e.g. "Disney dining reservations open 60 days before")
