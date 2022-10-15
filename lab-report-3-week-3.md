# Week 3 Lab Report

## Part 1: Search Engines
Here's the code for simple search engine I have made:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
        String keyword;
        int num = 0;
        int num2 = 0;
        String[] keyWordlist = new String[9999];
        String newKeyword;


    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Welcome to the Simple Search Engine!!!");
            
        } else if (url.getPath().equals("/" + keyWordlist[0])) {
            keyword = keyWordlist[0];
            return String.format(keyword);
        } else if (url.getPath().equals("/" + keyWordlist[1])) {
            keyword = keyWordlist[1];
            return String.format(keyword);
        } else if (url.getPath().equals("/" + keyWordlist[2])) {
            keyword = keyWordlist[2];
            return String.format(keyword);
        } else{
                System.out.println("Path: " + url.getPath());
                if (url.getPath().contains("/add")) {
                    String[] parameters = url.getQuery().split("=");
                    if (parameters[num].equals("newKeyword")) {
                        newKeyword = String.format(parameters[num]); 
                        keyWordlist[num2] = newKeyword;
                        num2++;
                        return String.format("A New Keyword Has Been Added: %s.", parameters[num+1]);
                    }
                    
                }
                if (url.getPath().contains("/search")){
                    String[] parameters2 = url.getQuery().split("=");
                        if (parameters[0].equals)
                    }


                }
            }
            return "404 Not Found!";
        }
    }

class SearchEngine {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
Search Engine Screenshot:

![Search Engine](https://user-images.githubusercontent.com/114555448/195967516-b1e70a8e-b3d6-4262-ba51-be08a3f93a84.jpg)
* The main method that is being called when this code is being executed is the getPath() method.
* The values that this method has influence over is mainly the url path to see if it only contains "/".
* If this value changes, it'll show a different message that depends on the keyword.

Add method Screenshot:

![Add Screenshot](https://user-images.githubusercontent.com/114555448/195967755-12d77450-6797-428b-9b7a-fd56c1fc9b04.png)
* The main method that is being called by this url is still the getPath() method, with the addition of the getQuery() method.
* The values that this method has influence over is the num value and the keyword variables.
* If these values changed, then the add method would switch between each of the added keywords.

## Part 2: Debugging Code
Array Test Code Input:
![image](https://user-images.githubusercontent.com/114555448/195968791-b6f7bd27-cd4c-428e-b3a3-6ad2f44ea356.png)
![reverseInPlace Tests](https://user-images.githubusercontent.com/114555448/195968893-bca6579d-b4dd-4dcb-93a4-166269b1a00c.jpg)

Array Test Code Output:
![reverseInPlace Failed Tests](https://user-images.githubusercontent.com/114555448/195968380-c2b5c0c2-46f4-4d2d-b66f-88b4c8deceb0.jpg)

Fixed Code:
![image](https://user-images.githubusercontent.com/114555448/195968828-ef6b3895-9d73-460d-87d5-d33c88103041.png)

The failing-induced input of the reverseInPlace() method is having an array greater than 1 when starting the program. The bug in the method replaces the index values without copying them elsewhere or retaining them in a variable or an array. The symptom and the bug are connected because the array couldn't save the values in itself, so it couldn't reverse it and output it.

