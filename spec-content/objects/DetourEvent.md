# DetourEvent Object
The `DetourEvent` object contains information that describes where, when, and what activity are taking place in a detour, along a road segment.

## Properties
Name | Type | Description | Conformance | Notes
--- | --- | --- | --- | ---
`road_event` | [RoadEvent](/spec-content/enumerated-types/RoadEvent.md) | Describes the basic characterisitics of a Road Event.  | Required |
`start_date` | String; [date-time](https://tools.ietf.org/html/draft-handrews-json-schema-validation-01#section-7.3.1) | The UTC time and date when the event begins. | Required | All datetime formats shall follow [RFC 3339 Section 5.6](https://tools.ietf.org/html/rfc3339#section-5.6). Example: `2016-11-03T19:37:00Z`.
`end_date` | String; [date-time](https://tools.ietf.org/html/draft-handrews-json-schema-validation-01#section-7.3.1) | The UTC time and date when the event ends. | Required | All datetime formats shall follow [RFC 3339 Section 5.6](https://tools.ietf.org/html/rfc3339#section-5.6). Example: `2016-11-03T19:37:00Z`.
`start_date_accuracy` | [TimeVerification](/spec-content/enumerated-types/TimeVerification.md) | A measure of how accurate the start Date Time is. | Required |
`end_date_accuracy` | [TimeVerification](/spec-content/enumerated-types/TimeVerification.md) | A measure of how accurate the end Date Time is. | Required | 
`beginning_cross_street` | String | Name or number of the nearest cross street along the roadway where the event begins. | Optional |
`ending_cross_street` | String | Name or number of the nearest cross street along the roadway where the event ends. | Optional |
`beginning_milepost` | Number | The linear distance measured against a milepost marker along a roadway where the event begins. | Optional | A milepost or mile marker is a surveyed distance posted along a roadway measuring the length (in miles or tenth of a mile) from the south west to the north east. These markers are typically notated on State and local government digital road networks. See also the `lrs_type` property on the [RoadEventDataSource](/spec-content/objects/RoadEventDataSource.md) object.
`ending_milepost` | Number | The linear distance measured against a milepost marker along a roadway where the event ends. | Optional | A milepost or mile marker is a surveyed distance posted along a roadway measuring the length (in miles or tenth of a mile) from the south west to the north east. These markers are typically notated on State and local government digital road networks. See also the `lrs_type` property on the [RoadEventDataSource](/spec-content/objects/RoadEventDataSource.md) object.
`event_status` | [EventStatus](/spec-content/enumerated-types/EventStatus.md) | The status of the event. | Optional |

## Used By
Property | Object
--- | ---
`properties` | [RoadEventFeature](/spec-content/objects/RoadEventFeature.md)

## Important Notes
None
