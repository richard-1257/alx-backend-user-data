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
+ [x] 0. **Regex-ing**
  + [filtered_logger.py](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/filtered_logger.py) contains a function called `filter_datum` that returns the log message obfuscated with the following requirements:
    + Arguments:
      + `fields`: a list of strings representing all fields to obfuscate.
      + `redaction`: a string representing by what the field will be obfuscated.
      + `message`: a string representing the log line.
      + `separator`: a string representing by which character is separating all fields in the log line (`message`).
    + The function should use a regex to replace occurrences of certain field values.
    + `filter_datum` should be less than 5 lines long and use `re.sub` to perform the substitution with a single regex.
   
+ [x] 1. **Log formatter**
  + [filtered_logger.py](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/filtered_logger.py) contains the following updates:
    + Copy the following code into [filtered_logger.py]([filtered_logger.py](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/filtered_logger.py)):
    ```python
    import logging


    class RedactingFormatter(logging.Formatter):
    """ Redacting Formatter class
    """

    REDACTION = "***"
    FORMAT = "[HOLBERTON] %(name)s %(levelname)s %(asctime)-15s: %(message)s"
    SEPARATOR = ";"

    def __init__(self):
        super(RedactingFormatter, self).__init__(self.FORMAT)

    def format(self, record: logging.LogRecord) -> str:
        raise NotImplementedError
    ```
    + Update the class to accept a list of strings `fields` constructor argument.
    + Implement the `format` method to filter values in incoming log records using `filter_datum`. Values for fields in `fields` should be filtered.
    + DO NOT extrapolate `FORMAT` manually. The `format` method should be less than 5 lines long.

+ [x] 2. **Create logger**</br>
   [filtered_logger.py](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/filtered_logger.py)  contains:
    + Use [user_data.csv](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/user_data.csv) for this task.
    + Implement a `get_logger` function that takes no arguments and returns a `logging.Logger` object.
    + The logger should be named `"user_data"` and only log up to `logging.INFO` level. It should not propagate messages to other loggers. It should have a `StreamHandler` with `RedactingFormatter` as formatter.
    + Create a tuple `PII_FIELDS` constant at the root of the module containing the fields from [user_data.csv](https://github.com/richard-1257/alx-backend-user-data/blob/master/0x00-personal_data/user_data.csv) that are considered PII. `PII_FIELDS` can contain only 5 fields - choose the right list of fields that can are considered as “important” PIIs or information that you **must hide** in your logs. Use it to parameterize the formatter.






