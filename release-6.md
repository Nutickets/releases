[![logo](https://user-images.githubusercontent.com/57409655/115874120-a567c880-a43b-11eb-95ea-9297cfea6658.png)](/releases)


# Release 6: May 31st - July 15th
Below you will find the summary notes for the 6th release of the Nuweb core platform. The focus points are highlighted in yellow.

## 🚀 New Features
* Add: Access Codes
    * Allow the creation of 'access codes', with associated sale items.
    * Access codes could be added to a customer's session via URL, Session token, or a form
        * The link to the form on the shop is only showed when the access code settings for 'display modal form entry' are enabled. This is disabled by default.
    * Sale items restricted by the access code can only be purchased when using the access link, or entering the code.  The items do not appear unless the code is entered.
    * Setting added to disable the sale of unrestricted items when an access code is entered - they are removed entirely from the sale item lists.
    * Access Codes can have validity dates - they can only be used between those dates + times. Outside of those times, the restricted items do not appear.
        * There is a toggle that allows for restricted sale items to go back to mass market sale, after the validity window closes.
    * Access Codes can have their own permissions applied for users.
        * When combined with visibility groups, access codes items are updated appropriately based on a user's visibility group settings.
    * Maximum uses (total and per customer) can be specified.
    * Low/High pricing has been updated to take into account the requirement for access codes.
    * Access codes have been added to sales reports, to allow the specific codes that were used, to be revealed.

- Added a quick-print option to the web-based box office mode upon completion of a sale
- Phase one of the season ticket roadmap has been launched with the option to setup season tickets for pre-season. This is in request-only BETA mode until phase two is launched in the upcoming release.


### The Charity Package
- Introduced charities and donations into the checkout process. Organisers can setup one or many charities within their events and configure them to accept fixed-increment or user-specified donation amounts as well as several other donation-specific settings such as min/max price, charity website URL, charity logo etc.
- Implemented GiftAid collection and reporting which can be optionally enabled per charity and the giftaid rate can be configured at the account-level.
- Added a new "Donations Received" report alongside lots of new fields within existing reports for the new charity features
- Added fundraising support via a JustGiving integration:
  - Customers who have purchased tickets to an event can create & manage a fundraising page in JustGiving via the My Account section
  - The default settings for the generated JustGiving pages can be configured per-event



## ✨ Enhancements
* Add "External ID" on sale items/items, to allow for tracking of external identifiers (such as SKUs, or reporting IDs)
* Add: Mandatory Title/Name/Address collection when enabling charity donations
* Add: Mandatory Title/Name/Address collection when enabling fundraising
- We now load availability upfront in order to display which areas are totally sold out in large venue seating plans

## 🤝 Integrations
- 

## 📱 Mobile Apps
- 

## 🧹 Housekeeping
* Fix: When part way through a form wizard (i.e. event creation), if users changed companies in another tab, the original form wizard could still be submitted with objects that weren't owned by the new company (i.e. venues)
* Fix: Inclusive discount code dates were setting the time element to midnight, meaning discount codes were expiring 23 hours and 59 minutes early
* Fix: Copying events was not properly copying the price band IDs for a seating plan.
* Fix: Seating plan availability not always being displayed properly on the seating plan, with customers facing "seat unavailable" messages if they then tried to add the seats.


## 💻 Technical
* Refactored: Bulk Event Copying + Bulk Timeslot Creation Experience
    * As with the seating plan changes, the copy event + bulk timeslot processes were refined in order to utilise the same batching process as with seating plans.
* Refactored: Seating Plan Import Experience
    * Seating plan importing is now batched into smaller tasks, allowing larger plans to be imported more reliably.
    * Doing this also means that other customers/clients aren't impacted whilst we wait for a large plan to import.
    * The UI has been updated to show the progress so that the spinner has more context than 'please wait'.
* Add: A delta availability payload on seating planned events, in the shop.
    * This allows a much smaller amount of data to be downloaded, to keep seating plan availability up-to-date, by passing a 'last updated' timestamp and receiving a delta payload of any changes since then.
* Refactored: Availability information for seating plans, to be more performant - especially on larger seating plans.






<style>
  header, footer { display: none; }
  section { width: 100% }
</style>
