> Given a list of strings, return a list where each string has "*" added at its end.

- addStar(["a", "bb", "ccc"]) → ["a*", "bb*", "ccc*"]
- addStar(["hello", "there"]) → ["hello*", "there*"]
- addStar(["*"]) → ["**"]

      public List<String> addStar(List<String> strings) {
        return strings.stream()
                .map(x -> x + "*")
                .collect(Collectors.toList());
      }
