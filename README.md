# Eigenvectors-of-Random-Matrices-Overlap-of-Ground-States
Here we examine the overlap of ground states of some randomly generated Hamiltonians of Majorana fermions.
## Some Background
One of the hottest topics in physics recently is the development of quantum computation. In particular, it came back to the spotlight with the release of the following article.

<https://www.nature.com/articles/s41586-019-1666-5>

In fact over the past two decades, different groups have attempted to engineer devices for quantum computation. The ideas behind different designs had been theoretically investigated even further. One of the fascinating ideas, which unfortunately hasn't been confirmed, is the so-called ___Majorana fermions___. Each majorana fermion, in plain English, can be roughly understood as half a fermion, or half an electron. Loads of studies are devoted to realizing excitations of this type in various materials. The author also contributed to one paper aiming to locate a Majorana bound state in spintronic effect.

<https://journals.aps.org/prb/abstract/10.1103/PhysRevB.95.014519>

Beside the candidate of quantum computation, the Majorana fermion itself has interesting algebraic properties and owns a big business in the enterprise of topological phases of matter. 

In this project, I want to report some observations I encountered when looking at some random Majorana models.
## Majorana Fermions in a Nutshell and the Theme of the Project 
The simplest model for _2N_ Majorana fermions consists of a _2N_ by _2N_ antisymmetric matrix _A_. The Hamiltonian, or the model that governs the dynamics in quantum mechanics, can be modeled by i/4 times _A_. The eigenvalues of the matrix corresponds to the energy allowed in this model. Very often physicists are interested in properties of the lowest energy state, ___the ground state___. 
That day a friend of mine came to me, discussing the discovery that was troubling her. Apart from her main puzzle, I realized what she did was essentially computing the overlap of the ground states of the same set of Majorana fermions "energized" by two different _A_ s. 

Neither did I want to steal the thunder, and nor did I possess the technical skills to do so. It came across me that if one was aiming to deduce any result for two general _A_ s, such property could probably holds true for two arbitrarily selected _A_ s. This naive idea led to some simulation results of the ground state overlaps. 

This idea is implemented as follows. I initialize two matrix's _A_, _B_, the entries of each of which are uniformly generated random number over a range. Two asymmetric Hermitian matrices are constructed with i(_A_ - _A_^T)/4 and i(_B_ - _B_^T)/4. They then can be diagonalized, and the overlap of the ground states can be computed. Repeating this process for a couple of times, we can plot the histogram of the distribution of the magnitude of overlaps. In the following I plot the histograms after 10000 iterations with different matrix sizes (4 by 4, 20 by 20, 40 by 40). The index _i_ denotes the range of random number. (When there are _N_ fermions in the problem, the matrix will be of size 2 _N_ by 2 _N_.)

#### Uniform Random U(0,i)
![The distributions of overlaps](https://github.com/whhsiao/Eigenvectors-of-Random-Matrices-Overlap-of-Ground-States/blob/master/distributions.png)

The above rows suggest that they may form some kind of distributions especially when the number of fermions become large. An immediate question is that how sensitive is these distributions to different parameters in the problem. From the above rows we sort of get the sense that they are not so sensitive to the range of uniform distribution and definitely depend heavily on the size of the matrix.

Another reason for looking into other distributions is the following. I note the difference of two uniform distributions is no longer a uniform distribution, but rather a triangle type distribution, which is not the most typical distribution we see everyday. Could these distributions look peculiar because of this funky distribution? This speculation may be eliminated by looking into similar sampling results using other probability distribution functions.

In the following I present the distributions of histograms generated by other random variables. First the exponential variables with parameters _i_.

#### Exponenital distribution Exp(i)
![The distributions of overlaps of Exponential r.v.](https://github.com/whhsiao/Eigenvectors-of-Random-Matrices-Overlap-of-Ground-States/blob/master/distributionHistogramExponential.png)

Next the normal distribution with mean 0 and standard deviation _i_.
#### Normal distribution N(0,i^2)
![The distributions of overlaps of Gaussian r.v.](https://github.com/whhsiao/Eigenvectors-of-Random-Matrices-Overlap-of-Ground-States/blob/master/distributionHistogramGaussian.png)

From pure eyeballing, we see there is no substantially difference between these distributions. Therefore, we see they are sentitive to the size of the matrix, but insensitive to the scaling of random variables or even the exact form the the random variable. A particular important message is given by reuslt generated by normal distributions. I have mentioned the difference between two uniform distributions is no longer a uniform distribution. Similarly, the difference between two exponential distributions is not an exponential distribution, but rather a Laplace distribution. Nonetheless, the difference between 2 normal distributions is still a normal random variable. Therefore, the above sequences of numerical experiments entail at least for some classs of antisymmetric Hermitian matrices, the results approach that generated by some normal random variables.

This observation actually gives us some hint in terms of finding the underlying probability distribution of the overlaps. I then try to generate overlaps of eigenstates in the same fashion using the matrices from the family of Gaussian ensemble. In the following I compare the smooth histograms generated by the original method (the entries of which are differences between Gaussian random variables) and standard Gaussian Sympletic ensemble matrices and obtain the comparison for matrix sizes 20 by 20 and 40 by 40 respectively.

![comparison with GSE size equal 20 by 20](https://github.com/whhsiao/Eigenvectors-of-Random-Matrices-Overlap-of-Ground-States/blob/master/comWithGSEN20.png)

![comparison with GSE size equal 40 by 40](https://github.com/whhsiao/Eigenvectors-of-Random-Matrices-Overlap-of-Ground-States/blob/master/compWithGSE.png)

Based on eyeballing, we see GSE could be a role model of these sequence of observations for further investigation.

## Fitting the distribution for Fairly large dimensions
### The probability model
The next goal for me is to find a probability distribution that can model this. A probability model should satisfy the following conditions.
* The domain is bounded within [0,1].
* The distribution is left skewed. 

## Fidelity susceptibility of GSE
