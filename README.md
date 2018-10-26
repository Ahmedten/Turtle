# Turtle

import urllib
def read_text():
    file = open("D:\Mine\Python Material\Studied apps\quotes.txt")
    contents = file.read()
    file.close()
    profanity_check(contents)

def profanity_check(text_to_check):
    connection = urllib.urlopen("http://www.wdylike.appspot.com/?q="+text_to_check)
    output = connection.read()
    print output
    connection.close()
read_text()
