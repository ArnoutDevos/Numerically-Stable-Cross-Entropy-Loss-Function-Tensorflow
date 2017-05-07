This is  only show how the 'softmax_cross_entropy_with_logits()' function in Tensorflow internally works, and estimate the exp() of large numbers.


Based on Tensorflow docmunet (link to mnist example) without using the 'softmax_cross_entropy_with_logits()' function for calculating loss in Tensorflow, we face the problem of numerically unstable results, actually happen in large numbers, this problem arises when the logits from the network output are large numbers, so python returns 'inf' in result, consider our network has 3 output, and they are large numbers such: [1000, 2000, 2500], now we should sqush this logits with Softmax $ \sum_{\forall i}{x_i^{2}} $ 
 
The "Numerically-Stable-Cross-Entropy-SingleLabel.py" file 
