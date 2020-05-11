
# Timesheets
The timesheet resource allows you to retrieve a daily timesheet and a weekly timesheet for a user on your account.

## Endpoints
* [Retrieve a daily timesheet](#retrieve-a-daily-timesheet)
* [Retrieve a weekly timesheet](#retrieve-a-weekly-timesheet)

## Retrieve a daily timesheet
Retrieves a single days timesheet. 

`GET /v1/timesheets/daily`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/timesheets/daily?userid=501&date=2020-04-05"`

### Parameters
##### * = Required
* `* userid` - The unique identifier for the user.
* `* date` - The date of the timesheet to return. Format is yyyy-mm-dd.

### Returns
Returns a timesheet object for a specific day.

-------------

## Retrieve a weekly timesheet
Returns a full week (7 days) of timesheet data.

`GET /v1/timesheets/weekly`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/timesheets/weekly?userid=501&date=2020-04-05"`

### Parameters
##### * = Required
* `* userid` - The unique identifier for the user.
* `* date` - The date of the timesheet to return. Format is yyyy-mm-dd.

### Returns
Returns an array of timesheet objects for a specific week.

-------------

### The timesheet week object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| startDate   | The first day of the timesheet's week.  |
| endDate       | The last day of the timesheet's week.  |
| totalHours    | The total hours entered for the week on the timesheet. |
| status       | The overall status of the week's timesheet. |
| days      | An array of timesheet day objects.  |
| comments        | An array of the timesheet's weekly comments.  |

### The timesheet day object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| specificDate   | The date of a particular day on the timesheet.  |
| totalHours       | The total hours for a particular day on the timesheet.  |
| status       | The status of a particular day on the timesheet.  |
| tasks      | An array of timesheet task objects associated to a particular day on the timesheet.  |
| clockInOut        | An array of clock objects associated to a particular day on the timesheet.  |

## The timesheet task object attributes:
| Attribute  | Description   |
| ---------- | ------------- |
| hrsWorkedId    | The unique identifier of the timesheet entry.  |
| specificDate   | The date associated with the timesheet entry.  |
| projectName  | The name of the project associated with the timesheet entry.  |
| projectTaskId    | The unique identifier of the task associated with the timesheet entry. |
| longDesc    | The name of the task associated with the timesheet entry. |
| shortDesc    | The name of the task code associated with the timesheet entry. |
| hours    | The hours associated with the timesheet entry. |
| comment    | The comment associated with the timesheet entry. |
| isApproved    | Flag indicating if the timesheet entry was approved. 1 = approved, 0 = not approved |

## The timesheet clock object attributes:
| Attribute  | Description   |
| ---------- | ------------- |
| clockInOutId    | The unique identifier of the clock in and out activity. |
| specificDate   | The date of a particular day on the timesheet. |
| projectName  | The name of the project associated with the clock's activity. |
| longDesc    | The name of the task associated with the clock's activity. |
| shortDesc    | The name of the task code associated with the clock's activity. |
| projectTaskId    | The unique identifier of the task associated with the clock's activity. |
| clockIn    | The clock in time stamp for the clock's activity. |
| clockOut    | The clock out time stamp for the clock's activity. |
| clockInFormatted    | The clock in time stamp for the clock's activity formatted based on the user's preference. |
| clockOutFormatted    | The clock out time stamp for the clock's activity formatted based on the user's preference. |
| sumHours    | The total hours for the clock in and out period. |

-------------

##### Example JSON Response
```json
{
    "startDate": "2020-04-27",
    "endDate": "2020-05-03",
    "totalHours": "8.00",
    "status": "Not Submitted",
    "days": [
        {
            "specificDate": "2020-04-27",
            "totalHours": "0.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180607",
                    "specificDate": "2020-04-27",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "0.00",
                    "comment": null,
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        },
        {
            "specificDate": "2020-04-28",
            "totalHours": "0.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180608",
                    "specificDate": "2020-04-28",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "0.00",
                    "comment": null,
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        },
        {
            "specificDate": "2020-04-29",
            "totalHours": "8.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180609",
                    "specificDate": "2020-04-29",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "8.00",
                    "comment": "what is good",
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        },
        {
            "specificDate": "2020-04-30",
            "totalHours": "0.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180610",
                    "specificDate": "2020-04-30",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "0.00",
                    "comment": null,
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        },
        {
            "specificDate": "2020-05-01",
            "totalHours": "0.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180611",
                    "specificDate": "2020-05-01",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "0.00",
                    "comment": null,
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        },
        {
            "specificDate": "2020-05-02",
            "totalHours": "0.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180612",
                    "specificDate": "2020-05-02",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "0.00",
                    "comment": null,
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        },
        {
            "specificDate": "2020-05-03",
            "totalHours": "0.00",
            "status": "Not Submitted",
            "tasks": [
                {
                    "hrsWorkedId": "46180613",
                    "specificDate": "2020-05-03",
                    "projectName": "Chanel",
                    "projectTaskId": "841428",
                    "longDesc": "Fetty",
                    "shortDesc": null,
                    "hours": "0.00",
                    "comment": null,
                    "isApproved": "0"
                }
            ],
            "clockInOut": {
                "clockactions": []
            }
        }
    ],
    "comments": []
}```
