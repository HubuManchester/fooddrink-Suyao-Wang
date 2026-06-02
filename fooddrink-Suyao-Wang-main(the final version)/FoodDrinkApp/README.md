# NutriTrack Food Assistant

A cross-platform food nutrition tracking application built with .NET MAUI.

## Main Features

- Food Management: Browse, search, and add food and drink records
- Camera Capture: Take photos of food and preview
- Location Services: Record dining or purchase location (country, city, coordinates)
- Text-to-Speech: Read nutrition summaries and help content aloud
- Haptic Feedback: Provide operation reminders with vibration and haptic feedback
- Theme Switching: Support dark/light themes and large font mode
- Accessibility: Semantic labels, screen reader announcements, and clear validation prompts

## Evaluation Criteria Coverage

| Criteria | Implementation |
|--------|----------|
| UI/UX and Accessibility | XAML pages, bottom navigation, consistent visual style, dark mode, semantic descriptions, screen reader announcements |
| Mobile Hardware | Camera, location, text-to-speech, vibration, haptic feedback (exceeds 4 required) |
| Functionality | List, search, add, detail, settings, and hardware demo flows |
| Validation and Error Handling | Required field checks, number validation, permission errors, and hardware unavailable prompts |
| Code Quality | Separation of models and services, clear naming, reusable services |
| Deployment | .NET MAUI cross-platform app targeting Android and Windows |

## Running the Application

Open the project with Visual Studio 2022 with .NET MAUI workload installed:

- Recommended demo targets: Android Emulator, Windows Machine

### Build Commands

```powershell
# Windows build
dotnet build .\FoodDrinkApp.csproj -f net9.0-windows10.0.19041.0

# Android build
dotnet build .\FoodDrinkApp.csproj -f net9.0-android
```

## Project Structure

```
FoodDrinkApp/
├── App.xaml(.cs)           # Application entry and global resources
├── AppShell.xaml(.cs)      # Navigation structure (Bottom TabBar)
├── MainPage.xaml(.cs)      # Home page - Food list and search
├── AddItemPage.xaml(.cs)   # Add record page - Form validation
├── FoodDetailPage.xaml(.cs) # Detail page - Nutrition information display
├── HardwarePage.xaml(.cs)  # Hardware demo page
├── SettingsPage.xaml(.cs)  # Settings page - Theme and font
├── Models/
│   └── FoodItem.cs         # Food data model
├── Services/
│   ├── FoodCatalogService.cs # Food data service (API + local fallback)
│   ├── SpeechService.cs    # Text-to-speech service
│   ├── AccessibilityService.cs # Accessibility font service
│   └── MockApiConfig.cs    # API configuration
├── Platforms/
│   └── Android/
│       └── AndroidManifest.xml # Permission configuration
└── Resources/
    ├── Images/             # Food image resources
    └── Styles/             # Global styles
```

## Screencast Demo Checklist

1. Explain the "Food and Drink" theme and the "NutriTrack" application concept
2. Demonstrate search, detail page, and adding new records
3. Show validation prompts when required fields are empty or invalid numbers are entered
4. Demonstrate camera, location, text-to-speech, vibration, and haptic feedback
5. Show dark mode and large font mode
6. Display key code files: models, services, pages, and Android permission configuration
7. Show Android and Windows deployment results
8. Show GitHub commit history and README

## Configuration

### Mock API Configuration

The project supports fetching data from mockapi.io. Open `Services/MockApiConfig.cs` to configure the API endpoint:

```csharp
public const string EndpointUrl = "https://your-api.mockapi.io/api/v1/foods";
```

For detailed configuration steps, see `mockapi配置说明.md` in the project root directory.

## Visual Style

Warm food-themed color palette:
- Cream background
- Tomato red accent
- Roasted orange secondary
- Basil green accent
