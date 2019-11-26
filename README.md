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
