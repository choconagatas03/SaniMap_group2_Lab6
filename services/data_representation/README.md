## Data Representation

The **Comfort Room (Restroom)** resource represents a single restroom facility within Rizal Park (Luneta), including its location, operating hours, accessibility, amenities, and current status. This is the core enterprise resource exchanged between the Comfort Room Registry Service and its consumers (including the reporting service and coverage/monitoring modules).

The system supports both **JSON** and **XML** data formats. Clients specify output preference using standard HTTP Content Negotiation (`Accept: application/json` or `Accept: application/xml`) and indicate request body payload formats using the `Content-Type` header.

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
