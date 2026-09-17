# E-Sports Telemetry & Engagement Analytics 🎮📊

A Power BI dashboard that tracks live-stream viewership, chat activity, and subscriber conversion across e-sports tournaments, games, and streamer channels.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)

## Overview

This report brings together stream telemetry and viewer engagement data to give a real-time-style view of how audiences respond during e-sports broadcasts — viewer counts, chat sentiment, and subscriber growth — sliceable by tournament, game title, streamer channel, and time.

## Dashboard Features

**KPI Cards**
- Total Concurrent Viewers
- Total Chat Message Count
- Positive Sentiment Score
- Subscriber Conversion Per Hour

**Slicers / Filters**
- Tournament Name
- Game Title
- Streamer Channel
- Timestamp (date/time range)

**Visuals**
- **Chat Sentiment Velocity vs. Concurrent Viewers** — combo line/column chart plotting sentiment velocity against live viewer counts over time
- **New Subscribers by Streamer Channel** — combo line/column chart comparing subscriber gains across channels
- **Average Concurrent Viewers Over Time** — area chart showing the viewership trend across the stream timeline

## Data Model

The report is built on the following tables:

| Table | Purpose |
|---|---|
| `tbl_Stream_Sessions` | Session-level attributes: tournament, game title, streamer channel |
| `tbl_Viewer_Engagement_(TimeSeries)` | Time-series metrics: concurrent viewers, chat messages, sentiment, new subscribers |
| `Fact_Stream_Engagement` | Consolidated fact table combining timestamped engagement metrics (sentiment velocity, sub conversion rate, concurrent viewers) |

## Tech Stack

- **Power BI Desktop** (.pbix)
- DAX measures for aggregations (sums, averages, conversion rates)
- Native Power BI visuals (cards, slicers, combo charts, area chart)
