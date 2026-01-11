# Report

1. In C, do you use printf or print? printf

2. What operating system do you use? Mac OS

3. Explain the `-Wall` option for your C compiler. Putting -Wall in the compiler enables warning messages that helps the coder know why their code isn't compiling.

    3a. Copy and paste the `SYNOPSIS` section from the gcc manual page (Hint: what is the linux command to get this?). Make sure to use a preformatted text block below

        ```
        SYNOPSIS
       clang [options] filename ...
        ```

4. How would you list all files in a directory using the long format, but exclude the `.`. and `..` file?

    ```console
    $ ls -l
    ```

5. Complete the table below based on linux permission sets for files.

    | Permission | Owner              | Group        | World        | Directory? |
    |------------|--------------------|--------------|--------------|------------|
    | -rw-r--r-- | read,write         | read         | read         | no         |
    | -rwx------ | read,write,execute | none         | none         | no         |
    | -r--r--r-- | read               | read         | read         | no         |
    | drwxr-xr-x | read,write,execute | read,execute | read,execute | yes        |
    | -rw-rw---- | read,write         | read,write   | none         | no         |
    | drx--x--x  | read,execute       | execute      | execute      | yes        |

6. Permissions for files are often set by binary values. For example 111 is read, write, execute. When all of them are converted and put together, that is an octal. For example: `700` is `rwx------` or `644` is `rw-r--r--` (common for web pages).
   Convert the following numeric representation to permissions.

   | Octal | Binary    | Permission |
   |  ---  |-----------|------------|
   |  700  | 111000000 | rwx------  |
   |  644  | 110100100 | rw-r--r--  |
   |  444  | 100100100 | r--r--r--  |
   |  622  | 110010010 | rw--w--w-  |
   |  660  | 110110000 | rw-rw----  |
   |  770  | 111111000 | rwx-rwx--- |
   |  111  | 001001001 | --x--x--x  |

> While we rarely will deal with permissions in this course, the above was to help you practice thinking about how to represent information.

7. Pick three linux commands. List them below using bullets (inset under this number). In your own words describe what each command does.

   * *example:* `ls` - lists directory contents
   * 'cd' - changes directory by itself will bring you back to the main directory cd [directory name] will bring you into a nested directory
   * 'mkdir' - makes a new director 
   * 'rmdir' - removes directory

8. Fix the following C code. You are free to write a small program to help figure it out.

    ```c
    int input;
    scanf("%d", &input);
    printf("The answer to the question is: %d\n", input);
    ```

9. In line two of the three C code lines above, what is being passed into scanf? Is it the value or is it the address of a memory location?
    Memory location

10. Thinking back to CS 5001 - you should have briefly covered a linear and binary search algorithms, if you didn't cover them, that is fine!
    
      10a. In your own words describe a linear search algorithm.

      Linear searching is starting from the first value and moving one by one through the list od data to find what your looking for

      10b. In your own words describe a binary search algorithm

      Binary search take a sorted list of data and breaks the list in half. It asks whether the item is in the first or later half, it then goes to that half and breaks it in half again repeating the process until the answer is found

      10c. Which one is faster? And is it situational?
      Binary is faster, but it requires the list to be sorted ahead of time
    
> [!IMPORTANT]
  > Whether you covered them or not, I would like you to look up at least two (2) references for them online, and include them in your answer for question 10 using in-text citations.
  
> **Example of in-text citations:**
  > 
  > Strings in C are sequences of characters stored in an array structure, ended by the null terminator [1]. In order to use them, most systems provide access to <string.h> to provide functions such as `strlen()` and `strcpy()` [2].


## References

GeeksforGeeks. 2025. Binary Search.(Dec. 27, 2025). Retrieved January 11, 2026 <https://www.geeksforgeeks.org/dsa/binary-search/>

W3Schools. DSA Binary Search. Retrived January 11, 2026 <https://www.w3schools.com/dsa/dsa_algo_binarysearch.php>

>[!TIP]
   > if you are unsure how to format something in ACM, this is a good case of using [claude](https://claude.northeastern.edu/) or other LLM - you can paste it in and ask it to format the link into ACM format. If you can't find all the info, we won't hold you to strict formatting, just a proper attempt.

[1] GeeksforGeeks. 2025. Strings in C. (January 10, 2025). Retrieved April 5, 2025 from <https://www.geeksforgeeks.org/strings-in-c/>

[2] GeeksforGeeks. 2025. C String Functions. (January 17, 2025). Retrieved April 5, 2025 from <https://www.geeksforgeeks.org/string-functions-in-c/>

[3] Insert citation here

[4] Insert citation here
