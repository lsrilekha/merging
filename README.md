def merge_sort(arr):
if len(arr)<=1:
return arr
mid=len(arr)//2
left_half=merge_sort(arr[:mid])
right_half=merge_sort(arr[:mid])
return merge(left_half,right_half)
def merge(left_half,right_half):
merged=[]
i=j=0
while i<len(left_half) and j<len(right_half):
if left_half[i]<right half[j]:
merged.append(left_half[i])
i+=1
else:
merged.append(right_half[j])
j+=1
merged.extend(left_half[i:])
merged.extend(right_half[j:])
return merged
arr=list(map(int,input().split()))
sorted_arr=merge_sort(arr)
print(sorted_arr)
# merging
