# CMPS 6610 Problem Set 03
## Answers

**Name:**Petra Santos


Place all written answers from `problemset-03.md` here for easier grading.




- **1b.**
In this case, both Work and Span are O(n). The algorithm does one comparison O(1) per element and goes through every element of L once O(n). Iterate is sequential so it needs the previous result to compute the next, so there's no parallelization possible here and span = work = O(n).




- **1d.**

Reduce only takes functions that are associative in order to take advantage of its divide-and-conquer algorithm. Reduce splits the sequence in half, recursively calling the function on each half-sized piece. So, even though the total work is the same (as iterate's) O(n), the span is O(log n), since we have log n levels, with all the calls at each level running in parallel.



- **1e.**
Instead of doing a split of 1:1 like reduce, reduce splits matches unevenly, into pieces of n/3 and 2n/3 (instead of 2 n/2 pieces). The work doesn't change with a different split, it's invariant regardless to split sizes. As for span, it will be S(n)= S(2n/3) + O(1) instead of S(n)= S(n/2) + O(1), since we'll have to wait on the 'slower' branch. This recurrence solves to O(log_{3/2} n) and log_{3/2} n = log n / log(3/2), which collapses to the same O(log n) under big-O.




- **2a.**
dedup(A) =
  let n = |A|
      firstFlags = ⟨ isFirst(A, i) : 0 ≤ i < n ⟩
  in ⟨ A[i] : 0 ≤ i < n | firstFlags[i] ⟩

isFirst(A, i) = reduce (∨) false ⟨ A[j] = A[i] : 0 ≤ j < i ⟩

Like previously said, work and span or reduce are O(n) and O(logn)

$$W_{\text{isFirst}}(i) = W_{\text{build}}(i) + W_{\text{reduce}}(i) = O(i) + O(i) = O(i)$$

$$S_{\text{isFirst}}(i) = S_{\text{build}}(i) + S_{\text{reduce}}(i) = O(1) + O(\log i) = O(\log i)$$

- **2b.**





- **2c.**






- **3b.**





- **3d.**





- **3f.**




