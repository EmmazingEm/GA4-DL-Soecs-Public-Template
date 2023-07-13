# `Insert Client Name` Data Layer Specs

## Overview
This repository contains the necessary specifications to build an Event Driven Data Layer.

## Events
Each file inside the **[events](events)** folder corresponds to a single use case or site event that needs to be implemented.

These will be used to share data with Google Tag Manager on desktop.

### SDR vs. DL Specs
Typically, you'll see that the SDR has a greater number of events when compared against this documentation. There are several reasons:
  1. GA4 automatically collects some events and the default parameters are good enough for our applications.
  2. The SDR documents the GTM and GA4 setup while this repository documents the datalayer. Some GA4 events are subsets of a single datalayer event. They are listed separately in the SDR so the analytics engineer knows to make a unique tag and trigger for it, but not in the datalayer specs because it would be redundant.

## Other Resources
[Here](https://docs.google.com/spreadsheets/d/1lH_sgRfepOMdfn0YNqHnx_PD9Y_PVBbqZ75zgTVMuSQ/edit#gid=369713555) is where you will find the current SDR template.

[Go here](https://developers.google.com/analytics/devguides/collection/ga4/reference/events?client_type=gtm) to access Google's official developer reference for recommended events. Each event's title will have a link to this reference as appropriate. Some of the events in this documentation are custom and will therefore not have a link to the developer reference.

## Questions/Comments
For any questions or comments, please contact `insert email address`.
