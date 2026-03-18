# Gravitational-Wave-Imprints-of-the-GERT-Phase-Transitions
The Cauldron’s Scar and the Thermodynamic Parsec: Gravitational Wave Imprints of the GERT Phase Transitionsrelacionados ao paper  
## What this repository contains

| File                  | Description                                             |
| --------------------- | ------------------------------------------------------- |
| `gert_p5_numerics.py` | Full numerical verification of all equations in Paper V |
| `README.md`           | This file                                               |

The manuscript itself (`.docx`) is provided separately as a supplementary file.

---

## Overview

This script reproduces every numerical result in Paper V from first principles, organised into the two mathematical blocks of the paper:

### Mathematical Block I — Tensor Spectral Index (Paper V, Section 4)

Derives the GERT prediction for the primordial tensor spectral index nT from the **Rayleigh–Jeans thermal fluctuations** of the Primordial Cauldron (Layer 2), and demonstrates the violation of the inflationary consistency relation nT = −r/8.

**Key result:**  
In the GERT framework, all tensor modes freeze simultaneously at crystallisation αem (not progressively via horizon exit). Applying the equipartition theorem to the proto-metric tensor modes:

```
<|h_k|²> ∝ k_B T_Cauldron / k²    (Rayleigh–Jeans)
Δ²_T(k) = k³/(2π²) · <|h_k|²>  ∝  k¹
```

→ **n_T^GERT = +1** in the equipartition limit  
→ **n_T^GERT ∈ [0, +1]** generically (flat to blue)  
→ **n_T ≠ −r/8** — inflationary consistency relation violated without fine-tuning

---

### Mathematical Block II — Entropic Phase Transition and NANOGrav (Paper V, Section 5)

Derives the epoch, Hubble rate, and characteristic gravitational wave emission scale of the GERT **Entropic Phase Transition** from the empirical anchor of Paper I, and identifies the result with the NANOGrav nanohertz signal.

**Input (from Paper I, zero free parameters added here):**

```
log₁₀ ρ_L2  =  −23.93  kg/m³    (Paper I best-fit, χ²/dof ≈ 0.99)
H₀           =  72.5  km/s/Mpc
Ω_m = 0.30,  Ω_Λ = 0.70,  Ω_r = 7.9×10⁻⁵
```

**Derivation chain (all equations numbered as in the paper):**

| Equation      | Expression                   | Result                             |
| ------------- | ---------------------------- | ---------------------------------- |
| (5.4)–(5.5)   | (1+z)³ = ρ_L2/ρ_m,0          | **z_L2 = 6.35 ± 0.02**             |
| (5.6)–(5.9)   | H★ = H₀·E(z_L2)              | **H★ = 10.95 H₀ = 2.573×10⁻¹⁷ Hz** |
| (5.13)        | f_emit = f_NANOGrav·(1+z_L2) | f_emit = 2.205×10⁻⁸ Hz             |
| (5.14)–(5.15) | λ★ = c/f_emit                | **λ★ = 0.441 ± 0.003 pc**          |
| (5.16)–(5.18) | β/H★ = 2π·f_obs·(1+z)/H★     | **β/H★ = 5.38×10⁹**                |

**The Thermodynamic Parsec:**  
λ★ = 0.441 ± 0.003 pc coincides with the SMBHB final-parsec bottleneck scale, providing a unified thermodynamic origin for the NANOGrav signal and the final-parsec problem. This value is derived from two independently measured quantities (Paper I cosmological fit + NANOGrav observation) with **no free parameters**.

---

## Requirements

Python 3.7+ with standard library only. No external packages required.

```bash
python3 gert_p5_numerics.py
```

---

## Output

The script prints:

1. **Mathematical Block I** — inflationary consistency relation derivation, GERT Rayleigh–Jeans derivation, generalisation via source spectral index nS
2. **Mathematical Block II** — step-by-step derivation of z_L2, H★, λ★, β/H★, and the full frequency table (Table 1 of the paper)
3. **Summary table** — all key numerical results with equation references

---

## Connection to the GERT Series

| Paper | Title                                   | Key result                            |
| ----- | --------------------------------------- | ------------------------------------- |
| I     | Thermodynamic ontology & Hubble tension | H₀ = 72.5 km/s/Mpc; log ρ_L2 = −23.93 |
| II    | Future boundary — metric dissolution    | α_crit = 12.88 ± 0.12                 |
| III   | Past boundary — metric emergence        | α_em = −3.0 ± 0.1; Ξ(α) = 1           |
| IV    | Internal anatomy — Gibbs Dance          | Fm peak (0.37) and FL peak (4.62)     |
| **V** | **Gravitational wave scars**            | **n_T ∈ [0,+1]; λ★ = 0.441 pc**       |

---

## Citation

If you use these scripts, please cite:

> Dutra V P (2026). *GERT V — The Cauldron's Scar: Primordial Gravitational Waves as the Frozen Thermodynamic Record of Layer 2.* Preprints 2026.
