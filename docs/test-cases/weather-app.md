# Weather App – Temperature Unit Toggle

## Type
Functional Test

## Priority
High

## Severity
Medium

## Description
Testing temperature conversion between Celsius and Fahrenheit in a weather application.

## Bug Found
When switching from Celsius to Fahrenheit:
- The temperature value changes correctly
- The unit label (°C / °F) does NOT update
- Max, min, and "feels like" values remain in Celsius

## Steps to Reproduce
1. Open the weather app
2. Click on "F"
3. Observe the temperature value updates
4. Notice:
   - Unit label still shows "°C"
   - Max, min, and feels like values do not change

## Expected Result
- Temperature value updates correctly
- Unit label updates (°C → °F)
- Max, min, and feels like values convert to Fahrenheit

## Actual Result
Only the main temperature updates, while the unit label and other temperature values remain unchanged.

## Root Cause
The application only updated the main temperature value.  
The unit label and other related values (max, min, feels like) were not included in the conversion logic.

## Solution
Updated the application to:
- Track the current unit (Celsius/Fahrenheit)
- Update the unit label dynamically
- Convert max, min, and feels like values along with the main temperature

## Status
✅ Fixed
