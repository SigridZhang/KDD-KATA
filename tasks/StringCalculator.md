Description:

String Calculator Kata (via Roy Osherove)

    1. Create a simple String calculator with a method int Add(string numbers). The method can take 0, 1 or 2 numbers, and will return their sum (for an empty string it will return 0). For example "" or "1" or "1,2"
       - Start with the simplest test case of an empty string and move to 1 and two numbers
       - Remember to solve things as simply as possible so that you force yourself to write tests you did not think about
       - Remember to refactor after each passing test
    2. Allow the Add method to handle an unknown amount of numbers
    3. Allow the Add method to handle new lines between numbers (instead of commas).
       - the following input is ok: "1\n2,3" (will equal 6)
       - the following input is NOT ok: "1,\n" (not need to prove it - just clarifying)
    4. Support different delimiters. To change a delimiter, the beginning of the string will contain a separate line that looks like this: [delimiter]\n[numbers...], for example ;\n1;2 should return three where the default delimiter is ; .
       - the first line is optional. all existing scenarios should still be supported
    5. Calling Add with a negative number will throw an exception "negatives not allowed" - and the negative that was passed.
       - if there are multiple negatives, show all of them in the exception message
    6. Numbers bigger than 1000 should be ignored, so adding 2 + 1001 = 2
    7. Delimiters can be of any length with the following format: “//[delimiter]\n” for example: “//[]\n12***3” should return 6
    8. Allow multiple delimiters like this: “//[delim1][delim2]\n” for example “//[][%]\n12%3” should return 6.
    9. make sure you can also handle multiple delimiters with length longer than one charTasks:
    1. empty string
        - input null, return 0
        - input "", return 0
    2. 1 numbers
        - input "1", return 1
        - input "0", return 0
    3. 2 numbers
        - input "0,1", return 1
        - input "1,2", return 3
    4. more than 2 numbers
        - input "0,1,2", return 3
        - input "10,20,30", return 60
    5. numbers split by new lines
        - input "1\n2", return 3
        - input "1\n2\n3", return 6
    6. numbers split by new lines and ,
        - input "1\n2,3", return 6
        - input "1,2\n3", return 6
    7. numbers split by delimiters users specify
        - input ";\n1;2", return 3
    8. throw exception message when there is one numbers or more
        - input "1,-2,3", return "negatives not allowed - -2"
        - input "-1,2,-3", return "negatives not allowed - -1,-3"
    9. ignore numbers which are bigger than 1000
        - input "1001,1", return 1
        - input "1000,1", return 1001
        - input "1001,1,2", return 3
    10. delimiters specified by users of any length with format: "//[delimiter]\n"
        - input "//[***]\n1***2", return 3
        - input "//[***]\n1***2***3", return 6
    11. multiple delimiters with format: " //[delim1][delim2]\n" 
        - input "//[*][%]\n1*2", return 3
        - input "//[*][%]\n1*2%3", return 6
    12. multiple delimiters with length longer than one char
        - input "//[**][%%%]\n1**2", return 3 
        - input "//[**][%%%]\n1**2%%%3", return 6     
    

  
  


