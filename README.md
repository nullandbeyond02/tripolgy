Tripolgy
Make traveling easy. The planner friend for your next group trip.

Built for IceHacks 2026 ·

Why I built it
The flights are booked, everyone’s excited, and somehow nobody planned what to do. Even once someone makes a plan, changing one activity can mean another round of group texts and another round of budget math.

Tripolgy turns a short survey into a day-by-day itinerary, then gives the group a way to discuss changes, decide who’s joining each activity, and see how those decisions affect the budget.

What you can do
Build a trip around your group. Add flights, lodging, and a budget for food and activities. Pick your pace, interests, dietary preferences, and must-see stops. Add friends by username or include guests without accounts.
Review and edit the itinerary. Switch between days, compare activity intensity, check available forecasts and estimated distances from your stay, and open stops in Google Maps. Add, move, or remove activities.
Decide together. Comment or react on individual stops. When a change needs approval, the original plan stays in place until everyone required has approved it.
See what each person might spend. Mark who’s attending each activity to update the estimated group total and each traveler’s share. You can also record planned contributions.
Make each trip your own. Reopen saved plans from My Trips, where you can keep the default destination cover when available or upload your own.
Run locally
Tripolgy uses HTML, CSS, and JavaScript. There’s no build step or package installation. You’ll need Python for the local server commands below.

Clone this repository or choose Code → Download ZIP on GitHub and extract it.

Open the folder containing index.html in VS Code. Keep the images folder next to index.html.

Open a terminal in that folder and run:

py -m http.server 5500
On macOS or Linux, use python3 -m http.server 5500 instead.

Open http://localhost:5500 in your browser.

Try the group approval flow
Create two test accounts in the same browser profile at the same URL. Log in as the first user, create a trip, and add the second user by username rather than as a guest. Propose moving an activity to another day. Then sign in as the second user, open the trip, and approve the request. Check that the activity moved to the new day.

How it works
The planner turns survey answers into an AI prompt and requests structured itinerary data. JavaScript converts the response into editable activity cards. If the AI service doesn’t return a usable plan, Tripolgy shows a labeled sample itinerary so you can still try the editing workflow.

The approval logic runs separately from the AI. It records proposed changes and applies them once the required approvals are in. Trips and changes are saved in the browser using localStorage.

Prototype limitations
Collaboration works within one browser profile. This prototype does not sync accounts, trips, or approvals across devices. Use a throwaway password. The invite button copies the site URL, not a link that grants access to a trip.
Travel details are estimates. Verify costs, hours, ratings, and accessibility before booking. The sample itinerary is not verified. Live AI, weather, and photo lookups depend on internet access and third-party services.
Production deployment would need a backend. Hosted authentication, shared storage, and server-side AI requests would support secure accounts and cross-device collaboration. Do not commit API keys.
Credits and AI disclosure
Tripolgy uses Pollinations for AI planning with optional Google Gemini support, Open-Meteo for forecasts, OpenStreetMap Nominatim for place lookup, and Wikipedia for online destination imagery. The homepage also uses six bundled destination photos.

ChatGPT and Claude were used as AI coding assistants during development.
