# DSA-Essentials-Bootcamp
Assignment - DSA Essentials Bootcamp

def find_majority_element(nums):
    count = 0
    candidate = None

    for num in nums:
        if count == 0:
            candidate = num

        if num == candidate:
            count += 1
        else:
            count -= 1

    # Verifying if the candidate is the majority element
    count = 0
    for num in nums:
        if num == candidate:
            count += 1

    if count > len(nums) // 2:
        return candidate
    else:
        return -1

nums = [2, 4, 5, 5, 5, 5, 5]
result = find_majority_element(nums)
print(result)
