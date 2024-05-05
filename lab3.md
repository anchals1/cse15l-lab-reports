# Anchal Saraswat CSE 15L Lab Report 3

## Part 1 - Bugs
**Failure Inducing Input for Buggy Program:**
```
  @Test
  public void testReverseInPlace2() {
    int[] input2 = {7, 8 ,9};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{9, 8 ,7}, input2);
  }
```
  

**Non Failure Inducing Input:**

```
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
  }
```


**Method with Bug (reverseInPlace):**

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
**Output when Running JUnit test with bug in method:**

<img width="927" alt="lab3pic1" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/6dfb88eb-3324-4e3a-a368-5550e2ea3ec9">


**Corrected Code:**

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

**Output when Running JUnit test with corrected method:**

<img width="821" alt="lab3pic2" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/77a7b97d-6c0d-4338-b897-944ba33310f5">

**How I debugged:**

For the reverseInPlace method, any input array that had more than value would be a failure inducing input, so a possible failure inducing input array I tested with was {7, 8, 9} whch has 3 values. This led to errors when I ran the reverseInPlace2 test,the problem with the method is that the array doesn’t sort properly because it ends up reusing values that have already been sorted. The first error message states that 7 was expected in the 3rd element, but 9 was in that spot which is because when the method reversed the array and assigned the last value it used the first element in the almost sorted in place array which is 9 but it was supposed to use the first element from the original array which is 7. To debug this I used two pointers as indices of the array with one starting at the 0th index and the second starting at the last index. Then I swapped both these values by saving the value of the left pointer in a variable and setting the value of left pointer to the right one, then I updated the right pointer with the left value I saved.The left pointer then increased by 1 and the right pointer decreased by 1 which moved them closer to the center of the array. This loop will keep continuing until the two pointers reach the middle which will mean that the entire array has been reversed.


## Part 2 - Researching Commands

**Command:** grep

**4 Interesting Command Line Options:**
1. `-i`
2. `-r`
3. `-w`
4. `-l`


**Examples with `-i`:**

```
grep -i "six" */*/1468-6708-3-1.txt

Six large controlled population-based studies of
          examining health status over time, we added a sixth
```

<img width="672" alt="lab3pic3" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/a87e6a54-52e3-4790-a232-07d500a2ac84">


```
grep -i "heart" technical/*/1468-6708-3-10
.txt
        Prevent Heart Attack Trial (ALLHAT) is a randomized,
        Heart, Lung, and Blood Institute (NHLBI). A double-blind,
        compare the rate of fatal coronary heart disease (CHD) or
        National Heart, Lung, and Blood Institute accepted a
        outpatient], heart failure [HF/treated in the hospital or
          Heart Failure Diagnosis
          nocturnal dyspnea, dyspnea at rest, New York Heart
          either of these alone, without other indications of heart
          Heart Failure Diagnostic Criteria
        1) New York Heart Classification functional class III:
        Assessment of Patients with Diseases of the Heart: AHA
```

<img width="506" alt="lab3pic4" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/6d15e56c-a00e-4153-8d4f-84f1d66ae28d">

When grep is used with `-i`, it means grep is going to search for lines in the file/files for the given string but the case is insensitive. We can see how it is useful in the example, the string being searched for is "six" and if a line in a file has "Six" or any other variation of it with capital, that line will be a match. This is convenient since the user doesn't have to worry about including multiple variations of the string when they are searching for matching lines.


**Examples with `-r`:**
```
grep -r "nocturnal" technical/biomed
technical/biomed/1468-6708-3-10.txt:          nocturnal dyspnea, dyspnea at rest, New York Heart
technical/biomed/1471-2202-3-20.txt:          sleep-wake distribution typical for this nocturnal
technical/biomed/1471-2202-3-20.txt:        arrhythmic by lesioning of the SCN. In nocturnal roden
ts,
technical/biomed/1471-2202-3-20.txt:        nocturnal and diurnal species, 
technical/biomed/1472-6793-2-18.txt:          illustrates coordination preferences during the noct
urnal
technical/biomed/1472-6882-1-10.txt:          nocturnal and enter water when chased [ 5 ] . They are
technical/biomed/1472-6882-1-10.txt:          are nocturnal, living in hollow fallen trees during the
technical/biomed/1476-511X-1-2.txt:          not removed the night before, and since nocturnal mice
technical/biomed/rr37.txt:          or nocturnal), use of systemic corticosteroids, use of
```

<img width="713" alt="lab3pic5" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/732acd2e-6172-4c7b-8019-bf64b1cd75db">


```
grep -r "dyspnea" technical/plos  
technical/plos/pmed.0010008.txt:        bronchodilation to relieve dyspnea, antibiotics for intercurrent respiratory tract
technical/plos/pmed.0020017.txt:          physicians and manifested by lessened dyspnea and cancer-related pain. However, this
```

<img width="724" alt="lab3pic6" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/ce7bf982-4bf6-44ca-b7db-7c215f11f0d8">

When grep is used with `-r`, it means grep will search for lines in the file/files for the given string recursively. This means all the files in the directory in the argument will be searched and the files in all the subdirectories will be searched too and matching lines will be returned. In this example, the string grep is searching for is "noctural" and it's recursively searching for this in the biomed directory and any other subdirectories. This is repeated with the string "dyspnea".


**Examples with `-w`:**

```
grep -w "all" technical/plos/journal.pbio.0020001.txt
        88% of all scientific and technical publications registered by the Science Citation Index
        Canada across all subject areas in
```

<img width="664" alt="lab3pic7" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/cb39ebe7-6ee6-4738-87ab-008e959f8b80">


```
grep -w "for" technical/plos/journal.pbio.0020010.txt
        JSTOR is successful for reasons its founders did not intend. Bill Bowen's inspired
        vision was of a solution to libraries' ever-voracious demands for space to house paper
        bold decision at the time, but the future for access to journal literature lies in
        Learned’, many of which are relevant to current access initiatives. The need for grant
        provides a model for others. Much of the credit must go to JSTOR's enterprising president,
        for easy access to high-quality content was the key to the fulfilment of that promise.
        adaptation of the JSTOR purchasing model for selling outside the United States, the United
        of research to provide opportunities for high-quality research conducted outside North
```

<img width="676" alt="lab3pic8" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/01dd4014-debf-4d01-8821-0925304c9714">

When grep is used with `-w`, it means grep will search for the lines where only the string given is occuring. This means it won't return the lines where the string is part of a larger word, it will only return the lines where the string is a full word or phrase itself. In these examples, the strings are "all" and "for" which can both be found in larger words. If we want to look for lines with these words by themselves and we don't use `-w`, then the output could include results that are not what we are looking for.


**Examples with `-l`:**

```
grep -l "Air Force One" *.txt         
  chapter-1.txt
  chapter-10.txt
  chapter-13.2.txt
  chapter-13.4.txt
  chapter-13.5.txt
  chapter-3.txt
```

<img width="499" alt="lab3pic9" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/ee37dc16-b7f3-45f0-9dac-c2400bedc93b">


```
grep -l "nocturnal" technical/biomed/*.txt            
technical/biomed/1468-6708-3-10.txt
technical/biomed/1471-2202-3-20.txt
technical/biomed/1472-6793-2-18.txt
technical/biomed/1472-6882-1-10.txt
technical/biomed/1476-511X-1-2.txt
technical/biomed/rr37.txt
```

<img width="609" alt="lab3pic10" src="https://github.com/anchals1/cse15l-lab-reports/assets/165833636/12cf4c20-24ef-40a9-a2a2-c6dbb46d0ea9">

When grep is used with `-l`, a list of files that contain the string in the command is returned. In these examples, the first output we see is all the files that contain the string "Air Force One", and the second output has all the files that contain the string "nocturnal". This is helpful if we want to know which files contain a keyword/phrase we want to filter by so there's a smaller list of files and is easier to navigate. 
