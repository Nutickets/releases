[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 5: April 21st - May 21st 2021
Below you will find the summary notes for the 5th release of the Nuweb core platform. The focus points are highlighted in yellow.

## 🚀 New Features
- Added <mark>stadium reserved seating with areas functionality</mark> as well as:
    - Added the ability to choose between large and small seating plans
    - Added relative sizing based on current zoom level
    - Improved seating plan speed
    - Added autosaving in the background and reloading of unsaved plans
    - General admission font sizes can be customised
    - Added resizing support for polygon general admission and shapes
- Implemented <mark>visibility groups</mark> (VGs) which allow admins to limit user access to events (and surrounding resources) within their VGs
    - VGs can be managed and assigned by users with the appropriate permissions
    - Events, venues, listings, orders, attendance and reports are automatically filtered according to users VGs
    - Additional VG filtering can be managed via the filters in Admin
    - User VGs can be managed through our API
- Added <mark>system auditing</mark> throughout admin, hub, the box office and the API ft. automated backups
- BETA: A configurable virtual waiting room for creating a fair and reliable shopping experience during popular event launches
- Added a billing address book data capture feature which is compatible with all on-site payment processors
- Added a <mark>first-party cookie banner with a customisable cookie policy</mark>
- Added event-level booking notification emails
- Added a new 'forced checkout' setting which prevents customers from navigating away from the checkout process without losing their reservation

## ✨ Enhancements
- Added customisable UTM tracking links to all transactional emails
- Added seating plan gates & stairs to all event-based reports
- Discount codes: add the option to limit %-based codes to only one application per order
- Add the ability to display a 'tickets remaining' badge against each sale item
- Add support for multiple custom domains per shop
- Added more detailed colour previews when using custom colour palettes in branding settings
- Added a incompatible browser page displayed when a user's browser doesn't support the features needed to run our app. The page prompts them to update their browser to the newest version
- <mark>Various UI/UX improvements:</mark>
  - Improved usability of date/time pickers
  - Restructured theme/branding customisations in Admin
  - More customisation options for menus: alignment, dividing lines, layouts, social media colour choices and logo options
  - Condense items/tickets to fit more on screen
  - Improve error feedback messages
  - Toggles are now keyboard accessible.
  - Error pages have been improved to both look better and offer more detailed information.
  - Event data capture now features a user-friendly progress bar when dealing with multiple events within a single order
  - Misc layout fixes and improvements in customer emails
  - Hid ‘Calendar view’ in items modal when timeslots span only 1 day, 
- Added a new setting for controlling sale item images: either on/off or use event thumbnail
- Added option descriptions to event codes (internal questions)
- Added the option to always display item descriptions
- Added the option to show/hide venue location and show/hide venue name
- Added the ability to show/hide the discount input field in both the shop and box office
- Added ‘event pass’ tickets to ‘Calendar view’
- Timeslots purchases now show timeslot date/time rather than event date/time
- Improved currency support: Currency formatting has been improved to show large number separators, the correct number of decimal places and language-specific symbols (eg £ shows as GBP in Arabic language)
- Added a ‘select all’ toggle when bulk-editing scheduled sale items
- Added a toggle to control if an event is hidden/shown in event listings whenever taken off sale, or put on sale
- Improved event page and event blocks to more clearly show where an event is off-sale
- Add the ability to enter an alternative email address when resending order confirmation and tax receipt emails
- Box office operator details are now hidden from ticket downloads when customer details are not provided during a box office sale

## 🤝 Integrations
- <mark>Integration with PayPal Commerce Platform</mark> featuring:
  - Organiser onboarding process
  - Customisable payment page with the choice between using PayPal guest checkouts or a custom branded card form for faster checkouts
  - Support for alternate payment methods (SOFORT, iDEAL, giropay and more)
- Added new computed fields to the customer report: registration source, purchase types, ticket types, ticket purchase count & more
- BETA: <mark>A new email campaign tool</mark> has been released which introduces early access to the following features:
    - Ability to send out mass marketing emails & campaigns
    - Ability to manage multiple lists
    - Ability to use custom data capture questions to onboard subscribers
    - Ability to create automated DRIP campaigns
    - Ability to segment lists and target campaigns toward customers based on purchase history, data capture, account type and more
- Support alternate PayTabs API URLs depending on the country of origin


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
- Fix a bug where customers were blocked from downloading tickets due to incomplete data capture on certain question types
- Fix an issue preventing welcome emails being sent during a customer data import
- Fix a bug with discount code calculations on fees where fees are absorbed by the organiser
- Fix a bug with image copying when scheduling events in bulk
- Ensure multi-lingual images are displayed correctly in customer emails based on user language preference
- Basket icon is now clickable again throughout the checkout process
- Swapped event location for event venue as a primary filter as its more useful
- Fixed issue with data capture where you couldn’t disable questions set to ask on “Every ticket on every event”

## 💻 Technical
- Various API additions and updates:
  - Suspend and restore users
  - Made password field optional when creating company users to support third-party authentication systems
  - Added filtering of purchased items by event(s)
  - Added a new endpoint for capturing data capture responses via the API
  - Added consistent pagination across all API endpoints to ensure all data sets are traversable
- Switch to using background jobs for resource-intensive actions (scheduling events in bulk, setting up large timeslotted seating plans etc.) to mitigate timeout issues
- Extended feature flags to support more than a simple 'on'/'off' mechanism by adding contexts (i.e. seatings plans can be limited to small plans only, both small and large plans or disabled entirely) 










<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
