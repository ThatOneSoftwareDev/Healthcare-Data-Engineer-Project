# Patient Vital Monitoring Pipeline

<img src="https://i.postimg.cc/mgdFVC2Q/headshot.png" align="right"
     alt="Size Limit logo by Anton Lovchikov" height="178">

Patient Vital Monitoring Pipeline is a real-time data system that ingests, processes, and stores patient health data from medical devices to enable fast monitoring and analytics.

- Real-time streaming ingestion using Pub/Sub to capture patient vital signs as they are generated.
- Layered data processing (bronze, silver, gold) to clean, validate, and transform raw medical data into reliable insights.
- Cloud Storage staging layer used to temporarily hold incoming data before transformation.
- BigQuery data warehouse for scalable storage and fast querying of processed patient health metrics.
- Alerting and monitoring support to detect abnormal vitals and trigger timely notifications.
- Scalable architecture designed to handle high-frequency healthcare data from multiple sources in real time.

<p align="center">
  <img src="https://i.postimg.cc/SNC20HSd/Chat-GPT-Image-Apr-22-2026-02-57-00-PM.png" alt="Size Limit CLI" width="738">
</p>

## Who Uses This

- [Nkomor Healthcare Inc.](https://www.linkedin.com/company/nkomor-healthcare-inc/posts/?feedView=all)
- [Shatoria Giles](https://linktr.ee/shatoriagiles)


## Architecture?
- [See LucidChart here](https://lucid.app/lucidchart/f2c81603-b835-406f-be5c-3988902d3a6e/edit?viewport_loc=-1769%2C-1342%2C8870%2C4253%2C0_0&invitationId=inv_4dc23d31-3b3a-404f-af96-ce149821892c)

<p align="center">
  <img src="https://i.postimg.cc/52tmxxX4/Patient-Vital-Monitoring-Pipeline.png" alt="Size Limit CLI" width="100%">
</p>


## How It Works

1. The pipeline starts when medical devices stream patient vital signs (heart rate, blood pressure, oxygen levels, temperature) into Pub/Sub, which acts as the real-time ingestion layer for incoming healthcare data.
2. The streaming data is then temporarily stored in Cloud Storage, where it lands in a raw format before any processing begins. This ensures no data is lost and allows replay if needed.
2. The system processes data through a multi-layer architecture:
     - Bronze layer stores raw, unprocessed patient data.
     - Silver layer cleans, validates, and standardizes the data (removing errors, formatting timestamps, handling missing values).
     - Gold layer transforms the data into analytics-ready metrics for reporting and monitoring.
4. After processing, the curated data is loaded into BigQuery, where it is organized for fast querying, dashboards, and historical patient analysis.
5. The pipeline continuously checks incoming data for abnormal readings (such as dangerously high heart rate or low oxygen levels). When thresholds are exceeded, it can trigger real-time alerts for healthcare providers.
6. Because the system is fully streaming-based, it processes patient vitals with minimal delay, enabling near real-time monitoring and faster clinical response times.

<p align="center">
  <img src="https://i.postimg.cc/y6Mqgbm8/Linkedin-banner.png" alt="Size Limit CLI" width="100%">
</p>
