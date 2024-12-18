# Ada Exception Handling Bug
This example demonstrates a potential issue with using a broad `others` exception handler in Ada, which can make it harder to debug unexpected issues within loops. The code intends to populate and print an array, but the `others` handler catches any exceptions without providing specific details.

## Problem
The problem lies in the over-reliance on a catch-all `others` exception handler.  If any error occurs within the loops (e.g., an attempt to access an array element outside its bounds, though this specific example doesn't contain such an error), it would be silently handled without any informative message, making debugging more difficult.

## Solution
The provided solution demonstrates more specific exception handling to pinpoint the issue. It shows how to address such problems by refining error handling.
