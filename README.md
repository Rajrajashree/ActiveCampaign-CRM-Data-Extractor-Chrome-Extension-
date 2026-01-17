A Chrome extension that demonstrates how CRM data (Contacts, Deals, Tasks) can be extracted from web pages using DOM logic and stored persistently using Chrome Extension APIs.
Note: A live ActiveCampaign account was not available, so this project simulates CRM data extraction while fully implementing the real Chrome Extension architecture.

📁 Folder Structure
activecampaign-crm-extractor/
├── manifest.json
├── service-worker.js
├── content/
│   └── extractor.js
├── popup/
│   ├── index.html


🚀 Installation Steps
1. Download or clone this repository.
2. Open Chrome and go to:
    chrome://extensions
3. Enable Developer mode (top-right).
4. Click Load unpacked.
5. Select the activecampaign-crm-extractor folder.
6. The extension will be loaded and visible in the Chrome toolbar.


🔍 DOM Selection Strategy
In a real ActiveCampaign environment, CRM data such as contacts, deals, and tasks would be extracted using DOM selectors targeting tables, rows, and data attributes.
Since a live account is unavailable, the extension simulates this process by:
Detecting page load via a content script
Generating mock CRM data objects
Logging extracted data in the browser console
Treating simulated data exactly like real DOM-extracted data
This demonstrates the full extraction flow without requiring credentials.


💾 Storage Schema
Extracted data is saved using chrome.storage.local in the following format:
{
  "contacts": [
  {"name": "John Doe", "email": "john@example.com" }
  ],
  "deals": [
    { "title": "Demo Deal", "value": 5000 }
  ],
  "tasks": [
    { "task": "Follow-up Call", "dueDate": "2026-01-20" }
  ],
  "lastSync": 1700000000000
}


🧪 How the Extension Works
1. Content script runs when a page loads.
2. Clicking Extract Now triggers CRM data extraction logic.
3. Data is saved to chrome.storage.local.
4. Console logs confirm successful extraction.
5. Data remains available after refreshing the page.
