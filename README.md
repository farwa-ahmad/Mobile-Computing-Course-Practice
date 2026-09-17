# Android Development Foundations

Seven standalone Android projects exploring native mobile development with **Java, XML layouts, and the Android SDK**. Created during my Mobile Computing coursework in 2021, this collection documents hands-on practice with UI composition, activity navigation, adapters, local persistence, animation, and media playback.

## Start here

- **[Multi-screen UI prototype](InstagramApp)** — an Instagram-inspired interface bringing together onboarding, sign-in and registration screens, bottom navigation, fragments, and a navigation drawer. First-launch state is stored with `SharedPreferences`; sign-in and registration are UI flows, not backend authentication.
- **[Lists and adapters](05WeekApplications/ListView_Adapters)** — a dynamic `ListView` backed by an `ArrayAdapter`, with item entry, sorting, and selection passed to another activity through intent extras.
- **[Local database exercise](06WeekApplications)** — a customer-record model and SQLite helper exploring table creation, inserts, queries, updates, and deletes. See the maintenance notes below for a known issue in the update/delete queries.

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

These projects retain their 2021 build setup. Compatibility with current Android Studio versions has not been verified; opening them may require toolchain adjustments or dependency migration. No successful build or emulator run is claimed by this documentation update.

## Coursework materials

The repository root also contains [handwritten Mobile Computing notes](00%20-%20Mobile%20Computing%20-%20Handwritten%20Notes.pdf) and weekly course documents. These complement the code; document titles do not imply a corresponding completed application. The Week 10, 11, and 12 files are empty placeholders in the original collection.

## Scope and maintenance notes

This is a record of my Android foundations and learning progression, rather than a production application suite. The original exercises and directory names are preserved.

- **UI prototype:** Sign-in and registration navigate between screens without authenticating users. Several navigation items display feedback rather than implementing full product features.
- **Database exercise:** Update and delete filters use `ID`, while the table defines `Customer_ID`. These operations need correction before use; the upgrade handler also drops and recreates the table rather than preserving records.
- **Tests:** The checked-in tests are starter examples, not comprehensive feature coverage.

