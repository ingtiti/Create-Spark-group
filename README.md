These two codes are used to create a Spark group from a TXT file with email addresses

NOTES:
  Does not check emails duplicates
  It create an emails.txt file and is OVERWRITED any time the code is running
  You need to log in developers.ciscospark.com to get your id token
  
extract_emails_from_text.py
  The code ask for a TXT file located in the same directory, compare line by line to identify email format texting.
  Every email address will be restored in a emails.txt file and located in the same directory
  When save address each one end with "\n" tag to break the line
  
new_spark.py
  Use the emails.txt file from extract_emails_from_text.py
  The addresses are restored on a list named member_list
  REMEMBER each email address finish it with "\n" and needs to be deleted to use on the "personEmail" JSON index on Spark API
  To delete it I use 'e[:-2]' in thi way the last 2 characteres will be skipped.
  For each email the script returns the JSON response, DON'T BE SCARE on the messages
  
Have a nice coding
