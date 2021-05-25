[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 5: April 21st - May 21st 2021
Below you will find the summary notes for the 5th release of the Nuweb core platform. The focus points are highlighted in yellow.

## 🚀 New Features
- Added stadium reserved seating with areas functionality as well as:
    - Added the ability to choose between large and small seating plans
    - Added relative sizing based on current zoom level
    - Improved seating plan speed
    - Added autosaving in the background and reloading of unsaved plans
    - General admission font sizes can be customised
    - Added resizing support for polygon general admission and shapes
- Implemented visibility groups (VGs) which allow admins to limit user access to events (and surrounding resources) within their VGs
    - VGs can be managed and assigned by users with the appropriate permissions
    - Events, venues, listings, orders, attendance and reports are automatically filtered according to users VGs
    - Additional VG filtering can be managed via the filters in Admin
    - User VGs can be managed through our API
- Added system auditing throughout admin, hub, the box office and the API ft. automated backups
- BETA: A configurable virtual waiting room for creating a fair and reliable shopping experience during popular event launches
- Added a billing address book which is compatible with all on-site payment processors
- Added a first-party cookie banner with a customisable cookie policy
- Added event-level booking notification emails
- Added a new 'forced checkout' setting which prevents customers from navigating away from the checkout process without losing their reservation

## ✨ Enhancements
- Added customisable UTM tracking links to all transactional emails
- Added seating plan gates & stairs to all event-based reports
- Discount codes: add the option to limit %-based codes to only one application per order
- Add the ability to display a 'tickets remaining' badge against each sale item
- Add support for multiple custom domains per shop
- Various UI/UX improvements:
  - Improved usability of date/time pickers
  - Restructured theme/branding customisations in Admin
  - More customisation options for menus: alignment, dividing lines, social media colour choices and logo options
  - Condense items/tickets to fit more on screen
  - Improve error feedback messages
  - Toggles are now keyboard accessible.
  - Error pages have been improved to both look better and offer more detailed information.
  - Event data capture now features a user-friendly progress bar when dealing with multiple events within a single order
- Added a new setting for controlling sale item images: either on/off or use event thumbnail
- Added option descriptions to event codes (internal questions)
- Added the option to always display item descriptions
- Added the option to show/hide venue location and show/hide venue name
- Added the ability to show/hide the discount input field in both the shop and box office
- Email improvements - layout improvements, timeslots purchases now show timeslot date/time rather than event date/time.
- Timeslot display improvements - Hid ‘Calendar view’ in items modal when timeslots span only 1 day, added ‘event pass’ tickets to ‘Calendar view’.
- Improved currency support - Currency formatting has been improved to show large number separators, the correct number of decimal places and language-specific symbols (eg £ shows as GBP in Arabic language).
- Added a warning to show when a map block has been added to an event page and the related venue does not have valid longitude/latitude coordinates.
- Google tag manager has been moved to marketing settings, alongside cookie banner.
- Added a ‘select all’ toggle when bulk-editing scheduled sale items.
- Added a toggle to control if an event is hidden/shown in event listings whenever taken off sale, or put on sale. 
- Improved event page and event blocks to more clearly show where an event is ‘Off Sale’.


## 🤝 Integrations
- Integration with PayPal Commerce Platform featuring:
  - Organiser onboarding process
  - Customisable payment page with the choice between using PayPal guest checkouts or a custom card form
  - Support for alternate payment methods (SOFORT, iDEAL, giropay and more)
- Added new computed fields to the customer report: registration source, purchase types, ticket types, ticket purchase count
- BETA: A new email campaign tool has been released which introduces early access to the following features:
    - Ability to send out mass marketing emails & campaigns
    - Ability to manage multiple lists
    - Ability to use custom data capture questions to onboard subscribers
    - Ability to create automated DRIP campaigns
    - Ability to segment lists and target campaigns toward customers based on purchase history, data capture, account type and more


## 🧹 Housekeeping
- Added feature toggles in Hub for various event add-ons (products, guest lists, streams, teams, access control, data imports and more)
- Allow carring over seating plan across multiple scheduled events
- Prevent duplicate event listing URLs
- Fix rebooking issues when global basket is disabled
- Fix event price range inaccuracies where off-sale tickets were incorrectly included
- Fix a password reset bug for companies using alternative admin subdomains
- Fix bug where scheduling events would occasional fail silently
- Fix minor GTM tracking bugs when using a redirect payment method
- Fix automatic invoice generation bugs
- Fix permission bug preventing you from removing certain abilities from a role

## 💻 Technical
- Various API additions and updates:
  - Suspend and restore users
  - Made password field optional when creating company users to support third-party authentication systems
  - Added filtering of purchased items by event(s)
  - Added a new endpoint for capturing data capture responses via the API
- Switch to using background jobs for resource-intensive actions (scheduling events in bulk, setting up large timeslotted seating plans etc.) to mitigate timeout issues
- Extended feature flags to support more than a simple 'on'/'off' mechanism by adding contexts (i.e. seatings plans can be limited to small plans only, both small and large plans or disabled entirely) 










<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
