# Brochures App

An Android application for browsing retail brochures, featuring a clean architecture implementation with Jetpack Compose.

## Architecture Overview

### Core Principles
- **Unidirectional Data Flow** - MVI pattern for state management
- **Modular Design** - Clear separation of concerns via clean architecture layers
- **Reactive UI** - Jetpack Compose with state hoisting

### Tech Stack
- **Kotlin**
- **Jetpack Compose**
- **Koin** - Dependency injection
- **Retrofit** - Network requests
- **Coroutines/Flow** - Asynchronous operations
- **MockK/Turbine** - Testing

#### Layer Responsibilities:

1. **Data Layer**
    - `datasource/remote/`: Retrofit API implementations
    - `repository/`: Business logic and data transformation
    - `di/`: Koin module configuration

2. **Domain Layer**
    - Entity definitions (`model/`)
    - Interfaces (`datasource/`)
    - Pure Kotlin business logic
    - Exception handling

3. **UI Layer**
    - Compose-based UI components (`component/`)
    - MVI pattern implementation (`BaseViewModel`)
    - Navigation (`navigation/`)
    - Screen implementations (`screen/`)

## Setup

1. Clone the repository https://github.com/ciriti/Brochures.git
2. Open in Android Studio
3. Build and run

## Testing

The app includes unit tests

To run tests:
- Unit Tests: `./gradlew test`

## Key Features

- Filtering brochures by distance
- Premium brochure highlighting
- Error handling with retry mechanism
- Loading states
- Responsive grid layout
