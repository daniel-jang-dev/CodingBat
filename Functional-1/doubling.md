> Given a list of integers, return a list where each integer is multiplied by 2.

- doubling([1, 2, 3]) → [2, 4, 6]
- doubling([6, 8, 6, 8, -1]) → [12, 16, 12, 16, -2]
- doubling([]) → []

      public List<Integer> doubling(List<Integer> nums) {
        List<Integer> nums2 = new ArrayList<>();
        for(Integer n : nums)
          nums2.add(n * 2);
        return nums2;
      }

      public List<Integer> doubling(List<Integer> nums) {
        nums.replaceAll(n -> n * 2);
        return nums;
      }
      // JAVA 8
      public List<Integer> doubling(List<Integer> nums) {
        return nums.stream()
        .map(n -> n * 2)
        .collect(Collectors.toList());
      }
