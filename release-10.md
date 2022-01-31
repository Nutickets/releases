[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 10: November 22nd - January 24th
Below you will find the summary notes for the 10th release of the Nuweb core platform. This release had a heavy focus on housekeeping and general UI/UX improvements as well as streamlining our processes going forward into the new year.


## 🚀 New Features
- The admin event dashboard has been redesigned and features brand new event level statistics on sales, attendees and orders:
    - New event status block containing status, payment link option and the most important actions.
    - Filtering of statistics based on currency and time period.
    - New statistics block containing high level statistics for all sale items, timeslots and pricebands.
    - New behaviour for when we show either statistics or actions on an event based on its status.
    - Option to see the top four selling items within each statistic item group.
    - Links to relevant reports for all statistics.
    - New actions block.
    - Better use of colour on event dashboard with certain item groups being assigned colours that aren’t the primary theme colour.


## ✨ Enhancements
* Box Office Users are no longer treated 
    * Removed: User email address in box office mode, when operating as admin user.
    * Removed: "Customer" details on orders, where box office user was admin user.
    * Removed: Option to send confirmation email, where operating box office as admin user (i.e. not allocated to a customer).
    * Removed: Box Office unallocated orders (i.e. no customer) are not included in the mass email lists for resending tickets, or emailing attendees.
    * Removed: Box Office users from the customers list.
- Reporting Improvements:
    - Added event fields and a customer filter to the scanning reports
    - Implemented temporary report generation and results caching for larger reports
    - Improved the exporting of reports to handle larger datasets via batch processing
    - We also use this new exporting functionality to generate our scheduled reports.
    - Improved the inputs for multi-select and single-select filters
    - Added a Report Exports page in both Admin and Hub which allows you to:
        - See the report export status (whether the export has finished and is available to download or is still
          exporting)
        - See a history of all previous exports, meaning you can easily re-download and previous exports
    - Added a report export email to notify you that your export is ready for download, with a link that takes you
      straight to the report export page
    - Added an email to notify you if the report failed to export.
    - Updated the scheduled email to include a link to download the report, rather than attaching it to the email. This
      prevents future issues of emails not reaching the end user if the file is too large.
- Redesigned the API docs with a completely new UI and improved documentation with clearer explanations and sample code
* Add: Sale item "additional info" in event media.
* Add: Item "description" in event media
* Add: Ability to delete charity/sale item parents, even when they contain children
    * If any of the children are part of reservations/orders, the whole group is taken off sale.
    * If any of the children (or parents) are attached to another event, the underlying item isn't deleted but the sale item itself is.
- Improve breadcrumbs in our wizards across Admin and Hub to improve the flow.
- Added date search to the multi-select sale item search component
- Integrated measures to prevent bots from abusing the company registration form.
- User permissions/roles UI tidied up, as well as paginating the records that are returned when selecting permissions
  for specific entities rather than loading the entire list of entities which was crashing the browser
- Changes to GTM/Google analytics: we now track the events triggered when first landing on the site, once the user opts-in to analytical cookies

## 🎨 User Interface (UI/UX)
- Improved the phrasing on the transfer interface when correcting a transfer
- Deployed a number of mobile optimisations covering the following areas:
    - My account
    - Responsive button / text sizes
    - Progress bars
    - Admin: event dashboard
    - Shop: Browse page
    - Shop: My account pages
- Added quick link pinning in admin & hub.
- Replaced the regular event page with a full page buy-now modal when browsing in box office mode.
- The admin event index page now groups events by date
- Release notes links have been added to Hub
- A number of UI tweaks & improvements have been made to the Fundraising pages in the shop.
- Modal headers and footers automatically snap to top and bottom of mobile screens
- Improved statistics shown on hub and admin dashboards to match the new event dashboard feature
- Fixed issue where focus was trapped inside the price-input, preventing the tab key from shifting focus to the next element in the form.
- Improved Breadcrumbs - Cleaner code, more granular breadcrumbs for wizard forms, better mobile breadcrumb UI.
- Improved Icons - Cleaner code, improved consistency with icons across the app.
- Mobile optimisations to the events index page in shop & the admin global search results.
- Admin filters UI improvements - Used the filter-collapse column layout from the reports pages in more commonly used index pages for cleaner UI.
- Accessibility improvements - Added a ‘Skip the main content’ link in the top left of the admin, for easier keyboard navigation.
- Added the ability to add order notes to an order on the success screen of box office checkout.
- Cleaned up the UI for the order summary in shop.
- Improved the UI of the new payment settings cards in admin.
- Fixed a bug where three-column layout event blocks did not render properly on mobile devices - Also improved the slider so it can be used by trackpad users as well as touchscreen devices.
- Added a Javascript linter to improve code formatting and consistency, reducing chance of future merge conflicts causing breaking changes.


## 🧹 Housekeeping
- Fix an issue in the scanning reports where on some occasions it was incorrectly aggregating the total scans (in/out)
- Fix a bug with event level ticket limits where it was incorrectly identifying users as having reached the ticket limit
- Fixed an incomplete data capture bug blocking shared ticket downloads where only the purchaser had incomplete data capture
- Fix an issue where the browser back button would block subsequent form submissions
- Fixed discount codes buy x get y formatting
- Fixed infinite loader appearing on assign items modal
- Fixed image upload not uploading properly
- Fixed ‘view’ button on image uploads to work again
- Fixed related events not showing on event page
- Fixed the taxes dropdown showing before a user has enabled currency on event creation
- Fixed tall visibility groups drop down on event dashboard
- Fixed percentage discount input relying on currency restrictions to appear
- Fixed map block not displaying on customise event page
- Fixed top-level edit buttons disappearing on event customise page
* Fix: Ensure that pre-requisites are validated at the 'whole order' level, to avoid issues where pre-requisites are not yet in the basket when attempting validation.
* Fix: Overstocking occurring in some edge cases
    * It was observed that where a user runs their expiry timer down to the last seconds, it's possible that an order could both be successful and unsuccessful, resulting in an overstocking of certain item types.
* Fix: Issue with some orders having both live and demo transactions (particularly those with refunds or rebooking entries).
    * As part of this all old orders were backfilled to ensure their data is/was correct.
* Fix: Charity donations were not being duplicated properly, when copying/scheduling events. The resulting copied charity was being added to the original event, not the new one.
* Fix: Charity donation variations could not be deleted.
* Fix: Seating plan allocation report was ignoring the status of orders, and showing expired, reserved (unpaid), and refunded orders as occupying spaces.
* Fix: Discount codes couldn't be used properly in box office mode, where the company settings only permitted 'box office only' entry of codes.
* Fix: Discount codes using a currency that is no longer enabled on the company, break the edit form of that discount code.
* Fix: Incorrect 'event level' timeslot price ranges, caused by an incorrect cache key being used, which meant the prices at this level were being incorrectly retrieved.
- Fix bug where access codes would sometimes not reveal sale items
- Fix bug where box office users no longer randomly load a basket
- Added prompt to give admin users the choice to skip the waiting room if the shop is currently too busy
- New test runner pipeline
- Add default “valid for” setting for how long payment links should live for before expiring
- Fix bug where resending emails for an event would sometimes also send an email to an order item of another event
- Reservations now show seating information
- Clicking view site in the top nav will show a reminder that you’re in box office when applicable
- Fix bug where clicking view site would not let you exit box office if you opened box office in another tab
- Fix validation error message where user could not turn manual payments off if they’ve never entered payment instructions before
- Fix bug where a non-seated ticket could not be added to a event with a seating plan assigned
- Incorrect reset email URL in the password reset email for specific hub users who have admin users registered under the
  same email address
- Fixing an issue where the company index page could not be viewed in Hub in Firefox.
- Fixing an issue with tickets disappearing in the UI if a pending transfer request was cancelled
- Fixing issues with the customer global search in box office that were 404'ing
- Fixing issues with headers being removed when a report was being saved as a custom report
- Fixing an issue preventing headers from being removed from custom reports


## 💻 Technical
- Deployed a new UAT environment for early testing of new development work against (anonymised) production-like data.
- Reduced the amount of JavaScript loaded on each page visit by up to 75% in some areas of the system.
- Implemented several improvements to our internal QA and development processes such as automated code compiles, upgraded dependencies, unit test runners, automatic coding standards and more.
* Add: 'rebooked from ID' is now tracked on individual order items.
* Queued Job Improvements:
    * We now store the company/context details within the queued actions, to ensure that the action remains context aware and ensure better segregation between companies.
    * Provides opportunity to store queued tasks for companies, and surface this information in the UI as required (seating plans, event timeslot creation, etc).
    * Using the above, we now have a 'queued job' page in admin UI which allows all pending jobs to be displayed, and their progress tracked.
* Refactor: Changes to the way in which we track box office mode through the store.
* Add: CalculateEventCapacity action, to accurately calculate the potential capacity of an event, considering all capacity restrictions in place.
    * This is built in a generic way such that this data could be surfaced elsewhere at some point in the future.


### API
Changes to the API are now documented exclusively in the changelog on the API documentation homepage.


## 🩹 Patch Notes
Below is a summary of all software patches made throughout this release period, outside of the regular scheduled release cycle. Patches follow the same structure as a regular release and can involve bug fixes, UI improvements or even brand new features.

#### 20th November 2021
* Fix: Guests lists were set as downloadable by default, but you could not disable this via the guest list create/edit form.
* Fix: Rebooking was failing for items where the "purchase limit of [1] per customer" was enabled, as the validation for the rebooking would not allow the user to posses a second of those item(s).
* Fix: Events with all items hidden behind an access code, could not be sold in box office.
* Fix: Incorrect display of "Sold Out" in box office mode, when using access codes.
* Fix: Remove the `event pass` timeslot, where no event pass tickets/season tickets exist.
    * This also fixes the issue with the event level timeslot showing 'from free', incorrectly.
* Fix: 500 error being shown on the reservations list, when attempting to view expired reservations.
* Fix: Event capacities were overinflated for some season ticket sales.
* Fix: Event ticket capacities were not showing season ticket sales properly, in some situations.


#### 3rd December 2021
* Fix: Rebookings involving products/guest lists and timeslots, were not always presenting correct options.


#### 17th December 2021
* Add: New feature toggles for changing the customer journey during checkout:
    * Feature toggle to force profile questions to be asked during data capture on every purchase
    * Limitation toggle to prevent profile information from being edited outside of the checkout journey
    * Limitation toggle to prevent data capture from being edited post purchase
* Add: "Force Minimum Quantity" setting for events, which when enabled will force users to add the minimum quantity of items to their basket as part of their order (i.e. they cannot select '0').

#### 20th December 2021
* Fix: issue with progressing from the delivery details page, to payment page, in checkout, where customers had outstanding transfers associated with their account.

#### 11th January 2022
* Add: Filter out events from child companies that are in demo mode
    * This does not apply if the parent company is also in demo mode.
* Fix: The event link component for external URLs, which mainly prevented parent companies from allowing customers to click on child events.
* Fix: Issue with "page has expired" messages where parent companies were using their apex/root domain, and were not redirected to their www. subdomain.

#### Post-release fixes
- Fix server performance degradation issues
- Fix 404 on event save for child events using parent company venues
- Fix a few instances where reports would fail to generate
- Fix an issue where a season tickets scanned into 1 event would prevent scanning into other events within the season
- Fix a ‘502 gateway error’ message when attempting to exit box office mode after the customer selection step



<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
