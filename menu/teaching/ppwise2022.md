---
layout: page
title: "Wave Equation"
permalink: /teaching/ppwise2022
---

## The Manual
The manual with all project tasks is available [here](/menu/teaching/wave_2022.pdf).

## The Project
The Wave Equation project consists of an analytical and numerical part.
Numerical Part topics:
- Finite differencing
- Convergence
- Runge-Kutta time integration (we stick to RK4)
- Periodic and open boundary conditions
- Numerical stability
- Black hole perturbations (Regge-Wheeler equation) [previous knowledge on GR **strongly** recommended]

Focus on the main tasks of the project, if there's time at the end you can go through the bonus tasks. A good score implies the successful completion of tasks 1-10 in addition to a satisfactory poster presentation (more details on the evaluation later).

Recommended reads:
- Finite Difference computing with PDEs, [link](https://suche.thulb.uni-jena.de/Record/89248148X)
- Computational Physics, Chapter 3, [link](https://farside.ph.utexas.edu/teaching/329/329.pdf)
- Lecture Notes on GR, Chapter 7, [link](https://arxiv.org/pdf/gr-qc/9712019.pdf)
- Lecture Notes on GW, Chapter 7, [link](http://sbernuzzi.gitpages.tpi.uni-jena.de/gw/notes/2022/main_v0.2.pdf)

### Poster
- Size A0
- $\LaTeX$ template available [here](https://git.tpi.uni-jena.de/mstnhsr/tikzposter_corporatedesign)
- Non-$\LaTeX$ templates [here](https://www.uni-jena.de/cd-vorlagen)


## Programming
- Python, C, C++ [Python highly recommended]
- Good programming practice:
	- Easy to understand variable names
	- Comment your code:
  
```
def fft(t, h):
    """
    Compute real (fast) Fourier transform
    Obs. Real FFT assumes that the input signal is real time-series.
    Analogously, This means that we are considering only positive frequencies (hermitianity).
		
    Input:
    * t : time axis
    * h : waveform
		
    Output:
    * f: frequency axis [Hz] (f>=0)
    * hfft: Fourier transform of h (complex array)
    """
    dt      = t[1]-t[0]
    hfft    = np.fft.rfft(h) * dt
    f       = np.fft.rfftfreq(len(h), d=dt)
    return f, hfft
```

- Document your code (make notes, will become helpful for the poster). I recommend using `markdown` as it is easy to manage and one can still write $\LaTeX$ equations with it, e.g. $\Pi = \partial_t \phi$, more [here](https://www.markdownguide.org/cheat-sheet/) but also using $\LaTeX$ is OK.
- Another possibility is using Jupyter-Notebooks [also *very* recommended]: [Jupyter server of the FSU Jena](https://jhub.rz.uni-jena.de/)
- If working in a team: I *highly* recommend using `git`. If this is the case, let me know so I can make an account for you in our [TPI's gitlab server](https://git.tpi.uni-jena.de/). More on git:
	- [w3schools](https://www.w3schools.com/git/git_intro.asp?remote=github)
	- [git-scm](https://git-scm.com/docs)
- If you need any help with any of these topics: Python in general, markdown, $\LaTeX$, git, jupyter, etc. Let me know and we can arrange a tutorial session.