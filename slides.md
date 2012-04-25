!SLIDE

#job_interview

!SLIDE

## Interviewing sucks.
You get asked dumb questions, and are asked to perform stupid programmer tricks.

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

@@@ ruby

    ans.fib(10, :iterative)
    
    => [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
@@@

!SLIDE
#Quine

@@@ ruby

    ans.quine(__FILE__)
    
    => "ans.quine(__FILE__)"
@@@

!SLIDE
#Primes
You want the first _n_ primes? 
You get the first _n_ primes!

@@@ ruby

    ans.primes(10)
    
    => [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]

@@@

!SLIDE

#Benefits

### Saves time!

!SLIDE

#Benefits

### It's easier than actually solving trivial problems yourself.

!SLIDE
#Benefits


### Demonstrate to prospective employers you use libraries to address solved problems, rather than re-inventing the wheel.
!SLIDE
## Ok, they know I can code
# Now what?


!SLIDE
## Personality Questions
# Everyone  lies when they get asked these.

How awful would it be to actually have to confront your greatest weakness.

!SLIDE

# - Fear of clowns
# - Never feels loved
# - Drinks too much

!SLIDE

## SOLUTION
With the job_interview gem, you don't even have to bother thinking of BS.

    include JobInterview::Questions

!SLIDE

## Q. Where do you see yourself in five years?

!SLIDE
## Q. Where do you see yourself in five years?

ruby-1.9.2-p290 :005 > in\_5\_years  

  => "I'd love to have enhanced shareholder value by creating diverse logistical intranet."  

  => "I'd like to made someone else rich with my multi-layered assymetric frame."  

  => "I'd love to have enhanced shareholder value by creating enhanced contextually-based ability."  

!SLIDE
## Q. Why are you leaving your current position?

!SLIDE
## Q. Why are you leaving your current position?  

  => "I'm not happy with the opportunities I have to expedite B2B schemas."  
  
  => "I'm leaving because I can't mesh vertical convergence."  
  
  => "I'm leaving because I have to innovate out-of-the-box metrics."
!SLIDE
## Q. Why are manhole covers round?
!SLIDE
## Q. Why are manhole covers round?  

=> "Because Reuleaux Triangles are hard to manufacture."

=> "Because men are round."

=> "So they don't fall in."

!SLIDE
## Q. What is your greatest weakness?

!SLIDE
## Q. What is your greatest weakness?  

ruby-1.9.2-p290 :027 > greatest_weakness
  

=> "Some times I work too much so I make too much money."

=> "I always care too much so I innovate too hard."

=> "I always fail so rarely so I shift too many paradigms."  

!SLIDE

## Q. Why do you want to work here?

!SLIDE
## Q. Why do you want to work here?  
  

ruby-1.9.2-p290 :051 > why_here
  

=> "Your company is re-inventing sharable mission-critical encryption."  

=> "Your company has revolutionized optimized web-enabled alliance."  

=> "Your company is renowned for secured multi-tasking customer loyalty."  

!SLIDE
## Q. Does P = NP?

!SLIDE
## Q. Does P = NP?  

ruby-1.9.2-p290 :075 > p\_equals\_np
  

=> "With our current models of computation, answering that question remains infeasible."  

=> "If it does, we can kiss encryption goodbye."  

=> "I doubt it, but it would make life easier for traveling salesmen."


!SLIDE

# Will it work?

!SLIDE

# Will it work?

We have excellent test coverage with RSpec, so we think it will.

@@@ ruby

    def is_correct_answer(type, answer)
      if answer.respond_to? :wrong
        return false
      else
        return true
      end
    end
@@@

...

@@@ ruby
    
    is_correct_answer.should be_true
    
@@@

!SLIDE

# The real question

![Why would you do that?](./whywouldyoudothat.jpg)

!SLIDE

- We wanted to hack on something trivial at BohConf
- Silly gems are fun
- We wanted to make a point about how inane most job interviews are.

!SLIDE

#Thanks for allowing us to waste 5 minutes of your time.

