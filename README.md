# REST API Data Fetching & Local Caching Application

A Flutter application demonstrating asynchronous network requests to a REST API, local data persistence with `SharedPreferences`, reactive UI state handling via `FutureBuilder`, and Material 3 design principles.

---

## 📌 Features

* **Asynchronous REST API Integration:** Fetches post feeds asynchronously from JSONPlaceholder (`https://jsonplaceholder.typicode.com/posts`) with timeout handling[cite: 1].
* **Offline Caching:** Persists raw JSON payloads locally using `SharedPreferences` to enable full offline playback[cite: 1].
* **Reactive Multi-State UI:**
  * **Loading State:** Displays dynamic skeleton placeholder cards while fetching data[cite: 1].
  * **Online Feed:** Renders live posts styled in Material 3 cards[cite: 1].
  * **Offline Mode:** Detects network disruption, loads cached posts, and displays a `"Viewing offline cached data"` banner[cite: 1].
  * **Error Handling:** Shows a dedicated `"Connection Unavailable"` screen with a retry button when offline and no cache is present[cite: 1].
* **Pull-to-Refresh:** Supports native swipe-to-refresh gestures via `RefreshIndicator`[cite: 1].
* **Clean Architecture:** Modular separation of concerns across bootstrapping, data serialization, and UI presentation[cite: 1].

---

## Screenshots
<img width="1470" height="956" alt="Screenshot 2026-09-23 at 1 53 17 PM" src="https://github.com/user-attachments/assets/2bc27a49-ad8b-4ec4-af4a-22043cefb6f4" />
<img width="1470" height="956" alt="Screenshot 2026-09-23 at 1 53 25 PM" src="https://github.com/user-attachments/assets/67037a6b-32a4-4fe6-b6f7-117255c539dc" />


## 📁 Project Structure

```plaintext
lib/
├── main.dart        # Application entry point & Material 3 global theme configuration[cite: 1]
└── post_screen.dart # Post model, network/cache logic, and screen UI components[cite: 1]
