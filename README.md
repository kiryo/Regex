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

# (^|^a-öA-Ö0-9])        Beginning of line or NOT number or letters. This means that no numbers or letters can be attached in beginning. 
# [0-9]{6}              6 numbers
# (-|A)                 Line or A
# [0-9]{3}              3 numbers
# ([A-Z]|[a-z]|[0-9])   Letter or number
# ($|[^a-öA-Ö0-9])      End of line or NOT number or letter. Same as in beginning
