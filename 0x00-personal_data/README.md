![personal data](https://github.com/richard-1257/alx-backend-user-data/assets/83041703/95df1eab-e85d-4962-8fd7-d3e72540eac8)

# Personal data
This project contains tasks for learning to protect a user's personal data.
`Back-end` `Authentification`

 - By: Emmanuel Turlay, Staff Software Engineer at Cruise

## Resources
- [What Is PII, non-PII, and Personal Data?](https://piwik.pro/blog/what-is-pii-personal-data/)
- [logging documentation](https://docs.python.org/3/library/logging.html)
- [bcrypt package](https://github.com/pyca/bcrypt/)
- [Logging to Files, Setting Levels, and Formatting](https://www.youtube.com/watch?v=-ARI4Cz-awo)

## Learning Objectives
- Examples of Personally Identifiable Information (PII)
- How to implement a log filter that will obfuscate PII fields
- How to encrypt a password and check the validity of an input password
- How to authenticate to a database using environment variables

## Tasks To Complete
+ [x] 1. **Regex-ing**
  + [filtered_logger.py](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/filtered_logger.py) contains a function called `filter_datum` that returns the log message obfuscated with the following requirements:
    + Arguments:
      + `fields`: a list of strings representing all fields to obfuscate.
      + `redaction`: a string representing by what the field will be obfuscated.
      + `message`: a string representing the log line.
      + `separator`: a string representing by which character is separating all fields in the log line (`message`).
    + The function should use a regex to replace occurrences of certain field values.
    + `filter_datum` should be less than 5 lines long and use `re.sub` to perform the substitution with a single regex.




