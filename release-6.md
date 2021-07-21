[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 6: May 24th - July 15th
Below you will find the summary notes for the 6th release of the Nuweb core platform.

## 🚀 New Features
- Added a new 'Payment Link' payment option when selling tickets via box office mode. This emails a unique secure URL to the customers email address allowing them to pay for their tickets within an allotted time.
- Added the ability to create access codes which allow organisers to hold seats or individual tickets from the public and lock them behind an access code:
    - Access codes can be applied either by visiting a unique URL or by entering the code manually. Manual code entry can be enabled/disabled globally.
    - Sale items restricted by the access code can only be purchased when using the access link, or entering the code. The items do not appear unless the code is entered and there is also the option to hide items outside of the applied access code.
    - Access codes also feature many of the settings available with discount codes such as max usages overall and per customer, validity dates and more.
    - Access codes have been added to sales reports, to allow the specific codes that were used, to be revealed.
- Added a quick-print option to the web-based box office mode upon completion of a sale
- Phase one of the season ticket roadmap has been launched with the option to setup pre-season season tickets. This is in request-only BETA mode until phase two is launched in the upcoming release.
- Added fractional tax band support
- Added support for same-day rebookings whereby customers can pick a different timeslot on the same day as their original booking
- Added the ability to issue online refunds for card-present stripe transactions made via our box office mobile app

### The Charity Package
- Introduced charities and donations into the checkout process. Organisers can setup one or many charities within their events and configure them to accept fixed-increment or user-specified donation amounts as well as several other donation-specific settings such as min/max price, charity website URL, charity logo etc.
- Implemented GiftAid collection and reporting which can be optionally enabled per charity and the giftaid rate can be configured at the account-level.
- Added a new "Donations Received" report alongside lots of new fields within existing reports for the new charity features
- Added fundraising support via a JustGiving integration:
  - Customers who have purchased tickets to an event can create & manage a fundraising page in JustGiving via the My Account section
  - The default settings for the generated JustGiving pages can be configured per-event

### Localisation, dates and times
- Added the ability to customise date formats within your shop and admin panel. Dates can be configured as either "Big endian", "Middle endian" or "Little endian".
- Added the ability to customiser time formats to either 12-hour or 24-hour time display.
- Added multi-timezone support; admin users can configure a company default timezone as well as a timezone per event and choose between whether or not to display timezone information throughout the shop.
- Cities and regions are now multi-lingual and translations can be populated when managing venues.
- Languages and countries will now display in the correct language according to the users preference.

### Stadiums and large seating plans
- Improved seating UI in shop / editor
- Seating tags: you can tag seats and set tags to either appear on the ticket OR on the tooltip OR use them as filters.
- New smaller features: Opacity for shapes and icons. Accessibility, gates, stand, stairs and tags for GA. Row labels will stick to row ends even when seats are hidden. Plan background colour could be changed. UI to rotate / resize elements in editor
- Filters on the seating plan to search for price bands and tags, and in the editor any stand/stair/gate. It works with areas too.
- Areas with no available tickets will be marked as unavailable
- Realtime availability: Seating plan refreshes availability in realtime, and will tell you if someone snatched your selected seats right before your eyes.
- Better UX after you add a seating plan to an event, with more guidance to finish setup
- You can get a well detailed all out information of everything on the plan in the new Plan information dialog

## ✨ Enhancements
- Added "External ID" on sale items/items, to allow for tracking of external identifiers (such as SKUs, or reporting IDs)
- Added ,andatory Title/Name/Address collection when enabling charity donations
- Added Mandatory Title/Name/Address collection when enabling fundraising
- We now load availability upfront in order to display which areas are totally sold out in large venue seating plans
- Improvements to the rapid scanning feature within access control such that it now supports the ability for customers to scan in with any barcode providing that they own at least one eligible item within their account. Previously rapid scanning behaviour only worked for addon items.
- Added the ability to manually expire active reservations within Admin
- Improvements to the virtual waiting room: allow box office staff to bypass the queue, add the ability for customers to give up their spot for another shopper, improved the waiting room timer so the customers max session time only begins counting once they reach the front of the queue.
- Display any ‘asked during registration’ questions to customers that are created outside of the normal registration flow (i.e. they were sent a ticket directly via their email address or were imported into the system by an admin)
- Display ‘applied discount codes’ when viewing orders in Admin
- Added an option for shop location to be displayed in the shop menu.
- New input for meta images, descriptions and titles for events, shops and listing pages.
- New option to display logo in top menu rather than main menu.
- UI improvements for sharing items.
- Ability to pin and unpin event actions as well as new modal for changing event status.
- New find your address search.
- Ability for users to add dynamic maps.
- Better map zoom functionality when hovering on locations.
- Listing map blocks now show all markers at once.
- Improved Apple Pass display to use either the shop background or seating tag background
- Marketing settings UI improvements - Settings are now split into categories and easier to find.
- Video blocks on event pages have been improved to access timestamped YouTube video URLs.
- Uploading images to Image Blocks in the Event Customisation page now adds the image to all active locales to help speed up setup. 
- Added venue information to ‘More details’ dropdown on Order Summary.
- Made customer account pages more responsive to smaller mobile devices.
- Added icons alongside the Profile menu options in Shop, to improve accessibility and offer visual queues to non-native language speakers.  

## 🤝 Integrations
- Apple Pass: Now you can scan a QR code from your computer with your iPhone to add Apple Pass to your phone, or add it to your Apple Wallet through Safari
- Integrated with Apple Sign-In, enabling customers to login with their Apple ID.
- Added a “Hosted Payment Page” option to the PayTabs integration which supports APMs such as Google and Apple Pay

## 📱 Mobile Apps
- An iOS Access Control hybrid app has been released, which supports both the legacy Nutickets platform and the current system.
- Added support for fully offline entry scanning in the Android Access Control app
- Added NFC pairing functionality to the Android Access Control app, compatible with the new system.

## 🧹 Housekeeping
- Fix: When part way through a form wizard (i.e. event creation), if users changed companies in another tab, the original form wizard could still be submitted with objects that weren't owned by the new company (i.e. venues)
- Fix: Inclusive discount code dates were setting the time element to midnight, meaning discount codes were expiring 23 hours and 59 minutes early
- Fix: Copying events was not properly copying the price band IDs for a seating plan.
- Fix: Seating plan availability not always being displayed properly on the seating plan, with customers facing "seat unavailable" messages if they then tried to add the seats.
- Fixed sold out badge showing twice in the shop.
- Fixed linebreaking UI issues throughout admin
- Fixed mobile view cutting off items and timeslots.
- Fixed team settings bug stopping this functionality from being disabled
- Disabled refund buttons if you've already refunded.
- Mobile UI improvements throughout checkout.
- Fix timeslot picker not working in safari.
- Fix all maps pins showing the same location.
- Error messages now appear inside iFrames/Modals for full visibility.
- More Arabic / RtL improvements have been applied.
- Fixed an issue when scheduling events in bulk occasionally producing multiple separate schedules
- Ticket prerequisites (customers must purchase one item before purchasing another) are copied over during event scheduling
- Fixed some inconsistent 403 error pages displaying in admin data capture pages
- Fixed an issue when refunding an order after a rebooking where it was previously showing the cancelled items and totals in the refund confirmation email
- You can now remove filters from custom reports as with any system report
- Fixed schedule report issue where on rare occasions, the wrong report was being attached to the email
- Fixed an bug preventing customers from accessing tickets when transferred back to the original purchaser
- Corrected the ‘verify your email address’ link that is sent after registering via a social login
- Reactivated Facebook login globally
- Fixed an issue whereby hub users couldn’t assign roles that they had, to other users.

## 💻 Technical
- Refactored: Seating Plan Import Experience
    - Seating plan importing is now batched into smaller tasks, allowing larger plans to be imported more reliably.
    - Doing this also means that other customers/clients aren't impacted whilst we wait for a large plan to import.
    - The UI has been updated to show the progress so that the spinner has more context than 'please wait'.
- Refactored: Bulk Event Copying + Bulk Timeslot Creation Experience
    - As with the seating plan changes, the copy event + bulk timeslot processes were refined in order to utilise the same batching process as with seating plans.
- Add: A delta availability payload on seating planned events, in the shop.
    - This allows a much smaller amount of data to be downloaded, to keep seating plan availability up-to-date, by passing a 'last updated' timestamp and receiving a delta payload of any changes since then.
- Refactored: Availability information for seating plans, to be more performant - especially on larger seating plans.
- Cookie banner now respects the ‘base domain’ setting in Admin (if available) to allow cookie banner to work on custom domains.

### API Updates
- Added full set of API endpoints to accomodate offline entry scanning
- Added NFC pairing API endpoints allowing tickets to be paired with NFC tags
- Added a 'lastUpdated' filter to several endpoints (GET /customers, GET /orders/items, GET/events) to allow filtering of data based on the modified time
- Various fields have been added to make linking and filtering data easier: Customer ID has been added to any endpoints that include order information, added the ability to include order items when retrieving orders in bulk, added separate first and last name fields when retrieving customers, add created and updated at timestamps to all events and tickets, added event ID where missing, made eventId optional when retrieving tickets, restructured event codes to lighten the payloads for accounts that have lots of internal data capture questions.




<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
