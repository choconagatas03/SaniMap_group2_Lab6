## Data Representation

The **Comfort Room (Restroom)** resource represents a single restroom facility within Rizal Park (Luneta), including its location, operating hours, accessibility, amenities, and current status. This is the core enterprise resource exchanged between the Comfort Room Registry Service and its consumers (the frontend, the Appointment/ Reporting service equivalent, and the Coverage & Monitoring service).


### Resource Schema

| Field | Type | Description |
| :--- | :--- | :--- |
| "restroomId" | integer | Unique identifier for the comfort room |
| "name" | string | Display name / landmark reference |
| "latitude" | number | Latitude coordinate|
| "longitude" | number | Longitude coordinate |
| "operatingHours" | string | Hours the facility is open, |
| "pwdAccessible" | boolean | Whether the facility is PWD-accessible |
| "genderType" | string | Unisex, Male/Female, etc. |
| "amenities" | array of strings | Available facilities, e.g., handwashing station, soap |
| "status" | string | "open", "closed", or "under_maintenance"  |

### Example Payloads

#### JSON Format
{
  "restroomId": 101,
  "name": "Rizal Monument Comfort Room",
  "latitude": 14.5826,
  "longitude": 120.9787,
  "operatingHours": "06:00-20:00",
  "pwdAccessible": true,
  "genderType": "Unisex",
  "amenities": [
    "handwashing station",
    "soap"
  ],
  "status": "open"
}
<img width="744" height="296" alt="image" src="https://github.com/user-attachments/assets/0ee1de95-440b-4b88-97ef-14b2a78c5c1f" />

