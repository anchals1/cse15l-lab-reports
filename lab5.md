# Anchal Saraswat CSE 15L Lab Report 5

## Part 1: Student Piazza Post


**Student Post:**

List Reverse Method:
IMAGE

Test Output:
IMAGE

Hello, 

I need help with errors I am running into when I try to test the reverseInPlace method that is meant to reverse an array in place. With the orginal code I get the error 
shown above when I run the Java file with JUnit. According to the error, the actual value of the second index of the reversed array we got was 9 but the expected value
was 7 so this is returning the wrong result. According to me, the issue could lie in the fact that the last digit of both the original and sorted arrays is the same so 
to me this would mean that the arrays are not being sorted properly and the failure inducing input for this method would be an array that has a length that is greater 
than one since I think the error is that the method's reusing values that have already been sorted at an index when the method is sorting in place. 

**TA Response:**

Hi, 

I think you should start exploring this with a test of the reverseInPlace method with an input array that has 2 or more values since you can manually keep track of the 
values that are being reversed in the array. I think it would also be helpful to include some print statements that will print which values are being swapped at the steps
in the loop so you can see if it's the correct value at a specific index. 

**Student Response:**

Image
Image

Thank you for the response! I decided to go with your recommendation and use print statements to see what was being replaced when the list is reversed with 7,8,and 9 as the
input. According to what was printed, it seems like everything is being correctly reversed except in the last run the code is swapping out 9 for 9 which is where the problem rises. 
The mothod's returning {9, 8, 9} but it should be {9, 8, 7} so the array is incorrectly getting sorted because it's reusing what has already been sorted."Swapping 9 for 9" means 
at the last index the method's using the first element in the sorted array which is 9, but it’s supposed to be using the first element from the original array which is 7. 

**Information About Setup:**

File and directory structure needed:
IMAGE

In the structure there's a test.sh file which contains the commands to run JUnit tests to run the ArrayTests.java file, which contains the code to test the reverseInPlace method, 
and the reverseInPlace method which is located in ArrayExamples.java.

Content of Method File before fixing bug:
Image 1

Command I ran to trigger the bug:

`bash test.sh`

test.sh contains: 
Image

How to fix bug:

I used two pointers as indices of the array, one starts at the 0th index and the other one starts at the last index, then I save the value of the left pointer in a variable and 
setting the value of left pointer to the right one which swaps the two values. Then the right pointer gets updated with the saved left value and the left pointer gets increased
by 1 and the right pointer decreases by 1 which moves the values closer to the center of the array. Eventually both the pointers reach the middle which means the array was reversed.
```
static void reverseInPlace(int[] arr) {
    int left = 0;
    int right = arr.length - 1;
    while (left < right) {
        int val = arr[left];
        arr[left] = arr[right];
        arr[right] = val;
        left++;
        right--;
    }
}
```

## Part 2: Reflection:

I gained knowledge about using vim during my lab experience in the second half of this quarter. Vim is quite helpful for debugging, and even though learning commands and becoming 
accustomed to them took some time, they were really helpful when I needed to open files on my computer but didn't have access to VSCode or other platforms. Being able to step 
through a program and debug is something I found quite amazing and am pleased I was able to learn more about. Debugging is also a skill that will always be needed in future classes 
and in the workforce as I am about to graduate.
