# de.systopia.fastactivity
CiviCRM Extension for high performance activity features

## Current status

Currently this extension implements a "FastActivity" tab which uses an entirely new BAO class (CRM_Fastactivity_BAO_Activity) to query the database.
This is implemented in the "standard" CiviCRM format with a separate whereClause function which is not present in the original CRM_Activity_BAO_Activity class.  This should allow for easy implementation of extended filtering in the future.

## Configuration
Settings such as which columns to display can be configured under __Administer->Customize Data and Screens->Fast Activities Tab__

## Features
- A new filter is provided on the contact activities tab which uses a multi-select to allow filtering on multiple activity types.
- An add/remove filter is added on edit activity for "With Contact" when > 20 to allow editing this field on large records.
- A new filter is provided on the contact activities tab which uses a multi-select to allow filtering on campaigns and their sub-campaigns.
- Some columns can be shown/hidden by configuring settings.
- Case activities can optionally be shown.

## Requirements
- Requires campaign extension (for campaigntree API) to search for activities of child campaigns in contact activity tab.
- Requires fontawesome extension for displaying icons (for various icons / engagement level): https://github.com/mattwire/uk.co.mjwconsult.fontawesome
