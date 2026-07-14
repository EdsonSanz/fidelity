# Web Client

Web app serving agricultural professionals with commodity prices, order management, financial tracking, grain contracts, weather forecasts, and more.


---

## Tech Stack

| Layer         | Technology                       |
| ------------- | -------------------------------- |
| Framework     | React Native 0.81.4 + Expo 54    |
| Navigation    | Expo Router 6 (file-based)       |
| Language      | TypeScript 5.8.3                 |
| State         | Redux Toolkit 2.8.2              |
| Data fetching | TanStack React Query 5           |
| HTTP          | Axios 1.13                       |
| Forms         | Formik + Yup                     |
| i18n          | i18n-js — ES (default) · PT · EN |
| Animations    | Rive · React Native Reanimated 4 |
| Maps          | React Native Maps 1.20           |
| Storage       | AsyncStorage                     |
| Build & OTA   | EAS Build + Expo Updates         |

---

```

- `useRef<ScrollView>` for programmatic scroll
- `useMemo` derives `currentIndex` from Redux `serviceFunctionalitySelected`
- `useEffect` watches `currentIndex` → calls `scrollTo()` on mount and on update
- `handleScroll` computes index from `contentOffset.x / ITEM_WIDTH` → dispatches to Redux
- ScrollView config: `snapToInterval={ITEM_WIDTH}` · `scrollEventThrottle={16}` · `decelerationRate="fast"`
- Dot indicators per item, active color driven by `currentIndex`
