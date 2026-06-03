# deloitee-intern
# Deloitte Telemetry Data Conversion Challenge

## Overview

This project converts two different telemetry data formats into a unified output format.

## Implemented Functions

### convertFromFormat1(jsonObject)

Converts telemetry data from Format 1 to the unified format by directly mapping the fields.

### convertFromFormat2(jsonObject)

Converts telemetry data from Format 2 to the unified format by:

* Extracting device information from nested objects.
* Combining location fields into a single location string.
* Converting ISO 8601 timestamps into milliseconds since Unix epoch.
* Mapping status and temperature fields to the unified schema.

## Output Format

```json
{
  "deviceID": "...",
  "deviceType": "...",
  "timestamp": 0,
  "location": "...",
  "operationStatus": "...",
  "temp": 0
}
```

## How to Run

```bash
python main.py
```

## Notes

* Both input formats are converted to the same unified structure.
* Timestamp conversion is handled using Python's datetime module.
* The implementation passes all provided unit tests.
*
