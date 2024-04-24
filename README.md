# TEC SPECS — MSI Day Hackathon Project

### About This Project

"TEC SPECS" aimed to be a functional _computer lab assignment and queueing system_ prototype featuring efficient back-end logic and original graphical assets — all done from scratch — by Ari Winograd and E.J. Yu during the 2023 MSI Day Hackathon. Originally intended to be a multi-platform application made from scratch with the help of a web development framework known as Framework7 (during the first attempt at this idea), this second attempt at the creation of TEC SPECS was envisioned as a website that could _also_ be installed as a progressive web app that supported offline functionality if desired — the latter of which intended to reflect traces of the original vision for this project. And what you're seeing in this GitHub repo right now was the result of the hackathon group's efforts from that weekend. For this second attempt, Framework7 was replaced by Astral — a responsive website template by ajlkn — as the base for our project's front-end (with approval for this given, as we only used the core stylesheet and script files bundled with this template to serve as a framework for our (now-dubbed) "functional prototype." Unfortunately, this MSI Day Hackathon project was not finished in time (due to various complications), but would have elegantly united a minimalistic graphical interface with a functional and efficient queueing system (in JavaScript) to provide a beautifully-crafted, graphical computer lab assignment and queueing system that surely would have impressed had the team been given more time. We wanted our "application" to be very simple yet very nice-looking and functional, requiring as little effort from incoming users to get a computer (or wait for one to free up) as possible **without** overlooking the ability to let admins **thoroughly** manage PC setups in TEC.

The name of our project is "TEC SPECS" — which is a play on words referencing the term "technical specifications" (or "tech specs" for short), with "TEC" reusing the official acronym for the building that this hackathon was hosted at ("Triton Esports Center", or "TEC" for short) and "SPECS" being an acronym meaning "Simple Player and Electronics Control System" that drives the completion of this project name's unique play on words.

### Hackathon Prompt

"Create a solution that enhances the efficiency of TEC operations by tracking and managing user session times at PCs. The goal is to improve queue times for patrons and streamline the overall organization of TEC usage."

Recommended Features:

-  Queue management with ID scan
-  User session tracking for each PC
-  Scalability: PC layout and statuses could be managed

### Hackathon Rules

1. Project must be worked on at TEC or Gliderport Lounge
2. Project must be worked on using MSI Laptops provided (Raider or Cyborg)
3. AI and use of websites like ChatGPT are strictly prohibited
4. Only work individually or in the teams you signed up with

# How to Use

Once you have opened `index.html` in your browser, you can add the following **HTML element IDs** to (or in — if existing) the URL to traverse through screens on this prototype as intended.

### Simulating an ID Scan (Front-End Demo)

1. **Simulate a student ID scan from the login screen:** Add `#studentSignOn` to the end of the URL.
2. **Simulate a return to the login screen (previous screen) some time after a student ID has been scanned:** Add `#loginIDscan` to the end of the URL (or replace the existing HTML element ID in the URL with `#loginIDscan` if there is one there already).
3. **Simulate an ID scan after returning to the login screen:** Add `#studentSignOn` to the end of the URL (or replace the existing HTML element ID in the URL with `#studentSignOn` if there is one there already).
4. **Simulate a return to the login screen (previous screen) via mouse event from the user:** Click on the `Back to Login` button.
5. *Repeat as desired to simulate students coming into TEC to obtain a PC they can use.*

### Simulating a Logon by User w/ Admin Credentials (Front-End Demo)

1. **Switch to "Administrator Login" screen:** Click on the `Switch to Admin Sign In Portal` button (or add `#loginPIDAD` to the end of the URL if you're experiencing issues / replace the existing HTML element ID in the URL with `#loginPIDAD` if there is one there already).
2. *Multiple options from here:*
- **Return to the main (previous) login screen:** Click on the `Back` button (or add `#loginIDscan` to the end of the URL / replace the existing HTML element ID in the URL with `#loginIDscan` if there is one there already).
- **Simulate a successful admin logon attempt:** Add `#adminSignOn` to the end of the URL (or replace the existing HTML element ID in the URL with `#adminSignOn` if there is one there already).
3. **Simulate an admin user clicking the Logout button:** Add `#loginIDscan` to the end of the URL (or replace the existing HTML element ID in the URL with `#loginIDscan` if there is one there already).
4. *Repeat as desired to simulate users with admin credentials coming into TEC to log into the system as an administrator and then logging off.*

### Testing Queueing Functionality (Back-End Demo)

Files in the `tec-specs-backend` folder (`./assets/js/tec-specs-backend`) may be opened in the browser or in an IDE. Test cases can be passed in as arguments using the console or by modifying `test.js` to quickly demo hardcoded test cases with console output feedback.

- `esports_ids.js` — A purposefully hardcoded list containing information about VIP / priority users.
- `layout.js` — For counting the maximum number of PCs in the space.
- `pcs.js` — Determines the availability of PCs.
- `studentform.js` — Assists in managing the queueing process.
- `test.js` — For quickly demoing hardcoded test cases with console output feedback.
