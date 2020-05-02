# 문제: Longest Common Prefix

Write a function to find the longest common prefix string amongst an array of strings.  
If there is no common prefix, return an empty string "".

**Example 1:**
>Input: ["flower","flow","flight"]  
>Output: "fl"

**Example 2:**
>Input: ["dog","racecar","car"]  
>Output: ""  
>Explanation: There is no common prefix among the input strings.


**Note**  
All given inputs are in lowercase letters a-z.


# 코드
    /**
    * @param {string[]} strs
    * @return {string}
    */
    var longestCommonPrefix = function(strs) {

        let result = "";
        if (!strs.length) return result;
        
        for(let i = 0; i < strs[0].length; i++){
            let prefix = strs[0].substring(0, i + 1);
            
            for(let str of strs){
                if(prefix != str.substring(0, i + 1)){
                    return result;
                }
            }
            result = prefix;
        }
        
        return result;
    };

Date: **2020.03.09**    
Status: **Accepted**  
Runtime: **60ms(Rank: 629.40%)**  
Memory Usage: **36.2MB**




