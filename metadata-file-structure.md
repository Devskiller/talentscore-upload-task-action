# Metadata file structure
The file stores programming task details in the form of YAML key-value pairs, with the following fields:

- **uuid**: ID of the task. With it you will be able to update tasks. You can use the existing one or generate an unique value using [generators](https://www.uuidgenerator.net/)
- **title**: title of a task
- **question**:  question which will be presented to the candidate
- **type**: `PROGRAMMING` or `CODE_REVIEW` 
- **difficulty**: difficulty level, one of `EASY`, `MEDIUM`, `HARD`
- **tags**: task tags, ie. what kind of knowledge this questions tests
- **points**: default number of points for this task
- **duration**: default time duration in the ISO 8601 duration format  
- **projectType**: technology associated with the task, e.g.: `CMAKE`, `NODEJS`, `MAVEN`
- **projectTypeVersion**: specific version of the technology, e.g.: `NODEJS16`, `GCC11`

## Example

```yaml
uuid: aee4ae94-5709-4917-8dde-fa54b91f84cf
title: Java | Sample Calculator task
question: |-
  Your task is to create a simple calculator capable of adding, subtracting, multiplying and dividing two numbers.
type: PROGRAMMING
difficulty: EASY
tags: ['C++', 'Basics']
points: 20
duration: PT1H
projectType: CMAKE
projectTypeVersion: GCC11
```