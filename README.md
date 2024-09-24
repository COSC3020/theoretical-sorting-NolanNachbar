# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

If you had a blackbox implementation of their algorithm, you would be forced to test it by running it through a variety of test cases. You could choose to give it 5 sorted arrays, then 5 randomized arrays. As you test it, you could plot your results; doing so, you would hope to see a linear relationship between the runtime and the array size, leading you to conclude that it does have $O(n)$ runtime.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

The complexity of the general sorting problem is $\Theta(n\log n)$; the claimed $O(n)$ algorithm is then impossible because there are $n!$ possible orderings of the elements. We know that the orderings can be arranged into a binary tree where there's a leaf for each one. The height of this tree is at least $\log n!$, so in the worst case there are at least $\log n!$ comparisons, and we know $lg(n!) = n \log n$. Thus the best theoretical runtime of $O(n\log n)$. The researcher is lying.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

I did this all on my own but I talked with Collin Davis about how to do the first part. 
