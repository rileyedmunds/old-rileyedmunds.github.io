---
layout: post
title: Vanilla Data Science Models
date: 2017-1-8 9:03:54
---

<style TYPE="text/css">
code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
</style>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
tex2jax: {
inlineMath: [['$','$'], ['\\(','\\)']],
skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry
}
});
MathJax.Hub.Queue(function() {
var all = MathJax.Hub.getAllJax(), i;
for(i = 0; i < all.length; i += 1) {
all[i].SourceElement().parentNode.className += ' has-jax';
}
});
</script>
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>




This winter break, before diving into the [Neural Network Zoo Challenge](http://rileyedmunds.com/2017/01/08/zoo/){:target="_blank"}, I coded up some simple data science models. 

Here's my [code on GitHub](https://github.com/rileyedmunds/datascience){:target="_blank"}, and here are some details behind the algorithms...
  
  
**Singular Value Decomposition**
- *uses* dimensionality reduction
- *algorithm* 
1. Start with matrix $A$.
2. Find $V$, $S$, and $U$ such that$\sum_{n=1}^{\infty} 2^{-n} = 1$ inside text

- **k-Nearest Neighbors**
- k-Means       
- Naive Bayes          
- Support Vector Machine      
- Logistic Regression     
- Decision Tree   
- Random Forest  

    

    
    
