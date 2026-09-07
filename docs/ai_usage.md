AI Use Log
Rosalind Problem #2: Asking Gemini to Explain Code
  Tool/model & version: Gemini
  What I asked for: I asked Gemini to explain my code.
  Snippet of prompt(s): “Please explain this code.”
  What I changed before committing: I did not change anything before committing.
  How I verified correctness (tests, sample data): I did not need to verify the correctness of Gemini’s explanation because it   was only explaining what my existing code did.
Rosalind Problem #2 Continued: Asking Gemini to Solve the Problem
  Tool/model & version: Gemini
  What I asked for: I asked Gemini to solve Rosalind Problem #2. Gemini initially told me that my existing code was correct,     so I then asked it to show me how it would write the code instead.
  Snippet of prompt(s): “Can you please solve the following problem? Given: Two positive integers a and b, each less than        1000. Return: The integer corresponding to the square of the hypotenuse of the right triangle whose legs have lengths a and    b.” I then asked Gemini to show me how it would have written the code.
  What I changed before committing: I did not change anything before committing because my code and Gemini’s code produced the   same result.
  How I verified correctness (tests, sample data): I tested the code using Rosalind’s sample dataset, a = 3 and b = 5, instead   of the numbers from my assigned dataset. The code produced the expected result of 34.
Rosalind Problem #4: Numbering Lines
  Tool/model & version: Gemini
  What I asked for: I looked up ways to number the lines in the poem. Gemini suggested using the enumerate() function.
  Snippet of prompt(s): I asked Gemini how I could number the lines in the poem.
  What I changed before committing: I added the enumerate() function to my code.
  How I verified correctness (tests, sample data): I ran the code and checked that the output numbered the lines correctly       using the practice data set.
Rosalind Problem #5: Dictionary Error
  Tool/model & version: Gemini
  What I asked for: I asked Gemini to explain the “set not being callable” error in my code.
  Snippet of prompt(s): “Explain the ‘set not being callable’ error in my code.” Gemini explained that Dictionary_1 =            {"Practice_5.txt"} creates a set rather than a dictionary because curly braces without key-value pairs create a set.
  What I changed before committing: I accepted the change that allowed the code to count the words and form a dictionary         instead of creating a set.
  How I verified correctness (tests, sample data): I tested the corrected code using the downloaded practice dataset. I then     downloaded a new dataset and ran the code again to make sure it worked with different data.
Biopython Installation Test
  Tool/model & version: Gemini
  What I asked for: I asked Gemini to give me a brief test to make sure Biopython was installed correctly.
  Snippet of prompt(s): “Give me a brief test to be sure Biopython is installed correctly.”
  What I changed before committing: I accepted and ran the suggested code to test the Biopython installation.
  How I verified correctness (tests, sample data): I ran the code and confirmed that the Biopython module imported               successfully without producing an error.
Rosalind Problem #7: AttributeError
  Tool/model & version: Gemini
  What I asked for: I asked Gemini to explain the AttributeError I received when trying to use .transcribe().
  Snippet of prompt(s): I asked Gemini to explain the error: AttributeError: 'builtin_function_or_method' object has no          attribute 'transcribe'. Gemini explained that my_sequence had been assigned a method object instead of a Bio.Seq object and    that .transcribe() needs to be called on a properly created Bio.Seq object.
  What I changed before committing: I accepted and ran Gemini’s changes, which added the necessary variables and properly        defined my_sequence as a Bio.Seq object before calling .transcribe().
  How I verified correctness (tests, sample data): I used the practice dataset to verify that Gemini’s solution produced the     correct RNA transcription.
