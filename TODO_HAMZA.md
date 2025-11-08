reflect this .tex of the resume into publications, cv and classes sections:
\documentclass[11pt,letterpaper]{article}

% ---------- Packages ----------
\usepackage[left=0.6in,right=0.6in,top=0.5in,bottom=0.5in]{geometry}
\usepackage[T1]{fontenc}
\usepackage{lmodern}
\usepackage{amsmath}
\usepackage{hyperref}
\usepackage{enumitem}
\usepackage{titlesec}
\usepackage{xcolor}
\usepackage{tabularx}
\usepackage{fontawesome5}

\definecolor{linkblue}{RGB}{0,51,153}

\hypersetup{
  colorlinks=true,
  urlcolor=black,
  linkcolor=black,
  citecolor=black
}

\newcommand{\bluehref}[2]{{\hypersetup{urlcolor=linkblue}\href{#1}{#2}}}

\titleformat{\section}
  {\large\bfseries}
  {}{0em}{}[\titlerule]
\titlespacing{\section}{0pt}{10pt}{6pt}

\setlist[itemize]{leftmargin=1.2em,itemsep=2pt,topsep=2pt,parsep=0pt}

\newcommand{\resumeheading}[2]{%
  \noindent\textbf{#1}\hfill#2\\[2pt]%
}

\pagestyle{empty}
\setlength{\parindent}{0pt}
\setlength{\parskip}{0pt}
\frenchspacing

\begin{document}

% ---------- Header ----------
\begin{center}
{\LARGE\textbf{HAMZA VIRK}}\\[8pt]
{\small
\faEnvelope\ \href{mailto:hvirk2@pride.hofstra.edu}{hvirk2@pride.hofstra.edu} \quad 
\faLinkedin\ \href{https://www.linkedin.com/in/hamza-virk-26856026a/}{linkedin.com/in/hamza-virk} \quad 
\faGraduationCap\ \href{https://scholar.google.com/citations?view_op=list_works&hl=en&user=od7rY-0AAAAJ}{Google Scholar} \quad 
\faGithub\ \href{https://github.com/Hamzavirk1}{github.com/Hamzavirk1}
}
\end{center}

\vspace{-2pt}

% ---------- Education ----------
\section*{EDUCATION}

\noindent\textbf{Hofstra University} \hfill Hempstead, NY\\
B.S. in Mathematics \hfill Sept 2022 -- May 2026\\
\textit{Major GPA: 3.7 $\bullet$ Presidential Scholarship $\bullet$ Dean's List 2024--2025}

% ---------- Papers ----------
\section*{PAPERS}
\noindent\textbf{Blind-IGT: Jointly Decoding Rewards and Rationality in Entropy-Regularized Competitive Games}\\
\textbf{H Virk}, S Amaglobeli, Z Syed\\
Under review, \textit{AISTATS 2026}
\bluehref{https://drive.google.com/file/d/1tyeBUtEADLBOb0LxYf0W3bwalF6skdwV/view?usp=sharing}{§}
\vspace{8pt}

\noindent\textbf{Arbitrage-Free Pricing with Diffusion-Dependent Jumps}\\
\textbf{H Virk}, Y Wu, M John\\
Under review, \textit{Journal of Stochastic Analysis} 
\bluehref{https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5371130}{§}
\vspace{8pt}

\noindent\textbf{Entry Deterrence and Antibiotic Conservation under Post-Entry Bertrand Competition}\\
R Mazzoleni, \textbf{H Virk}\\
Working paper
\vspace{8pt}

\noindent\textbf{Improving a Propensity Score Adjustment Method in Genetic Association Studies using Machine Learning}\\
V Berardi, \textbf{H Virk}, J Ferbinteanu, M John\\
Working paper
\vspace{8pt}


\noindent\textbf{Integer Occurrences in Rational Linear Recurrences}\\
M Lippmann, E Rowland, \textbf{H Virk}$^{\dagger}$\\
Working paper

\footnotesize{
\textit{$^{\dagger}$Authors listed alphabetically (pure mathematics convention)}
}
\normalsize

% ---------- Research Experience ----------
\section*{RESEARCH}

\resumeheading{Student Researcher, EconCS}{Hofstra University}
\textit{Collaborators: \bluehref{https://www.sandro.software}{Sandro Amaglobeli}, \bluehref{https://www.linkedin.com/in/zuhayr-syed-46224322b/}{Zuhayr Syed}} \hfill May 2025 -- October 2025
\begin{itemize}
  \item Pioneered the Blind-IGT framework to resolve fundamental multiplicative scale ambiguity in bilinear inverse problems, enabling first joint recovery of reward parameters and rationality in Quantal Response Equilibria.
  \item Developed NLS estimator and rigorously proved it achieved the optimal convergence rate; extended the framework to Markov Games proving optimal rates and robustness to unknown transition dynamics.
\end{itemize}

\vspace{6pt}


\resumeheading{Research Assistant, Department of Mathematics}{Hofstra University}
\textit{Advisor: \bluehref{https://www.hofstra.edu/faculty-profile/?id=1643}{Dr. Yihren Wu}} \hfill November 2024 -- Present
\begin{itemize}
  \item Established a rigorous framework for arbitrage-free pricing in models with path-dependent jumps. Solved the complex measure-change problem using Girsanov's theorem and conditional Esscher transforms.
  \item Implemented a Gaussian HMM on SPX and VIX data to study market dynamics, using the Lee–Myland test to detect and categorize jumps, analyzing how these jump types affected subsequent state transitions.
\end{itemize}



\vspace{6pt}


\vspace{6pt}


\resumeheading{Research Intern, Feinstein Institute for Medical Research}{Manhasset, New York}
\textit{Advisor: \bluehref{https://www.researchgate.net/profile/Majnu-John}{Dr.~Majnu John}} \hfill June 2025 -- Present
\begin{itemize}
  \item Developed machine learning methods for confounder detection and subset selection in high-dimensional genetic data, improving statistical power of a recently published propensity score-based method.
  \item Compared the performance of various approaches using extensive simulations in R, and a real data analysis of a genome-wide association study.
\end{itemize}


 
\vspace{6pt}

\resumeheading{Research Assistant, Department of Economics}{Hofstra University}
\textit{Advisor: \bluehref{https://scholar.google.com/citations?user=w9foa_oAAAAJ&hl=en}{Dr.~Roberto Mazzoleni}} \hfill September 2025 -- Present
\begin{itemize}
  \item Developed a game-theoretic Industrial Organization model (SPNE) to analyze how Bertrand competition impacted antibiotic conservation by incumbents facing market entry in the presence of evolving resistance.
  \item Proved that the anticipation of fierce price competition universally incentivized strategic conservation to deter entry, independent of bacterial cross-resistance levels—a sharp contrast to established Cournot models.
\end{itemize}



\resumeheading{Research Assistant, Department of Mathematics}{Hofstra University}
\textit{Advisor: \bluehref{https://ericrowland.github.io}{Dr.~Eric Rowland}} \hfill January 2025 -- Present
\begin{itemize}
  \item Ran computational experiments for 24+ weeks testing millions of coefficient pairs to identify minimal/maximal integer runs under certain conditions, using patterns from data to recursively construct new integers.
  \item Characterized integer occurrences in linear recurrences, proving restrictions on consecutive terms and establishing finiteness results via $p$-adic logarithmic bounds.

\end{itemize}

\vspace{6pt}

\resumeheading{ASPiRe REU Fellow}{Hofstra University}
\textit{Project: Topological Data Analysis for hallucination detection in LLMs} \hfill May 2025 -- August 2025
\begin{itemize}
\item Applied persistent homology to LLM attention, developing a framework to detect hallucinations by comparing a response's internal persistence diagram to its prompt-grounded one, measuring the divergence via the Wasserstein distance.
\end{itemize}


% ---------- Talks/Presentations ----------
\section*{TALKS AND PRESENTATIONS}
\begin{itemize}[leftmargin=*, itemsep=2pt]
    \item {\textit{PerToDive for Provable Hallucination Detection}}, ASPiRe Symposium, Hofstra University \hfill August 2025
    \item {\textit{Near-Integer Sequences Satisfying a Linear Recurrence}}, Mathematics Department Seminar \hfill December 2025
\end{itemize}


% ---------- Coursework ----------
\section*{RELEVANT COURSEWORK}
\vspace{2pt}
\begin{itemize}[leftmargin=*, itemsep=1pt, nosep]
\begin{minipage}[t]{0.48\textwidth}
\item MATH 171/172: Real Analysis I \& II$^{\mathrm{T}}$
\item MATH 173: Complex Analysis
\item MATH 135A: Linear Algebra
\item MATH 143: Engineering Mathematics
\item MATH 199C: Topological Data Analysis
\item MATH 145: Abstract Algebra
\item MATH 199B: Statistical Inference
\item MATH 216: Nonlinear Optimization
\item MATH 137: Probability \& Statistics
\end{minipage}
\hfill
\begin{minipage}[t]{0.48\textwidth}
\item MATH 167: Elementary Topology$^{\mathrm{T}}$
\item MATH 198A: Matrix Algebra \& Comp.
\item ECON 186: Econometrics
\item ECON 172: Game Theory
\item ECON 132: Intermediate Macroeconomics
\item MATH 114: Intro to Higher Mathematics
\item MATH 071/072/073: Calculus I, II, III
\item CSC 14: Discrete Mathematics
\item MATH 100: Communicating Mathematics
\end{minipage}
\end{itemize}
\vspace{2pt}
\footnotesize{\textit{T = Taking Spring 2026}}
\normalsize
% ---------- Technical Skills ----------
\section*{TECHNICAL SKILLS}
\noindent\textbf{Languages:} Python, Stata, R, \LaTeX\\
\textbf{Libraries/Packages:} NumPy, pandas, Matplotlib, scikit-learn, hmmlearn; ggplot2, dplyr, tidyr, caret (R), estout, outreg2\\
\textbf{Specialized Techniques:} Maximum likelihood estimation, Hidden Markov Models, time series analysis, ARIMA modeling, Monte Carlo simulation, bootstrap resampling, model calibration

% ---------- Honors ----------
\section*{HONORS AND AWARDS}
Presidential Scholarship, Hofstra University $\bullet$ ASPiRe Summer Research Fellowship (\$5000 award) $\bullet$ Dean's List 2024--2025 $\bullet$ Academic Excellence Scholarship, Forman Christian College 
% ---------- Languages and Interests ----------
\section*{LANGUAGES AND INTERESTS}
\noindent\textbf{Languages:} English, Urdu (Native), Punjabi\\
\textbf{Interests:} Chess, poker, literature, music
\end{document}