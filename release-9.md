[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 9: October 20th - November 18th
Below you will find the summary notes for the 9th release of the Nuweb core platform.


## 🚀 New Features
- Introduced feature toggles to prevent the creation of free tickets, disable modification of past events, disable refunds for past events and enforce event organiser information to be filled out for every event.
- Add: "live mode" filter on sales/order reports, allowing "all", "live only", "demo only", or "company settings" to be chosen.
- Revamped the relative date filters throughout all reports with the following changes:
    - Introduced several new options such as "Week-to-date", "Last 7 days", "Last year" and many more
    - Eliminated ambiguity with some existing options, i.e. "Last month" was changed to "Last complete month". E.g. if today is Thursday 21st October, the 'last complete month' would be September.
    - Added the date range to the title of reports for absolute clarity of the applied date filters
- Added 'Account Manager' field to companies in hub which can be used as a filter when viewing companies & reports
- Added the ability to view a purchased seat on the seating plan directly from the purchased item detail page
- Added 'Powered by', 'From name' and 'From email' options to companies where previously they were only available at the reseller-level
- Added the ability to send a one-off communication email to all attendees of an event
- Added some variant options for Apple Passes - Event Strip & Event Background, Generic Square & Generic Rectangular.
- Added the ability for guest users to rebuild their basket. Previously only users signed in to the system had access to this feature.
- Added the ability to edit the body text for the emails of Scheduled Reports.
- Added a new "Hide Attendees" toggle when editing a zone, allowing you to control if the attendees tab is visible/hidden in the access control app.
- Continued improvement of the new "printables" feature which allows total control over the appearance of PDF & apple pass tickets:
    - Added variables as an object
    - Reworked text adding, interface and options on seating plans and event media
    - Added Ticket data customisation and empty text customisation
    - Fixed lines, rotations, resizing
    - Added more interactive hover effects

## ✨ Enhancements
- Remove mandatory fields from the zone-based reports so that it can be customised to a more precise set of headers
- Add Finnish, Swedish, German, Italian, Greek, Slovenian and Canadian French language support
- Added the ability to cancel a seating plan sync/assignment whilst it's still processing.
- Event listing subheadings can now be translated
- Various dashboard performance improvements for a snappier load time
- Added useful report links to the event dashboard
- Added useful attendance links to the event dashboard
- Implemented the "Has timeslot" and "Sale Item" filters to the attendance reports, to match what is available in the attendance section
- Internal questions can now be copied when copying an event or scheduling repeats
- Added non-ticket items to the Download page in the shop
- Added a 'use these images for all languages' button to the Image block on Event page-settings, to more easily complete multi-locale event pages.
- Added Order success page to the Admin Text Manager
- When you leave box office, any items that were in your basket are now automatically removed.
- Event data capture has been added to the Customer Journey report.


## 🎨 User Interface (UI/UX)
- Quantity selector button now adheres to the company branding colours
- Added a more obvious display of which box office user is currently signed in.
- Added a new customer search component used in the Box Office and Admin for searching customer emails or names and automatically populating forms.
- Added a new action card container component which optimises how many actions we show on mobile by presenting a 'view more' dropdown.
- Added a new design for Box Office customer selection during box office checkouts
- Improved UI for the 'you are about to leave box office' messaging
- Box office buttons now follow Theme settings (shape / colour)
- General Admin Dashboard UI improvements


## 🧹 Housekeeping
- Prevent overselling in some situations when using ticket categories in the legacy platform
- Changing currency on dashboard no longer results in 'NaN' being displayed.
- Changing relative date period on dashboard now correctly reloads data.
- Fixed bug which hid event description from being editable if event was not created with one.
- Fixed bug where custom season ticket label wasn't appearing in order summary or basket page.
- Fixed various modals not being displayed properly in mobile.
- Fixed bug where the mass update modal was not triggering properly for certain event fields like name and description.
- Fix issue with not being able to download invoice PDF.
- Fix Data Capture validation not being applied when answering questions after checkout that were marked as hidden during checkout.
- Fix Data Capture issue where partially refunded items were still expecting data capture responses.
- Increased maximum image size validation to resolve issues with not being able to upload JPEGs.
- Removed several buttons throughout admin from users that do not have the required permission level to perform that action


## 💻 Technical
- Removed orphaned seats from old events, which no longer have seating plans attached.
- Fix duplicate seats which were causing integrity issues with data. These did not impact event sales as they were often for old test events.
- Fix an issue where the admin dashboard was incorrectly hiding certain orders from the gross/totals/counts, where part of the order was completed in demo mode.
- Performance issues with pairing and scanning tickets have been resolved.

### API
- Added an array of Timeslot data to the `GET /activated-events` endpoint
- Improved order search by adding a `query` parameter to the `GET /orders endpoint`, meaning you can now search orders by customer email, customer full name, order reference or event name.
- New endpoint `POST /guestdata` added, which allows you to synchronise all guest list data to your access control device
- New endpoint `PUT /guestdata` created, which allows you to update the current number of guests that have attended (for a particular guest list order item).
- Added new `permissions` attribute to the `GET /activated-events` endpoint, containing information on whether the authenticated user can or cannot edit the event.
- Added a new `hideAttendees` attribute to the `GET /zones/all` endpoint, allowing for us to control if the attendees tab in the access control app is or is not visible.


## 🩹 Patch Notes
Below is a summary of all software patches made throughout this release period, outside of the regular scheduled release cycle. Patches follow the same structure as a regular release and can involve bug fixes, UI improvements or even brand new features.

#### 22nd October 2021
- Fix the ordering of customers on the dashboard so that it always displays newest registrations first
- Fix the inability to delete company branding logos/icons.
- Fix a bug for multi-company accounts where changing companies didn't update the dashboard statistics

#### 25th October 2021
- Fix a display-only bug where parent company event listings weren't respecting child company access codes

#### 26th October 2021
- Various fixes to the customer list in admin to resolve issues where some links were 404ing and some customers were being listed more than once

<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
