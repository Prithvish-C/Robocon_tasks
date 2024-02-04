//Pascal's Triangle

class Solution:
    def generate(self, numRows: int) -> List[List[int]]:
        res = [[1]]
        for i in range(numRows - 1):
            temp = [0] + res[-1] + [0]
            row = []
            for j in range(len(res[-1]) + 1):
                row.append(temp[j] + temp[j + 1])
            res.append(row)
        return res

//Merge 2 sorted lists

# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def mergeTwoLists(self, list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
        def sort(list1, list2):
            if list1 is None:
                return list2
            if list2 is None:
                return list1
            else:
                if list1.val <= list2.val:
                    merged_list = ListNode(list1.val)
                    merged_list.next = sort(list1.next, list2)
                else:
                    merged_list = ListNode(list2.val)
                    merged_list.next = sort(list1, list2.next)
                return merged_list
        
        return sort(list1, list2)


//Valid Parentheses

class Solution:
    def isValid(self, s: str) -> bool:
        stack = []
        lookup = {")":"(", "}":"{", "]":"["}
        
        for p in s:
            if p in lookup:
                if stack and stack[-1] == lookup[p]:
                    stack.pop()
                else:
                    return False
                
            else:
                stack.append(p)

        return stack == []

//Robot return to origin

class Solution:
    def judgeCircle(self, moves: str) -> bool:
        def move(a,i,j):
            if(a=='L'):
                j-=1
            elif(a=='R'):
                j+=1
            elif(a=='U'):
                i-=1
            else:
                i+=1
            return i,j
        i=j=0
        for a in moves:
            i,j=move(a,i,j)
        return i==0 and j==0    

//Construct the rectangle

from math import sqrt
class Solution:
    def constructRectangle(self, area: int) -> List[int]:
       sqrt_area=int(area**0.5)
       for length in range(sqrt_area,0,-1):
           if area %length==0:
               width=area//length
               return [width,length]
