[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 8: August 31st - October 20th
Below you will find the summary notes for the 8th release of the Nuweb core platform.


## 🚀 New Features
The major focus of this release has been about enhancing our box office product, diving deeper in season ticket functionality and delivering an initial framework for designing bespoke eTickets / printable media.

#### Box Office
- Added several new box office payment methods: “Invoice”, “Gift Card” and “Reserve to pay onsite”
    - Invoice: customisable payment instructions will be emails to the customer, once the money has been received you can complete the order from the new dashboard or from the reservation page
    - Gift card: allows you to run reports on orders paid with physical gift cards
    - Reserve to pay onsite: keeps the reservation active until marked as either complete or released within admin
- Add the ability for admin/box office users to generate a new barcode for any purchased item
- Add a number of useful download options in admin & box office including the ability to share the download links via a QR code.
    - The QR code can link to a direct download or require a full account creation and data capture to be filled in by the customer prior to accessing the tickets
- Added a “pay now” button in the my account section for customers with outstanding payment links
- Added the ability to change the purchaser post-sale from admin & the box office
    - This also comes with the ability to regenerate barcodes and transfer ownership of the purchased items at the same time
- Added the ability to one-click quick-sell the same items in an order
- Added the ability to one-click start a new reservation with items from an existing order
- Added the ability to transfer individual tickets or multiple tickets from the same order from admin & the box office
- Added quick sell buttons for each payment method to the event page when selling tickets in the box office
- Added the ability to send payment link reminder notifications
- Allow editing of the basket total whilst processing a box office sale
- Add: Button on the event seating plan page to begin a box office order with the selected seats (if available).
- Add: Admin users can now reallocate (or swap) bookings between spaces for the same event
- Added a new dynamic box office style dashboard to the admin, which displays certain elements depending on what level of permission you have
- Allow box office users to bypass all data capture validation when processing sales
- Updated box office mode to display events, timeslots and tickets that would otherwise be hidden, unavailable or sold out in the shop
- Add: New button on the item selector modal, to allow box office users to force a refresh of availability for seating plans.
- Add: Customer selector on the navbar before an order exists, allowing pre-selection of a customer to checkout as
- Add: New button on the 'view customer' page to start box office mode, as the selected customer.

#### Season Tickets
- Add: Respect season ticket sales throughout entire event schedule - this allows for season tickets to be used as upsells on any event in a single schedule.
- Add: Disallow season ticket purchase where event-day items are purchased for those seats (or capacity is reached), in the schedule.
- Add: Attendance Reports now allow you to see the season ticket that has access to an event, even if it wasn't purchased in that event.
- Add: New toggle on attendance reports to ungroup/group season ticket sales, so that you can quickly see which event a ticket was purchased in.
- Add: Support for season tickets on general admission areas - we'll always respect the general admission capacity across the entire schedule.
- Add: New setting to allow season ticket sales to count towards ticket capacities.
- Add: Dynamic capacities for event/tickets, to take into account the sale of season tickets (where appropriate).

#### eTicket & Apple Pass Builder
- Add: Event Media Management Page - allowing viewing, creation, and editing, of event media (eTickets, receipts, printables)
- Add: Apple Wallet Pass settings, to allow you to specify which apple wallet pass design is used for tickets/season tickets/products/guest lists.
- Add: Suitable default templates for all scenarios, in the event companies haven't configured their printables or passes.

#### Reporting
- Add filters to financial reports allowing you to split the currency from the amount for easier manipulations of the numbers when exporting into spreadsheets
- Add the option to display refund transactions as negative values in the transaction reports
- Add: Price Band, Stand, and Area Utilisation reports - showing number of sales across price bands, along with financials.  These can be viewed on a per event basis, or aggregated across all assigned events/schedules.
- Add: Space allocation reports - showing all spaces for the selected events/schedule, along with the allocations that currently exist.  If no allocation exists, the space is still displayed. Also respects season ticket purchases.
- Added Transfer reports
- Split out name into first name and surname across all customer-centred reports. The original (full) ‘name’ field is still available as a default header
- Include add-ons and the ability to filter them in the attendance reports
- Added a number of reporting quick-links throughout the dashboard allowing you to view filtered views as a report, such as orders, reservations, customers, transactions and more
- Added many more relative date filter options to all reports


#### Discount Upgrades
- Add: "Visible in Box Office" toggle within admin when creating a discount code
- Add: "Visible in Shop" toggle within admin when creating a discount code (this remains disabled for now)
- Add: Discount code selector on the basket/checkout pages, showing available discounts (based on visibilities). These codes are pre-filtered to only show codes that are applicable to the current basket
- Add: Ability to assign a specific role ID to a discount code, so you can only use that discount code if you have that role, in box office mode.
- Add: New ability to control which members of the box office team can create arbitrary discount amounts on the fly.
- Add: New 'overuse' toggle when creating discount codes, to allow overuse when in box office mode.



#### Quality of Life Features
- Added the ability to customise the order in which events display in custom event blocks
- Added an Admin Global Search enabling organisers and box office staff to search the database of customers, orders, reservations and events from anywhere in the system
- Added the ability to quickly jump out of box office mode when trying to visit the ticket shop from admin
- Add an automatic stock adjustment function in place allowing organisers to refund without stocking
- Added the ability to filter audits by subject ID
- Allow changing the price band of a seat from the manage seating plan screen
- Add: Button on the item modal for seated events, to take you directly to the seating plan management page in admin
- Add: UI to edit the total stock for individual spaces, for a single event. (seats are capped at 1 whereas general admission areas can be set to any number)
- Added 'View in seating plan button' when viewing an order
- Added links to Orders/Reservations/Attendance reports from the event dashboard
- Added timeslot and sale item filters to the attendance section
- Added links to Scanning/Zone Summary/Customer Journey reports from the Access Control Dashboard (formerly, the "manage zones" section)



## 🎨 User Interface (UI/UX)
- A wide range of features and UI improvements have been made to offer Admin Users the ability to sell Items at a physical Box Office
- Incorporated box office mode into the admin section to create a streamlined box office sales experience for staff members
- Added French and Hungarian support
- Multiple Payment Gateways now show more uniformly in mobile size screens
- Date picker inputs have been revamped in reporting
- Event actions dropdown now respects user permissions more closely, showing only actions that the user has access to perform
- Better Price-input that respects all locales and currency formatting
- New Customer Account layout offering better access to Customer Orders, Items and Profile information.
- Data Capture UI improvements
- Improved Event Page and Admin Event Dashboard to offer easier access to core features
- Improved maps in the Shop to make pins and events easier to navigate
- Improved the Shop Menu so lengthy menus appear neatly even on lower resolution screens
- Report widgets key labels now show correctly
- Fixed bug where 'Bulk Edit' modal sometimes did not appear as expected
- Fixed some smaller bugs in the seating plan editor
- Fixed some translation issues across the Admin
- Improved Shop footer UI, offering more flexibility in customisation
- Fixed an issue where the 'restricted' item badge was not showing when expected
- Fixed an issue where Event level capacities were not considered during the calculation of 'Items Remaining'
- Fixed an issue where Event Passes were not showing when expected



## 🧹 Housekeeping
- Added clearer messaging and better handling of errors when rebookings cannot be processed
- Correct links on event listings for events that are not part of a schedule but appear within an event block which groups events into schedules
- Fix an issue with price ranges on the event listing pages after switching to an alternate currency
- Fixed an issue where some emails were showing the wrong subject line when using custom subjects
- Fix an issue preventing guest checkouts using emails that exist as customers from other resellers of the platform
- Prevent pending transactions incorrectly appearing within an order when double submits were made
- Hide payment gateway selector in box office mode when not opting to pay via online card
- Fixed an issue where events were not showing on certain listings if the first event of the schedule was missing a required tag



## 💻 Technical
- Add: New 'description' field for discount codes, which is automatically generated, to describe the discount that's being provided [used in the box office discounts].
- Add: Event Schedule reporting filter, for use in future reporting modifications.
- Add: Seating Plan Spaces are now linked between events, where the same seating plan was used. This provides incredible opportunities to introduce features where we need to quickly get details about all related seats across an entire event schedule.
- Fix: Ensured that the access control app respects visibility groups on all expected areas (events, sale items, orders, zones).
- Fix: Rebooking was broken for orders that contained a season ticket for an event without a seating plan. This is now fixed and those season tickets are removed from the rebooking process.
- Fix: Transfers made in box office mode, were revealing the name/email of the staff member. This now just shows the company name.
- Fix: Issue where guest checkout was shown as 'not available' where customers were already guests within a specific reseller, even if not a guest at that specific company.
- Add: Event start/end dates to the attendance reports.
- Improvement: Improved the performance of the availability updates on seating plans with areas.


## 🩹 Patch Notes
Below is a summary of all software patches made throughout this release period, outside of the regular scheduled release cycle. Patches follow the same structure as a regular release and can involve bug fixes, UI improvements or even brand new features.

#### 2nd September
- Added a new ‘upsell wizard’ feature toggle to admin > general settings which encourages customers to purchase upsells after selecting their tickets

#### 10th September
- Added new timeslot settings: on sale from/until dates as well as the ability to hide them when out of stock and/or off sale
- Several improvements to refunds:
    - If an online refund fails, the message from the gateway is displayed to the user issuing the refund
    - Bulk refunds are now processed in a background job to remove the chances of a browser timeout occurring and interfering with the refunds
    - Admin users are now sent an email summarising the refunds that were processed during a bulk refund as well as detailing any problems that might have prevented a refund from being issued.
- Rebooking now allows both customers and staff to rebook to a different item of equal value where previously it only supported same item different time-slot/event.
- Fixed an issue preventing you from setting a timeslot capacity to zero
- Added one-click pause/resume sales buttons to all timeslots and sale items in admin
- Added the ability to hide timeslot start/end dates for situations where only the earliest or latest arrival times are relevant
- Introduced the concept of ‘global’ vs ‘assigned’ data capture columns in the reporting section which allow you to group repeat questions into a single column

#### 22nd September
- Corrected the logic ‘external fees’ column in the sales report to accurately reflect the amount-per-item contributed towards the fee charged by the gateway
- Added event-based headers to the orders & transactions reports including event IDs, names, dates and custom internal questions (event codes)
- Added new total received headers to both sales & transaction reports which is based on actual transaction fees (only applicable to PayPal transactions at present)
- Fixed shop menu display issues on smaller screens when lots of menu links are active

#### 23rd September
- Fix event descriptions not being saved when auditing and visibility groups were both enabled
- Added upsells (products, donations, guest lists) to reserved seating events where they were missing from the UI
- Improved the flow for addons to ensure customers cannot miss them during checkout


<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
