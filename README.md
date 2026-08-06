# Dirichlet Follow-the-Leader Closes the Gap in Simultaneous Multiclass U-Calibration

## Abstract

Can one forecaster attain the optimal regret rate for every bounded proper loss and also adapt to every smooth proper loss? Recent work answered this up to a dimension gap. Its self-concordant perturbation gives roughly $K^{5/4}\sqrt T$ worst-case regret and incurs an additional $\beta\sqrt K\log K$ for $\beta$-smooth losses. We close both gaps with a one-line forecaster. After observing class counts $c_{t-1}$, draw the next prediction from $\mathrm{Dir}(c_{t-1})$, on the face of classes seen so far. This is a fresh Bayesian bootstrap of the outcomes. The analysis rests on an exact identity: averaging any bounded proper loss under $\mathrm{Dir}(\alpha)$ equals a discrete derivative of its Dirichlet-averaged Bayes risk. The identity makes the be-the-perturbed-leader term telescope to a nonpositive Jensen gap. A one-count likelihood ratio then bounds stability by the inverse square root of that class's count. The resulting single, horizon-free algorithm satisfies

$$\sup_{\ell}\\,\mathbb E\\,\mathrm{Reg}_\ell \leq 4\sqrt{S_TT} \leq 4\sqrt{KT},$$

$$\mathbb E\\,\mathrm{Reg}_\ell \leq \tfrac{5}{2}\beta(1+\log T)\qquad\text{for every }\beta\text{-smooth proper }\ell.$$

Here $S_T$ is the number of observed classes. Known lower bounds show that both rates are optimal in their nontrivial regimes. The proof covers nondifferentiable losses and changes of the active simplex face.

## Main results

**Theorem (Simultaneously optimal regret).** For every $K,T\geq 1$, let $S_T$ be the number of distinct outcomes observed. The Dirichlet Follow-the-Leader forecaster satisfies

$$\mathrm{PUCal}_T \leq 4\sqrt{S_T T} \leq 4\sqrt{\min\\{K,T\\}\\,T}.$$

Simultaneously, for every $\beta$-smooth proper loss $\ell$,

$$\mathrm{Reg}_\ell(T) \leq \tfrac{5}{2}\beta H_T \leq \tfrac{5}{2}\beta(1+\log T),$$

where $H_T=\sum_{t=1}^T 1/t$. Both worst-case rates are optimal up to universal constants in their nontrivial regimes.

**Lemma (Count deletion, the Dirichlet-proper-loss identity).** Let $\alpha\geq 0$, $n=\sum_i\alpha_i$, and suppose $\alpha_j\geq 1$. For $F(\alpha)=\mathbb E_{P\sim\mathrm{Dir}(\alpha)}f(P)$ with $f$ the Bayes risk of $\ell$,

$$\mathbb E_{P\sim\mathrm{Dir}(\alpha)}\\,\ell(P,e_j) = nF(\alpha) - (n-1)F(\alpha-e_j).$$

Averaging any bounded proper loss under a Dirichlet posterior equals a discrete first derivative of the Dirichlet-averaged Bayes risk. This is the mechanism that makes the perturbed-leader term telescope to a nonpositive Jensen gap.

**Lemma (One-count stability).** The total variation between consecutive Dirichlet predictions is controlled by an inverse square root of the incoming class's count. This is the second half of the analysis: perturbed-leader stability that plugs into the identity to give the $\sqrt{S_T T}$ rate.

**Lemma (Smooth proper-loss FTL).** For any $\beta$-smooth proper loss, the follow-the-leader term of the same forecaster contributes only $\tfrac{5}{2}\beta H_T$ regret. This is the second half of the simultaneous guarantee: no separate algorithm for the smooth regime is needed.

## Keywords

online learning, U-calibration, proper loss, follow-the-perturbed-leader, Dirichlet distribution, Bayesian bootstrap, smooth loss adaptation, multiclass forecasting, horizon-free regret

## Files

- `main.pdf`
- `main.tex`
- `references.bib`
- `iclr2027_conference.sty`, `iclr2027_conference.bst`, `natbib.sty`, `fancyhdr.sty`
- `supplement.zip` bundled auxiliary material (identity verification script and README)
- `main.pdf.ots`, `README.md.ots`, `supplement.zip.ots` OpenTimestamps priority proofs
