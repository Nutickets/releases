[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 4: March 26th - April 20th 2021
Below you will find the summary notes for the 4th release of the Nuweb core platform. The focus points are highlighted in yellow.

## 🚀 New Features
- Added <mark>full multi-lingual support</mark> across the entire platform for user content. Organisers can now provide translations for events, data capture, images and much more for any language supported within their account.
- Added a new section in _Admin > Website > Text_ that allows organisers to <mark>customise customer emails</mark> at both the account-level and event-level
- Reserved Seating:
  - <mark>Added stands, gates and block</mark> allocation
  - Added top menu - including keyboard shortcut guides
  - Object editing menu could be either on the top or the side
  - Added full screen mode + ability to hide right column so the plan can truly be full screen
  - Added the ability to draw Gates/Stands/Stairs:
    - Ability to change how these definitions are called (i.e rename 'gate' to 'entrance')
    - New interface to assign these attributes, so you can double-check if you've done your setup correctly
  - ♿︎ <mark>Seat accessibility:</mark> display accessibility icon over seat, you can choose to highlight it with a blue background colour too. Accessibility icon was added into the icon library too.
  - Comment: Add any comments to a seat (it could be about visibility, accessibility etc), it will appear in the shop in purchase, and as as a tooltip
  - Under label options you can change how newly added Blocks, Tables, General Admissions are called
  - Seat properties: in the right column when you've got any objects selected with seats, you can edit the selected seats' properties like: accessibility, price bands, gates etc
  - Labelling offsets can go into negative (ie when you want to have a couple of rows with custom labels like VIP, and start labelling after them)
  - No redirect on save + loading animations and error message if an error happened during save, with export button so you can rescue your changes
  - Default object labels are now appear as placeholders in the label editor, instead of filling the field
  - Select multiple seats while holding up control / command (this in addition to holding up shift)
  - Added animation for seating plans that load in small size (because it's loaded on a phone or because they are big) + "Click to zoom in"
  - Added tooltip in seating editor to check seat properties like gates stairs etc
- Add the ability to create links in our WYSIWYG editor (i.e. in data capture questions, event pages, emails, etc.)
- <mark>Added a ‘regional settings’</mark> menu which displays automatically on a customers first visit to a multi-lingual shop
- Added the ability to manage tags (i.e. event tags) from a central interface including the ability to 'merge' tags
- <mark>Various branding and theming updates:</mark>
  - Introduced a new design for picking colour themes in Admin and Hub
  - Ability to style both primary and secondary buttons as either filled or line
  - Ability to change both button colour and button text colour to a wide array of branding values
  - Ability to add full width header images to listing pages and repeat events browse pages
  - Ability to add subheadings to listing pages
  - Ability to edit the top navbar background colour, text colour, layout, menu position and opacity
  - New layout options for footer as well as the ability to edit footer background colour, text colour and an option to hide the bottom footer
  - New alternate footer design if bottom footer is hidden
  - Extended previews in admin to showcase all the new design options
  - New collapsable card components


## ✨ Enhancements
- Added two new data capture options:
  - "Assign question to all tickets for all events"
  - "Assign question to all tickets of a specific event"
- Added the ability to send a customised order confirmation e-mail for any imported tickets
- Added the ability to specify the currency and language that a page should display in when linked externally (i.e. `https://your-ticket-shop.com/?locale=en&currency=GBP`). + added support to specify language/currency via cookies for third-party integrations.
- Added new scheduled events header options for further customisation of your schedule/season pages
- Made ‘change currency’ option visible to non-logged in users
- Added new social media and app store links and create compressed pngs for each new icon
- Added sold out/off sale styling for all timeslots, tickets and event blocks


## 🤝 Integrations
- Added a <mark>PayTabs payment gateway integration</mark>
- Integrate with the <mark>General Entertainment Authority</mark> (GEA) for Saudi Arabia
- SumUp: added the ability to toggle the ‘zip code’ field in the payment form
- Quickpay/SumUp: added the ability to link with a test account for testing the integration before going live
- Added a new <mark>customer importer</mark> to allow migration of customers from external systems
- Added an `appView` flag added to the shop, which when enabled hides the main menu. This is useful when embedding the shop into an iOS / Android app


## 🧹 Housekeeping
- Fixed stripe double charge bug in rare cases
- Fixed <mark>sales & attendance reporting inconsistencies</mark>
- Fixed ordering of addons in ticket shop to match the ordering setup in admin
- Fixed issue where child company menu and listings were displaying in parent company sites
- Allow the ‘purchase limit’ settings to be bulk edited
- Fix: “Access Stream” Button missing when “download” wasn’t ticked
- Fix: Double + Triple rebooking (i.e. rebooking a rebooking that was rebooked). You can book back and forth until your heart is content.
- Fix: Seating plan - price band validation added to ensure that price bands can’t change during sales.
- Fix: Ensure calendars have upper/lower bounds, to stop someone scrolling into oblivion
- Fix: Percentage based fees were formatted with currency instead of %, and had decimal place issues
- Gateway fee previews and price formatting in admin event sale item edit / create were fixed
- Fixed a display issue on validation errors when customer address was set to 'required'
- Updated the url in the footer of emails to favour the URL provided in settings > company details > website
- Updated the email event-image aspect ratio to more closely match the shop
- Minor bug fixes & display issues for right-to-left languages (i.e. Arabic)
- Fixed date input to follow the new formatting for 12h times
- Removed search from main navigation on all pages
- When creating time slots, the event times are now displayed for ease of reference


## 💻 Technical
- We now ensure that the exact details of items at the point of sale, are recorded (for future reporting if needed, following rebooking)
- Introduced the concept of 'protected' data capture questions which cannot be deleted under any cirumstance. This can be applied to system-critical data capture
- API: added event codes to the retrieve events endpoint
- API: added order items to the transactions endpoint
- API: added data capture answers to the retrieve customers endpoint
- Fully automated the deployment process with the option to display a maintenance mode page during critical database migrations to preserve data integrity











<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
