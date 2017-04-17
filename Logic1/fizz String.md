> Given a string str, if the string starts with "f" return "Fizz". If the string ends with "b" return "Buzz". If both the "f" and "b" conditions are true, return "FizzBuzz". In all other cases, return the string unchanged. (See also: FizzBuzz Code)

- fizzString("fig") → "Fizz"
- fizzString("dib") → "Buzz"
- fizzString("fib") → "FizzBuzz"

      // 1. IF - ELSE 
      public String fizzString(String str) {
        String answer = "";
        int len = str.length();
        char first = str.charAt(0);
        char last = str.charAt(len-1);

        if(first == 'f')
        {
          answer = "Fizz";
          if(last == 'b' && first != last)
          {
            answer += "Buzz";
          }
        }
        else
        {
          if(last == 'b')
          {
            answer = "Buzz";
          }
          else
          {
            answer = str;
          }
        }
        return answer;
      }
      // 2. simple
      public String fizzString(String str) {
        boolean f = str.startsWith("f");
        boolean b = str.endsWith("b");

        if (f && b) return "FizzBuzz";
        if (f) return "Fizz";
        if (b) return "Buzz";
        return str;

        // Style: you could use a series of "else" there, but it seems simpler
        // to just not have them.
      }
