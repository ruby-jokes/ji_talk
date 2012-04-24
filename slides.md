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

!SLIDE

#FizzBuzz

@@@ ruby

    require 'job_interview'
    
    ans = JobInterview::Answer.new
    ans.fizz_buzz(5)
    
    => [1, 2, "Fizz", 4, "Buzz"]
@@@

!SLIDE

#Fibonacci

(iterative _and_ recursive implementations!)

!SLIDE

#Fibonacci

@@@ ruby
   
    ans.fib(10)
    
    => [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]

@@@

!SLIDE

#Fibonacci
Defaults to recursive. But we can also iterate!

    ans.fib(10, :iterative)
    
    => [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
    

!SLIDE
#Quine

@@@ ruby

    ans.quine(__FILE__)
    
    => "ans.quine(__FILE__)"
@@@

!SLIDE
#Primes
You want the first _n_ primes? You get the first _n_ primes!

@@@ ruby

    ans.primes(10)
    
    => [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]

@@@

!SLIDE