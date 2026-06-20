# 🚀 Jetpack Compose & UI Architecture: Ultimate Interview Prep Blueprint (Free Sample & Checklist)

Welcome to the open-source sample repository and study checklist for the **Jetpack Compose & UI Architecture: Ultimate Interview Prep Blueprint**.

This handbook is designed for senior and lead Android software engineers preparing for top-tier technical loops. It covers 55 advanced questions, Compose runtime internals (slot table, gap buffer), State management, custom layouts, pointer input, testing rules, stability profiling, and Google interview loop strategies.

---

## 🛍️ Get the Full Playbook (₹2,499 / ₹3,999)

Get the complete compiled, ad-free PDF eBook containing all 55 questions, code blueprints, and the full audio study companion:
* [👉 **Buy the PDF Playbook on Gumroad (₹2,499 / ₹3,999)**](https://yogirana.gumroad.com/l/mtziu)
  - **Standard Edition (₹2,499)**: Includes print-ready 82-Page Master Playbook + 7 topic handbooks.
  - **Premium Edition (₹3,999)**: Includes all PDFs + the full Audio Study Companion.

---

## 📋 Compose & UI Architecture Checklist

Use this checklist to track your learning progress or prepare for senior system design and coding interview loops:

### ⚙️ Section 1: Compose Runtime & Internals
* [x] **Topic 1**: How does Jetpack Compose work internally? Explain the Compose runtime and slot table. *(Read Free Sample Below)*
* [ ] **Topic 2**: What is recomposition? What triggers it and how does Compose minimize unnecessary recompositions?
* [ ] **Topic 3**: What is the Snapshot system in Compose? How does it enable state observation and transactions?
* [ ] **Topic 4**: Explain the Compose phases: Composition, Layout, and Drawing. How can you optimize each?
* [ ] **Topic 5**: What is @Composable annotation? What are the rules and restrictions for composable functions?
* [ ] **Topic 6**: Explain remember, rememberSaveable, and derivedStateOf. When do you use each?
* [ ] **Topic 7**: What are side effects in Compose? Explain LaunchedEffect, SideEffect, DisposableEffect, rememberCoroutineScope, and rememberUpdatedState.
* [ ] **Topic 8**: What is State Hoisting? Explain the pattern and when NOT to hoist state.
* [ ] **Topic 9**: Explain Compose's key() composable. Why is it critical for lists and animations?
* [ ] **Topic 10**: What is CompositionLocal? How does it work and when should you use vs avoid it?

### 🏗️ Section 2: State Management in Compose
* [ ] **Topic 11**: How do you connect a ViewModel to a Compose screen? Explain the full data flow.
* [ ] **Topic 12**: What is the difference between collectAsState and collectAsStateWithLifecycle? Discuss lifecycle awareness in Compose.
* [ ] **Topic 13**: How do you model complex UI state in Compose? Discuss UiState design patterns.
* [ ] **Topic 14**: How do you handle one-time UI events (navigation, snackbars, dialogs) in Compose?

### 📐 Section 3: Layout, Modifiers & Custom Composables
* [ ] **Topic 15**: How does the Modifier system work? Explain modifier order and why it matters.
* [ ] **Topic 16**: How do you create a custom Layout in Compose? Explain the Layout composable and measure/place protocol.
* [ ] **Topic 17**: How does LazyColumn work internally? How does it differ from RecyclerView?
* [ ] **Topic 18**: Explain Compose animations. Discuss AnimatedVisibility, animateFloatAsState, updateTransition, and Animatable.
* [ ] **Topic 19**: How do you handle gestures and touch in Compose? Explain pointerInput, detectTapGestures, and nestedScroll.
* [ ] **Topic 20**: How do you implement a custom Modifier?

### 🔁 Section 4: View Interoperability & Testing
* [ ] **Topic 21**: How do you embed a Compose composable inside a traditional View-based layout?
* [ ] **Topic 22**: How do you embed a traditional View inside Compose using AndroidView?
* [ ] **Topic 23**: How do you test Composables? Explain ComposeTestRule, finders, assertions, and actions.
* [ ] **Topic 24**: What is Modifier.testTag and the semantics tree? How does Compose UI testing find nodes?
* [ ] **Topic 25**: What is Navigation in Compose? Explain NavController, NavHost, and deep links.

### 🚀 Section 5: Performance Optimization & Advanced Topics
* [ ] **Topic 26**: How do you identify and fix performance issues in Compose?
* [ ] **Topic 27**: What are Compose stability annotations? When do you use @Stable vs @Immutable?
* [ ] **Topic 28**: How do you implement pull-to-refresh in Compose?
* [ ] **Topic 29**: Explain Compose's approach to accessibility. How do you make composables accessible?
* [ ] **Topic 30**: What is the difference between Canvas composable and the draw modifiers? When do you use each?
* [ ] **Topic 31**: What is Paging 3 integration with Compose? Explain LazyPagingItems.
* [ ] **Topic 32**: How do you implement a bottom sheet in Compose? Explain ModalBottomSheet and state management.
* [ ] **Topic 33**: Explain how Compose handles configuration changes. What survives and what doesn't?
* [ ] **Topic 34**: What is BoxWithConstraints and when do you use it?
* [ ] **Topic 35**: What is Compose Multiplatform and how does it relate to Android Compose?
* [ ] **Topic 36**: How do you implement a drag-and-drop list in Compose?
* [ ] **Topic 37**: What is the role of LocalContext, LocalLifecycleOwner, and other CompositionLocals provided by the framework?
* [ ] **Topic 38**: How do you handle insets (status bar, navigation bar) in Compose?
* [ ] **Topic 39**: What is the difference between Modifier.clickable and Modifier.pointerInput for handling touch?
* [ ] **Topic 40**: What is the Compose UI architecture recommendation from Google? (MAD Architecture)
* [ ] **Topic 41**: What is Accompanist library? Which Accompanist components have been promoted to Compose core?
* [ ] **Topic 42**: How do you implement a custom TextField with validation in Compose?
* [ ] **Topic 43**: What is Compose's approach to themes? Explain MaterialTheme, custom themes, and dark mode.
* [ ] **Topic 44**: How does Compose handle IME (keyboard) insets and keyboard avoidance?
* [ ] **Topic 45**: How do you debug Compose layouts? What tools does Android Studio provide?

### 🎯 Section 6: Advanced Scenarios & Google-Specific Topics
* [ ] **Topic 46**: Design a reusable, production-grade loading state component in Compose.
* [ ] **Topic 47**: What are known issues or limitations of Jetpack Compose that you've encountered?
* [ ] **Topic 48**: How would you implement a complex nested scrolling behavior, like a collapsing toolbar with a sticky header?
* [ ] **Topic 49**: How do you handle focus management in Compose? (FocusRequester, FocusManager)
* [ ] **Topic 50**: What is Compose's integration with WorkManager? How do you show progress from a WorkManager task in Compose?
* [ ] **Topic 51**: How does Compose handle the back gesture / predictive back navigation?
* [ ] **Topic 52**: What is the windowSizeClass in Compose and how do you build adaptive layouts?
* [ ] **Topic 53**: What is the difference between Compose UI tests, screenshot tests, and integration tests?
* [ ] **Topic 54**: How do you handle errors and retry in Compose UI systematically?
* [ ] **Topic 55**: Advanced scenario: You have a Compose screen that renders 200+ items with complex per-item state. It has severe recomposition jank. Walk through your debugging and optimization process.

---

## 📖 Free Chapter Sample: Topic 1 (How does Jetpack Compose work internally?)

### Question
How does Jetpack Compose work internally? Explain the Compose runtime and slot table.

### Answer
Jetpack Compose is a declarative UI toolkit built around a custom runtime that manages a persistent tree of UI elements. At its core is the Composer and the slot table (gap buffer).

When a composable function runs, it doesn't directly create View objects. Instead, it emits 'slots' into the slot table – a linear data structure (like a memory tape) that stores the data and state associated with each composable's position in the tree. The slot table uses a gap buffer data structure: an array with a movable gap, enabling efficient insertions and deletions in the middle.

The Composer controls this slot table. As composables execute, the Composer reads/writes slots in sequence. Each composable has a unique 'key' derived from its position in the source code (line number + call sequence number) – this is called the call site key or positional key. This key determines where in the slot table its data lives.

On recomposition: the Composer walks the slot table again. For each composable, it checks if inputs have changed (using `==` equality). If unchanged, it **SKIPS** the composable (no re-execution). If changed, it re-executes and updates the slot. This is **positional memoization** – memoization based on call position, not explicit keys.

The output of the composition is a tree of `LayoutNodes` (not Views). The Layout phase measures and places these nodes. The Draw phase renders them to the canvas. This is entirely separate from the Android View system.

#### Follow-up / Cross Questions
* **What is the gap buffer in the slot table?**
  A gap buffer is an array with a 'gap' (empty space) that can be moved to any position. Insertions and deletions at the gap position are O(1) – you just fill/empty the gap. Moving the gap to a new position is O(distance). For Compose's use case – sequential traversal with occasional structural changes – this is extremely efficient.
* **What is the difference between the Composition and the LayoutNode tree?**
  The Composition (slot table) is the logical representation of composable calls and their data. The LayoutNode tree is the physical representation used for measurement and layout – like the View hierarchy. One composable may emit zero LayoutNodes (pure logic/state nodes) or multiple. The Layout Modifier chain lives in the LayoutNode.

> **GOOGLE TIP**: Mentioning 'slot table,' 'gap buffer,' and 'positional memoization' signals deep Compose knowledge. Most candidates only know the public API – these internals are a key differentiator.
