Important note: This version/branch of the app is deprecated and will no longer be supported.

# TA-bugcrowd

A Splunk® add-on providing a modular input for cyclically retrieving submissions from your Bugcrowd programs, creating a Splunk event for each new or updated submission.

Created using the Splunk Add-On builder.

Tested on Splunk Enterprise 7.1.3.

## Installation

Just unpack to $SPLUNK_HOME/etc/apps and restart your Splunk instance. Choose between search heads, indexers and heavy forwarders in distributed environments.

## Requirements

You'll need to provide a valid API key (HTTP Authorization Header token) to your Bugcrowd program(s) when setting up inputs.

Your Splunk instance requires acess to the internet (via a proxy) to query https://api.bugcrowd.com.

## TODO / Known Issues

api.bugcrowd.com does currently not return the timestamps of submissions' state transitions. Thus the add-on will set transition events' timestamps to the observed transition time, which is up to _input schedule_ seconds later than the actual state transition. Will work with Bugcrowd to enhance the API to return the necessary information.

Add Bugcrowd logo after consent.

Potentially add showcase dashboard.

Add open source license.

## History

### v1.1.1

- Added "dest" field extraction

- Fixed timestamp recognition

### v1.1.0

- Added mapping to CIM "Vulnerabilities" data model as good as possible

- Changed default visibility to true

- Renamed "source" key to "submission_source" as it was causing conflicts with Splunk's source field

