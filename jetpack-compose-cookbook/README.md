# Jetpack Compose Cookbook (Premium UI & Animations)

This is the public repository folder for the **Jetpack Compose Cookbook**, a curated collection of production-ready, highly optimized recipes for building premium UIs, smooth animations, and custom graphics in Android.

[![Buy on Gumroad](https://img.shields.io/badge/Gumroad-Buy%20Cookbook-blueviolet?style=for-the-badge&logo=gumroad)](https://yogirana.gumroad.com/l/sriav)

---

## 📋 The Complete 12-Recipe Study Checklist

Use this checklist to track your progress as you master advanced declarative UI development:

### I. Layouts & Structures
- [ ] **Recipe 1: Collapsible Header with Nested Scroll Integration (Advanced)** – Sync scroll gestures of a LazyColumn with a collapsing image banner.
- [ ] **Recipe 2: Pinterest-Style Staggered Grid Layout (Intermediate)** – Efficiently render staggered grid cards with varying heights.
- [x] **Recipe 3: Sticky Headers in LazyColumn (Intermediate)** – *[Free Sample Below]* Create pinned, dynamic list header separators.

### II. Animations
- [ ] **Recipe 4: Swipe-to-Reveal Contextual Actions (Advanced)** – Build swipeable list items with spring physics and sliding action buttons.
- [ ] **Recipe 5: Shimmer Loading Effect for Placeholders (Intermediate)** – Render shimmering skeleton placeholder sweeps during API loads.
- [ ] **Recipe 6: Expandable Floating Action Button (FAB) (Intermediate)** – Build a primary action button that animates open to reveal sub-menu options.

### III. Canvas & Custom Graphics
- [x] **Recipe 7: Circular Progress Ring with Gradient Sweep (Intermediate)** – *[Free Sample Below]* Draw custom loaders with SweepGradient brushes and rounded caps.
- [ ] **Recipe 8: Bezier Curve Line Chart (Advanced)** – Render responsive analytics graphs with smooth curve paths and gradient fills.
- [ ] **Recipe 9: Animated Vertical Bar Chart (Intermediate)** – Draw responsive bar charts that grow with clean animation scaling.

### IV. State & Performance
- [ ] **Recipe 10: Scroll Optimization with derivedStateOf (Advanced)** – Eliminate scroll lag by buffering state emissions.
- [ ] **Recipe 11: Double-Tap-to-Zoom Gesture Modifier (Intermediate)** – Chaining pointerInput modifiers for double-tap zoom and pan actions.
- [ ] **Recipe 12: Optimized Lazy Lists with Custom Keys & Content Types (Advanced)** – Maximize view recycling efficiency for complex multi-type feeds.

---

## 🔓 Free Sample Recipes

Here are two complete sample recipes directly from the book so you can verify the code and design quality:

### 1. Recipe #3: Sticky Headers in LazyColumn (Intermediate)
* **The Challenge**: Grouping list items (like transactions by date or contacts by alphabetical initials) and pinning category headers to the top of the screen during scrolling until the next group pushes them out.
* **The Solution**: Use Compose Foundation's `stickyHeader` API inside the `LazyColumn` builder. It dynamically pins header components to the top boundaries during list scrolling.

#### Code Blueprint
```kotlin
@OptIn(ExperimentalFoundationApi::class)
@Composable
fun StickyHeadersList(groupedContacts: Map<Char, List<String>>) {
    LazyColumn(modifier = Modifier.fillMaxSize()) {
        groupedContacts.forEach { (initial, contacts) ->
            // Sticky category header
            stickyHeader {
                Text(
                    text = initial.toString(),
                    modifier = Modifier
                        .fillMaxWidth()
                        .background(Color(0xFFF1F5F9))
                        .padding(horizontal = 16.dp, vertical = 8.dp),
                    style = MaterialTheme.typography.titleMedium,
                    color = Color(0xFF4F46E5)
                )
            }
            
            // Standard contact items in the group
            items(contacts) { contact ->
                Text(
                    text = contact,
                    modifier = Modifier
                        .fillMaxWidth()
                        .padding(16.dp),
                    style = MaterialTheme.typography.bodyLarge
                )
                Divider(color = Color(0xFFE2E8F0), thickness = 0.5.dp)
            }
        }
    }
}
```

#### Code Analysis
* **`stickyHeader { }`**: An experimental (but stable in behavior) DSL function inside `LazyColumnScope`. It pins the defined component to the top of the container viewport until another `stickyHeader` scrolling up replaces it.
* **`Map<Char, List<String>>`**: Structuring data as a map allows you to loop through keys (initials) and values (contacts list) in a single pass, matching standard database query outputs.

---

### 2. Recipe #7: Circular Progress Ring with Gradient Sweep (Intermediate)
* **The Challenge**: Creating a customized circular loader/progress indicator that supports gradient sweeps, custom round caps, and animated value updates (which the standard Material CircularProgressIndicator does not support).
* **The Solution**: Draw the ring manually using a `Canvas` and `drawArc`. We will pass a `SweepGradient` brush and animate the sweep angle using `animateFloatAsState`.

#### Code Blueprint
```kotlin
@Composable
fun GradientCircularProgress(
    progress: Float, // 0.0f to 1.0f
    modifier: Modifier = Modifier,
    strokeWidth: Dp = 12.dp
) {
    // Animate progress change
    val animatedProgress by animateFloatAsState(
        targetValue = progress,
        animationSpec = tween(durationMillis = 800, easing = FastOutSlowInEasing),
        label = "progress_anim"
    )

    Canvas(
        modifier = modifier
            .size(150.dp)
            .padding(strokeWidth / 2)
    ) {
        val sizeMin = size.minDimension
        val strokeWidthPx = strokeWidth.toPx()

        // 1. Draw Background Grey Ring
        drawCircle(
            color = Color(0xFFF1F5F9),
            radius = sizeMin / 2,
            style = Stroke(width = strokeWidthPx)
        )

        // 2. Draw Active Gradient Progress Ring
        drawArc(
            brush = Brush.sweepGradient(
                colors = listOf(
                    Color(0xFF3B82F6), // Start: Blue
                    Color(0xFF10B981), // Mid: Emerald
                    Color(0xFF3B82F6)  // End: Back to Blue
                )
            ),
            startAngle = -90f, // Start at 12 o'clock
            sweepAngle = animatedProgress * 360f,
            useCenter = false,
            style = Stroke(
                width = strokeWidthPx,
                cap = StrokeCap.Round
            )
        )
    }
}
```

#### Code Analysis
* **`SweepGradient`**: Draws a circular color wheel sweep. Repeating the starting color at the end makes the gradient seamless where the arc joins.
* **`drawArc`**: Renders the curve segment. Setting `useCenter = false` draws only the border stroke without filling the inner wedge.
* **`StrokeCap.Round`**: Caps the beginning and end of the progress arc with half-circles, creating a modern, premium feel.

---

## 🚀 Get the Full Cookbook
To get all 12 premium recipes (including collapsible headers, Bezier curve charts, swipe-to-reveal items, shimmer loaders, and derivedStateOf optimizations) complete with full design blueprints, code blueprints, and detailed code analysis:

👉 **[Get the Jetpack Compose Cookbook on Gumroad](https://yogirana.gumroad.com/l/sriav)**
