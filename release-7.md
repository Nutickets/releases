[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 7: July 19th - August 25th
Below you will find the summary notes for the 7th release of the Nuweb core platform.


## 🚀 New Features
- Reporting: implemented a brand new reporting UI to more easily manage fields, filters and widgets included in custom reports. Providing quicker access to information, and collapsable menus to increase table size. 
- Added the ability for purchasers to correct a transfer if they accidentally entered the wrong email address or changed their minds - this feature can be toggled on or off.
- Implemented 3D Secure V1 and V2 for Realex in the Nutickets legacy platform
- Allow discount codes/access codes to be edited, allowing codes to be changed at any time.


## ✨ Enhancements
- Allow box office users to bypass any sharing restrictions during checkout
- Extended the event search in the shop to allow searching events by venue name
- Added pagination to event blocks to allow for more than 50 events to be shown per block. Pagination links can be toggled on or off per individual block
- Added a ‘Load more’ button for map blocks that feature more than the event limit set on the block
- Social Sharing blocks now allow for a customisable list of social networks.  
- Introduced a complete refurbished design for the admin customise event page
- Admin event seating plan page additions:
    - Search for seats by name
    - Selected matched seats
    - New icons to distinguish seats that were sold, are unavailable or restricted to specific user type
- Admin Event List Enhancements: new UI, improved checkbox selection, added a plethora of actions
- New settings for how prices should be shown on event blocks/event listings:
    - Can hide/show fees
    - Can hide/show add-on items
- Added the ability to rename seating plan spaces, tables, rows, block, and stands after attaching to an event.


## 🤝 Integrations
- Implement a Single Sign-On solution to support OAuth2/OpenID Connect/Identity Server SSO providers
- Integrated our ticketing platform with the Tawakkalna COVID-19 health and safety app.


## 📱 Mobile Apps
- Added pairing with NFC tags to the android access control pro app
- Added "Kiosk" mode in the mobile Box Office app for Android

## 🧹 Housekeeping
- Fix reporting issue where ‘asked during registration’ questions weren’t appearing in certain reports when answered during checkout.
- Fix double booking issues that occurred during failed off-site payments
- Fix a restocking bug that prevented seats being re-released when the reservation was manually completed by an admin user
- Fix some price range display issues where timeslot from prices were always showing as zero
- Customer Names now show on E-Tickets
- Improved Shop Search results to remove city/tag results with no associated events
- Limited ‘fixed value discounts’ to one Currency to avoid customers gaming exchange rates for higher value discounts.
- Multi image upload component fixed and applied to event gallery blocks
- Map blocks improved to show all events when none are hovered
- Improved Google Maps API help text and tooltips
- Fix: Item validation for min/max/multiple quantities was acting inconsistently in the basket, and when rebooking.
- Refactor: Basket error messages now display more context (i.e. the event name, item type, item name, that triggered the error). This is particularly useful where a user tries to add multiple items to their basket at once.
- Fix: Assigned visibility groups weren't correctly displaying on the venues index.
- Fix: Visibility group filtering wasn't being applied to the venues filter on seating plans index.
- Fix: Seating plans were not properly filtered by a user's visibility groups.
- Fix: Allowed editing of customer email addresses via admin, when using impersonation mode from the reseller.
- Fix: Honour the live mode flag on companies, in the sales based reports. This means demo transactions will no longer show up.
- Fix: When copying events with timeslots, some sale items (particularly add-ons) were being duplicated. Prevented this from happening.
- Fix: Access codes were being counted even if items purchased didn't require them.  We now remove access codes at the point of payment, where they aren't needed.
- Fix: Issue with seating plans not respecting disabled/deleted access codes, and seats still being marked as unavailable.
- Fix: Seating Plan cache when an access code is applied. The availability image of areas remained the same, as it was not considering that different customers should see different items.
- Fixed issues with exporting/downloading reports when we are filtering by email addresses
- (internal) Corrected the automatic Stripe invoice generation


## 💻 Technical
- Fixed some blocking issues preventing the automatic audit backup script from always completing.

#### API Updates
- Added a `/sale-items` endpoint, allowing API users to retrieve complete lists of items within an account.
- Added an `/inventory-items` endpoint to retrieve a complete paginated list of inventory (global) items

<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
