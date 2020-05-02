# 문제: Valid Parentheses

Given a string containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

An input string is valid if:

Open brackets must be closed by the same type of brackets.
Open brackets must be closed in the correct order.
Note that an empty string is also considered valid.


**Example 1:**
>Input: "()"
>
>Output: true


**Example 2:**
>Input: "()[]{}"
>
>Output: true


**Example 3:**
>Input: "(]"
>
>Output: false


**Example 4:**
>Input: "([)]"
>
>Output: false


**Example 5:**
>Input: "{[]}"
>
>Output: true




# 코드

    /**
    * @param {string} s 
    * @return {boolean}
    */
    var isValid = function(s) {
        var stack = [];
        
        if(s.length == 0)
            return true;
        
        else if(s.length % 2 != 0)
            return false;
        
        for(var char of s){        
            switch(char){
                case "(" :
                    stack.push(")")
                break;
                case "{" :
                    stack.push("}")
                break;
                case "[" :
                    stack.push("]")
                break;
                default:
                    if(stack.pop() != char)
                        return false;
                break;
            }
        }
        
        return stack.length == 0;
    };

Date: **2020.05.02**    
Status: **Accepted**  
Runtime: **76 ms(Rank: 83.94%)**  
Memory Usage: **33.8 MB(Rank: 78.33%)** 




