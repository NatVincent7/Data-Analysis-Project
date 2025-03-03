# Data Dictionary: Google Analytics Sample (ga_sessions_20170801)

**Table Name:** `ga_sessions_20170801`  
**Description:**  
This table contains session-level data for the Google Merchandise Store. It includes visitor identifiers, session timestamps, and summary metrics stored in nested fields. For our CLV Prediction and Customer Segmentation project, we focus on key fields from the main table and its nested records.

---

## Main Table Fields

| Field Name     | Data Type         | Description                                     | Notes                       |
|----------------|-------------------|-------------------------------------------------|-----------------------------|
| visitorId      | STRING            | Unique identifier for the visitor               | Primary identifier          |
| visitNumber    | INTEGER           | Sequential visit number for the visitor         |                             |
| visitId        | INTEGER           | Unique session identifier                       |                             |
| visitStartTime | TIMESTAMP         | Start time of the session                       |                             |
| date           | STRING (YYYYMMDD) | Date of the session                             |                             |
| fullVisitorId  | STRING            | Another unique identifier (often similar to visitorId) |                    |

---

## Nested Records

### 1. `totals`
*Contains aggregate session-level metrics.*

| Field Name           | Data Type | Description                                                         | Notes                                           |
|----------------------|-----------|---------------------------------------------------------------------|-------------------------------------------------|
| visits               | INTEGER   | Number of visits in the session (usually 1 per session)             |                                                 |
| hits                 | INTEGER   | Total hits in the session                                           |                                                 |
| pageviews            | INTEGER   | Total pageviews recorded                                            | May be null if not applicable                   |
| timeOnSite           | INTEGER   | Total time spent on site during the session (in seconds)            |                                                 |
| bounces              | INTEGER   | Indicator if the session was a bounce (1 if bounced, 0 otherwise)     |                                                 |
| transactions         | INTEGER   | Number of transactions that occurred                                | May be null if no transaction occurred          |
| transactionRevenue   | FLOAT     | Revenue generated from transactions (often stored in micros)        | Scale as needed to convert to standard currency  |
| newVisits            | INTEGER   | Indicator if the session was a new visit                             |                                                 |

---

### 2. `trafficSource`
*Provides information on the session's marketing origin.*

| Field Name   | Data Type | Description                                    | Notes                              |
|--------------|-----------|------------------------------------------------|------------------------------------|
| referralPath | STRING    | Referral path of the traffic source             | May be null                        |
| campaign     | STRING    | Marketing campaign associated with the session  |                                    |
| source       | STRING    | Traffic source (e.g., google, direct, referral)   |                                    |
| medium       | STRING    | Traffic medium (e.g., organic, CPC)              |                                    |
| keyword      | STRING    | Search keyword used (if applicable)              |                                    |

---

### 3. `device`
*Contains information about the visitor’s device.*

| Field Name         | Data Type | Description                                    | Notes                    |
|--------------------|-----------|------------------------------------------------|--------------------------|
| browser            | STRING    | Browser used by the visitor                    |                          |
| operatingSystem    | STRING    | Visitor’s operating system                     |                          |
| deviceCategory     | STRING    | Type of device (desktop, mobile, tablet)       |                          |

---

### 4. `geoNetwork`
*Provides geographic information about the visitor.*

| Field Name  | Data Type | Description         | Notes    |
|-------------|-----------|---------------------|----------|
| continent   | STRING    | Continent           |          |
| country     | STRING    | Country             |          |
| region      | STRING    | Region or state     |          |
| city        | STRING    | City                |          |

---

### 5. `hits` (Repeated Record)
*Holds detailed event-level data for each session.*

| Field Name                  | Data Type  | Description                                              | Notes                                      |
|-----------------------------|------------|----------------------------------------------------------|--------------------------------------------|
| hitNumber                   | INTEGER    | Sequential number of the hit within the session          |                                            |
| time                        | INTEGER    | Time offset (in seconds) from session start              |                                            |
| page.pagePath               | STRING     | URL path of the page hit                                 |                                            |
| eventInfo.eventCategory     | STRING     | Category of event (if applicable)                        |                                            |
| eventInfo.eventAction       | STRING     | Action performed (if applicable)                         |                                            |

*Note:* You can expand this section if you need more details (e.g., transaction or promotion fields).

---

## Relationships

- **Main Table & Totals:**  
  The `totals` nested record provides session-level summary metrics (e.g., pageviews, transactions, revenue).

- **Main Table & trafficSource:**  
  The `trafficSource` nested record details the origin of the session, which can be used to analyze marketing effectiveness.

- **Main Table & Device/GeoNetwork:**  
  These nested records provide context on the visitor’s device and geographic location.

- **Unnesting Hits:**  
  If needed, you can unnest the `hits` field to analyze detailed event-level data. Use keys like `visitorId` and `visitId` to link hit-level data back to session-level data.

---

*This template focuses on the most relevant tables and nested records for an e-commerce CLV prediction project. You can adjust or expand the documentation as you explore the dataset further.*

