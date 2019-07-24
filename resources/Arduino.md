# 🔌 Arduino resource

All the Arduino projects from the [projects hub](https://arduino.becauseofprog.fr) are in this endpoint.

**Warning : this service isn't online yet !**

### Arduino project object

| Field         | Type                               | Description                        | Can be null ? |
| ------------- | ---------------------------------- | ---------------------------------- | ------------- |
| url           | string                             | project's URL                      |               |
| author        | [user object](User.md#user-object) | project's author                   |               |
| name          | string                             | project's name                     |               |
| summary       | string                             | project's summary                  |               |
| illustration  | string                             | picture to illustrate project      | ✅            |
| video         | string                             | video to illustrate project        | ✅            |
| link          | string                             | link to further informations       | ✅            |
| description   | string                             | project's description              | ✅            |
| timestamp     | integer                            | unix timestamp, project's creation |               |
| is_from_staff | boolean                            | if the project is from the staff   |               |
| is_featured   | boolean                            | if the project is featured         |               |

## Get all projects

`GET /arduino-projects`

Get all the projects. Returns a `data` list with [arduino project objects](#arduino-project-object) inside.

## Create project

`POST /arduino-projects`

Create a new Arduino project. Requires auth.

### Required data

| Field   | Type   | Description       |
| ------- | ------ | ----------------- |
| url     | string | project's URL     |
| name    | string | project's name    |
| summary | string | project's summary |

### Optional data

| Field        | Type   | Description                   |
| ------------ | ------ | ----------------------------- |
| illustration | string | picture to illustrate project |
| video        | string | video to illustrate project   |
| link         | string | link to further informations  |
| description  | string | project's description         |

## Get project

`GET /arduino-projects/{arduino-project.url}`

Get one project by its URL. Returns a [arduino project object](#arduino-project-object) called `data`.

## Edit project

`PATCH /arduino-projects/{arduino-project.url}`

Edit a prokect. Requires auth and to be the project's author.

**Editable fields :** `name`, `summary`, `illustration`, `video`, `link`, `description`.

## Delete project

`DELETE /arduino-projects/{arduino-project.url}`

Delete a project. Requires auth and to be the project's author.
