f = open("input.txt","r")
nums = [int(i) for i in f.readlines()]
target = 2020
for num in nums:
    if target - num in nums:
        print(num * (target - num))
        break
    
    
    f = open("input.txt","r")
nums = [int(i) for i in f.readlines()]
nums.sort()
i = 0
while i < len(nums) - 2:
    j = i + 1
    k = len(nums) - 1
    while j < k:
        sum = nums[i] + nums[j] + nums[k]
        if sum == 2020:
            print(nums[i],nums[j],nums[k])
            print(nums[i] * nums[j] * nums[k])
            break
        elif sum > 2020:
            k -= 1
        else:
            j += 1
    i += 1
