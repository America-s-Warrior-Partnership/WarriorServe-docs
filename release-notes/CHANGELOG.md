# Change Log

All notable changes to WarriorServe will be documented in this file.

This project follows:
- Semantic-ish versioning if applicable
- Categories such as Added, Changed, Fixed, Removed, Security

## [Beacon 1.91] - 2026-06-10
### Changed
- Case.WarriorSrv__RecordTypeNameAuto__c label from `Record Type Name` to `Record Type Label`
- Contact.WarriorSrv__RecordTypeNameAuto__c label from `Record Type Name` to `Record Type Label`

## [Beacon 1.9] - 2026-04-20
### Added
- Added async prevention from calling in ContactTriggerHandler to prevent limits issues
### Changed
- VeteranConfirmationStatus_Queuable from manually setting ContactTriggerHandler to skip calling from queueable
### Fixed
- None
### Removed
- None

### Request
- [CR-001 Contact Trigger Prevent Queue From Async](../change-requests/CR-001-contact-trigger-prevent-queue-from-async.md)
- [CR-002 Record Type Name to Label](../change-requests/CR-002-record-type-name-to-label.md)