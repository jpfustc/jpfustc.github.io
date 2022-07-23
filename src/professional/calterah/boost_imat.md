# Boost IMAT algorithm

Iterative Method with Adaptive Thresholding is a cheap and robust compressed sensing technique. Its general principles can be described as such:

* Suppose a signal can be transformed between two domains. The signal is sparse in one domain, and its defect is known in the other domain.
* Define the two inversal transforms
* With signal in sparse domain, apply some filter to utilize its sparsity
* With signal in defect domain, mask the filtered signal to utilize the knowledge of defect
* Iterate until convergence or timeout

e.g. Consider an Angle of Arrival estimation problem:

* signal is of known defect in spatial domain (due to sparse array design), and can be considered sparse in angular or spectral domain. (priori knowledge)
* signal can be transformed between spatial domain and spectral domain with FFT/iFFT, or DBF matrix/inverse DBF matrix.
* signal can be masked in spatial domain given sparse array design
* signal can be filtered in spectral domain given certain conditions



