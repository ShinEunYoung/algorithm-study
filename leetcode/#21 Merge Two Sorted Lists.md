# 문제: Merge Two Sorted Lists

Merge two sorted linked lists and return it as a new list. The new list should be made by splicing together the nodes of the first two lists.


**Example:**
>Input: 1->2->4, 1->3->4
>
>Output: 1->1->2->3->4->4



# 코드

    function ListNode(val, next) {
        this.val = (val===undefined ? 0 : val)
        this.next = (next===undefined ? null : next)
    }

    /**
    * @param {ListNode} l1
    * @param {ListNode} l2
    * @return {ListNode}
    */
    var mergeTwoLists = function(l1, l2) {
        var output = new ListNode;
        
        let mergedList = output;
        
        if(!l1 && !l2) return null;
        
        while(l1 && l2){
            if(l1.val < l2.val){
                mergedList.next = l1;
                l1 = l1.next;
            }
            else{
                mergedList.next = l2;
                l2 = l2.next;
            }
            mergedList = mergedList.next;
        }
        
        mergedList.next = l1 || l2;
        
        return output.next;
    };

Date: **2020.05.02**    
Status: **Accepted**  
Runtime: **60 ms(Rank: 85.23%)**  
Memory Usage: **35.4 MB(Rank: 92.31%)** 




