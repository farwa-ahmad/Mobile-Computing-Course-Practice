# Android Development with Java

I enjoy building software across platforms. This collection brings together seven Android projects from my Mobile Computing coursework (2021), built with **Java, XML layouts, and the Android SDK**.

The projects demonstrate hands-on work with multi-screen interfaces, navigation, dynamic lists, local data storage, animation, and audio/video playback—from focused exercises to a larger social-app UI prototype.

## Standalone Android projects

For larger application work from the same period, see the dedicated project repositories:

- **[MyList — cloud-backed task manager](https://github.com/farwa-ahmad/MyList-Android)** — a Java Android task manager using Firebase Firestore, RecyclerView, ViewBinding, due dates, completion state, and swipe-to-edit/delete interactions.
- **[eCure — healthcare app prototype](https://github.com/farwa-ahmad/eCure-Android)** — a larger Java/Firebase Android prototype with patient and doctor account flows, authentication, profiles, location features, doctor discovery, and partially implemented appointment/doctor workflows.

Those repositories are intended as the cleaner, project-focused versions. This repository preserves the broader coursework progression and supporting materials.

## Start here

- **[Multi-screen UI prototype](InstagramApp)** — an Instagram-inspired interface bringing together onboarding, sign-in and registration screens, bottom navigation, fragments, and a navigation drawer. First-launch state is stored with `SharedPreferences`; sign-in and registration are UI flows, not backend authentication.
- **[Lists and adapters](05WeekApplications/ListView_Adapters)** — a dynamic `ListView` backed by an `ArrayAdapter`, with item entry, sorting, and selection passed to another activity through intent extras.
- **[Customer records](06WeekApplications)** — a local SQLite database and form-based interface for adding, viewing, updating, and deleting customer records.

## Project guide

Each linked directory is a separate Android Studio project with its own Gradle configuration.

| Project | Concepts explored |
| --- | --- |
| [Views and layouts](03WeekApplication/Views_GridLayout) | XML-based views and ConstraintLayout |
| [Intents and activities](04WeekApplication) | Button events, opening a website with an implicit intent, and explicit activity navigation |
| [Lists and adapters](05WeekApplications/ListView_Adapters) | ListView, ArrayAdapter, collection sorting, and intent extras |
| [Animation and media](05WeekApplications/AnimationApp) | View-property animation, MediaPlayer audio controls, and VideoView playback |
| [Local database](06WeekApplications) | SQLiteOpenHelper, ContentValues, Cursor queries, and customer-record forms |
| [Custom navigation drawer](07WeekApplications/CustomNavDrawerApp) | Toolbar, DrawerLayout, ActionBarDrawerToggle, and menu-selection feedback |
| [Multi-screen UI prototype](InstagramApp) | Onboarding with ViewPager, SharedPreferences, animated backgrounds, view binding, fragments, and AndroidX Navigation |

## Technology

**Application code:** Java with Java 8 source compatibility, XML resources, AndroidX AppCompat, ConstraintLayout, and Material Components.

**Platform APIs:** Intents, SharedPreferences, SQLite, MediaPlayer, and VideoView.

**Original build configuration:**

| Setting | Checked-in value |
| --- | --- |
| Android Gradle Plugin | 4.2.0 |
| Gradle wrapper | 6.7.1 |
| Compile / target SDK | 30 |
| Android SDK Build Tools | 30.0.3 |
| Minimum SDK | 16 for most projects; 22 for Views and layouts |

## Open a project

1. Clone the repository:

   ```bash
   git clone https://github.com/farwa-ahmad/Mobile-Computing-Course-Practice.git
   ```

2. In Android Studio, choose **Open** and select an individual project folder, such as `Mobile-Computing-Course-Practice/InstagramApp`. The repository root is a collection, not a single Gradle project.
3. Configure your local Android SDK location and install the SDK platform and Build Tools listed above.
4. Sync Gradle using a JDK and Android Studio setup compatible with the original Gradle/Android Gradle Plugin versions, or migrate those versions together in a separate branch.
5. Select the `app` run configuration and an emulator or connected Android device meeting the project's minimum SDK, then run.

These projects preserve their original 2021 Android configuration. Modern Android Studio versions may prompt upgrades to Gradle, JDK, or dependencies when opening them.

## Coursework materials

The repository also includes [handwritten Mobile Computing notes](00%20-%20Mobile%20Computing%20-%20Handwritten%20Notes.pdf) and weekly course materials alongside the application code.
