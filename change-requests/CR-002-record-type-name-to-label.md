# CR-002 Record Type Name to Label

## Status
Delivered Version 1.10

## Request Date 
2026-06-09

## Requested By
Kindra Dopp / America's Warrior Partnership

## Owner
William Galinat / WarriorServe

## Summary
Several automation processes reference the field RecordTypeNameAuto__c. The field currently stores the Record Type Label rather than the Record Type API Name, which can create confusion for administrators when building or troubleshooting automation.

## Business Reason
Improve administrator usability and reduce configuration errors caused by misunderstanding the field's purpose.

## Current Behavior
The field name and label indicate that the field contains the Record Type Name. However, the value stored is the Record Type Label.

## Requested Behavior
Update the field label, help text, and related documentation to clearly indicate that the field contains the Record Type Label.

## Impacted Areas
- Case - WarriorSrv__RecordTypeNameAuto__c
- Contact - WarriorSrv__RecordTypeNameAuto__c