*emergent* provides a toolkit / framework for implementing neural network models, written in [Go](https://golang.org), with an optional Python interface that is automatically generated from the Go code.  See the [github](https://github.com/emer/emergent) site for all the code and extensive documentation.

The primary application of *emergent* is for the biologically-based [*Leabra*](https://github.com/emer/leabra) algorithm, which simulates point neuron equations with either rate-code or spiking activations, and a biologically-based form of error-backpropagation based on bidirectional excitatory projections.  This more complex, many-state-variable model is not well-supported by existing backpropagation-oriented tools such as PyTorch or TensorFlow, which operate fundamentally on simple tensors of floating-point numbers.

A primary goal of *emergent* is to provide effective GUI interfaces that make it easier to understand the functioning of complex neural models, including an interactive 3D NetView, interactive 2D line and bar plots, heat-map grids of tensors, and tables of data.  The [eTorch](https://github.com/emer/etorch) repository provides these interactive GUI elements for PyTorch-based models.

Most existing Python-based simulation systems rely on C / C++ for the high-performance back-end computation, accessed via the higher-level but much slower Python wrapper language.  Go provides an attractive alternative language framework, featuring the runtime speed of complied C code, but a very rapid compilation speed approaching that of interpreted languages like Python (just a few seconds per compile / run iteration).  Furthermore, the language is very elegant and well-designed, with an extensive standard library, resulting in a high-level of programmer productivity.  The garbage-collection runtime system eliminates a huge amount of complexity and headache, and has essentially no noticible effect on running simulations which do not typically allocate much memory once they have started.

# Documentation

* [github wiki](https://github.com/emer/emergent/wiki) has the main framework-level documentation.

* [leabra repository](https://github.com/emer/leabra) documents the *Leabra* algorithm.

* [CompCogNeuro](https://CompCogNeuro.org) is a free online textbook for *Computational Cognitive Neuroscience* modeling, with associated [simulations](https://github.com/CompCogNeuro/sims) based on the *emergent* system.

# Videos

* Demo videos coming soon!

* [CompCogNeuro Lecture Videos](https://www.youtube.com/playlist?list=PLu02O8xRZn7xtNx03Rlq6xMRdYcQgEpar) feature interactive demonstrations of *emergent* models.
