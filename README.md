# Regex
# Regular Expression
# 
# This expression is for scanning finnish social security numbers.
# Use for this is example in companies that can warn users not to store these numbers in computers or networkdrives.
# 
# This expression is different. What makes it special it can find social security numbers between words but excludes match if these is number or letter
# in beginning or end. If there is symbol or space insted its a match.

# Expression can be used in various ways. Example powershell or from File Server Resource Manager.


# Expression explaned:
# (^|[^a-öA-Ö0-9-])[0-9]{2}[0-1]{1}[0-9]{3}(-|A)[0-9]{3}([A-Z]|[a-z]|[0-9])([^a-öA-Ö0-9-])
#
# (^|[^a-öA-Ö0-9-])     Beginning of line can't contain numbers, letters or line. This means that no numbers or letters can be attached in beginning. 
# [0-9]{2}              2 numbers
# [0-1]{1}              1 Number (first number of month can only be 1 or 0)
# [0-9]{3}              3 Numers, second number of month and 2 numbers of year
# (-|A)                 Line or A
# [0-9]{3}              3 numbers
# ([A-Z]|[a-z]|[0-9])   Letter or number
# ($|[^a-öA-Ö0-9-])      Same as in beginning. Can't contain numbers, letters or line
