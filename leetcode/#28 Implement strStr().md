# 문제: Implement strStr()

Implement strStr().

Return the index of the first occurrence of needle in haystack, or **-1** if needle is not part of haystack.


**Example 1:**
>**Input:** haystack = "hello", needle = "ll"
>
>**Output:** 2


**Example 2:**
>**Input:** haystack = "aaaaa", needle = "bba"
>
>**Output:** 2


# 코드

    /**
    * @param {string} haystack
    * @param {string} needle
    * @return {number}
    */

    var strStr = function(haystack, needle) {
        var index = -1;
        
        if(haystack == needle || !needle)
            return 0;
        
        if(haystack.length < needle.length)
            return index;
        
        for(var i = 0; i < haystack.length - needle.length + 1; ++i){
            if(haystack[i] == needle[0]){
                if(haystack.substr(i, needle.length) == needle){
                    index = i;
                    break;
                }
            }
        }
        return index;
    };

Date: **2020.05.02**    
Status: **Accepted**  
Runtime: **48 ms(Rank: 94.95%)**  
Memory Usage: **33.7 MB(Rank: 100%)** 




