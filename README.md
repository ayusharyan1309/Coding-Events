# Coding Events — Event Discovery App

A **Flutter mobile application** for discovering and exploring tech/coding events. Fetches events from an external API, displays them in a searchable list, and shows detailed event information including venue, organizer, and date/time.

## Features

- **Event List** — Browse all upcoming events with banner images
- **Search** — Filter events by country/venue name
- **Event Details** — Full event view with banner, organizer info, date/time, venue, and description
- **Book Now** — Booking button (UI ready)
- **Clean UI** — Material 3 design with custom color scheme

## Quick Start

```bash
git clone https://github.com/ayusharyan1309/Coding-Events.git
cd Coding-Events
flutter pub get
flutter run
```

## Architecture

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│  External    │────▶│  HTTP Client │────▶│  Flutter UI  │
│  Events API  │     │  (Dart)      │     │  (Screens)   │
└──────────────┘     └──────────────┘     └──────────────┘
```

## Project Structure

```
lib/
├── main.dart                          # App entry point
├── constants/global_variables.dart    # Color constants
├── model/EventsModel.dart             # JSON data model
├── services/
│   ├── eventServices.dart             # API service layer
│   └── utilities/app_url.dart         # API endpoint constants
├── features/
│   ├── home/screens/home_screen.dart  # Event list + search
│   └── eventDetails/
│       ├── screens/eventDescription.dart  # Event detail view
│       └── widgets/
│           ├── dateTimeInfo.dart      # Date/time display
│           ├── eventAddress.dart      # Venue address
│           └── eventinfo.dart         # Organizer info
```

## API

| Endpoint | Description |
|----------|-------------|
| `GET /v1/event` | Fetch all events |

Base URL: `https://sde-007.api.assignment.theinternetfolks.works/`

## Event Data Model

| Field | Description |
|-------|-------------|
| `title` | Event name |
| `description` | Event description |
| `banner_image` | Banner image URL |
| `date_time` | Event date and time |
| `organiser_name` | Organizer name |
| `organiser_icon` | Organizer icon URL |
| `venue_name` | Venue name |
| `venue_city` | Venue city |
| `venue_country` | Venue country |

## Tech Stack

| Component | Technology |
|-----------|------------|
| **Framework** | Flutter 3.1+ / Dart |
| **HTTP** | http package |
| **State** | flutter_bloc |
| **UI** | Material 3 |
| **API** | External REST API |
