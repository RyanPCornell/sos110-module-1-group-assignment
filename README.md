# SOS 110 — Module 1 Group Assignment: Map a Biome as a System

A four-slide web deck for the in-class hand-off of the Module 1 group assignment
(the Ecosystem Approach / Web of Life one-page system diagram).

**Live:** https://ryanpcornell.github.io/sos110-module-1-group-assignment/

1. **Title**
2. **Announcements** — upcoming assignments, plus a live attendance roll call the
   instructor runs from the `?host` copy of the deck.
3. **The assignment**, set as a course handout — objective, the three instruction
   steps, and the submission requirements.
4. **★ Module 1 SET Builder** — a drag-and-drop sandbox for building the diagram
   the assignment asks for: pick one of nine biomes and record its vegetation,
   precipitation and temperature; drag in social, ecological, trophic and
   technical components (or a blank "Custom…" piece, and double-click anything to
   rename it); join trophic levels with ⚡ energy arrows and everything else with
   + / − causal arrows; watch the feedback loops it finds; shock it; write the
   sustainability lens, the explanation and the AI credit; then **Save as PDF**
   for the Canvas submission.

Everything is self-contained — no build step, no dependencies, no media folder.
The only external requests are Google Fonts.

## Running it in class
Open the live link. Press <kbd>→</kbd> / <kbd>space</kbd> or click to advance;
<kbd>M</kbd> or the ☰ button opens the slide menu.

Add `?host` to the URL for the instructor copy, which gets the **Attendance**
button on slide 2. Pick the section from the dropdown, press **Attendance** to
open the sign-in pop-up on every student's copy, then **Submit Attendance** to
close the roll call and mail the roster.

## Built from
`_deck-builder/module1_assignment.py` + `_deck-builder/module1_set_builder.py`
(not in this repo — this is the built output).

    DECK_OUT=".../module-1-assignment-web/index.html" python3 module1_assignment.py

`firebase-config.js` holds the Firebase web config and the attendance endpoints.
Those values are not secrets — they ship in every web page that uses them, and
access is controlled by the Firestore security rules. No student data is written
to Firestore; attendance goes straight from the browser to a Google Form.
