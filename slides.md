!SLIDE

#job_interview

!SLIDE

## Interviewing sucks.
You get asked dumb questions, and and are asked to perform stupid programmer tricks.

!SLIDE

#FizzBuzz
## (Don't write it like this)
@@@ ruby
    def fizz_buzz(max)
      acc = []
      (1..max).each do |n|
        if ((n % 3 == 0) && (n % 5 == 0))
          acc << "FizzBuzz"
        elsif (n % 3 == 0)
          acc << "Fizz"
        elsif (n % 5 == 0)
          acc << "Buzz"
        else
          acc << n
        end
      end
      return acc
    end

@@@

