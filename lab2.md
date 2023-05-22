# Welcome to CSE 15L *Lab Report 2*
## Part 1
Working with the `StringServer`

Here is what the code for StringServer looks like:
![Image](stringserver.png)


Here we see how how using /add-messages works:
![Image](single.png)
- The method called while trying these diferent paths are the handleRequest method, which basically takes the string given such as *Giselle* and it returns it on the screen as we see in the imgae. 
- The relavant argumnets are URL url which are basically shows the URL and the contents of it such as the path and query.
- The values of the relevant fields change depending on requests made on the server.As we see in the code if both conditions are meet then it updates to the string of choice given if not it remains unchanged. 

More exampels to show how how using /add-messages works with single strings:
![Image](seconds.png)

Just like before we see that:
- The method called while trying these diferent paths are the handleRequest method, which basically takes the string given such as *Howareyou* and it returns it on the screen as we see in the imgae. 
- The relavant argumnets are URL url which are basically shows the URL and the contents of it such as the path and query.
- The values of the relevant fields change depending on requests made on the server.As we see in the code if both conditions are meet then it updates to the string of choice given if not it remains unchanged. 

## Part 2
### Bugs from lab 3
Failure inducing input for method `reverseInPlace` 

```
  @Test
  public void testReversedInPlace2(){
    int[] input2= {1,2,3,4};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{4,3,2,1}, input2);
  }
```
This test is meant to have an outcome of an int array that follows this format `{4,3,2,1}` yet the bug in the code causes it to print something else. We see this in the following image. This image will show the output than can be considered the **symptom** of the bug.
![Image](failure1.png)

<sub> This image shows that for index 2, the expected value was 2 but the actual value from the buggy program was 3. This is because the the for loop used in the reverseInPlace method does not divide the length (used as the condition for i) so it essentially switches the elements to the correct reversed order and instead of stopping there it does this once more, setting the array back to its original order. </sub>

Before fixing this issue, we could try more tests. We can try one that would not induce failure. 

```
  @Test
  public void testReversedInPlace3(){
    int[] input2= {1};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{1}, input2);
  }
```
Since this test is reversing the order of an array with only one element in it, it does not accuretly show the bug. We see this in the following image.
![Image](pass1.png)
<sub> Which basically shows that this test ran and there was no issue with the actual and expected output. </sub>

Now the following code is the one with the bug:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

As mentioned bofore one of the reasons why the code does not work as intended is becaused of the condition for i in the for loop. It also fails to keep track of the item that is moving from the first index to the last. To fix something like this we could alter the code in the following way:

```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp=arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length -i-1]=temp;

    }
  }
```


## Part 3
### New Knowledge
These past two labs tought me several new things that I didnt know before.

Starting with the URLHandler:
+ We worked to understand how this program takes a "URL as input and respond with the text of a web page". We got to see this with different taks during the lab.
![Image](numberurl.png)
![Image](incrementedurl.png)
These are some examples of different ways we practiced with the urlhandler interface. We used the given commands to see the effect each had on the url. As seen in the pictures one of them would increment the number that would be outputed, after calling the increment path.
+ We built and run the server on our local computer which was something that i had also not done before.

More from lab 3:
+ All though I had written tests for some of my other classes to test a method I hadnt yet used JUnit. So using JUnit to test and work with was at first  confusing but after seeing the examples given it was simple to follow. 
+ I was able to practice when writing tests for the methods with bugs, and since I sort of knew what the method was supposed to output looking at the error thrown by JUnit it just made it easier to understand how it worked and overall it was a helpful tool to test code and debug it.
