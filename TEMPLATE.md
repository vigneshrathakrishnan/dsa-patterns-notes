# Two Sum

## Pattern
Hashing

## Approach
- Use a hashmap to store visited numbers
- For each number, check if (target - num) exists

## Key Insight
Lookup in O(1) using hashmap reduces time complexity

## Mistake I Made
(TBD)

## Complexity
- Time: O(n)
- Space: O(n)

## Code
```js
function twoSum(nums, target) {
  const map = new Map();

  for (let i = 0; i < nums.length; i++) {
    const complement = target - nums[i];

    if (map.has(complement)) {
      return [map.get(complement), i];
    }

    map.set(nums[i], i);
  }
}