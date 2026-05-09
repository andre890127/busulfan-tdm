# Busulfan TDM q24h – AUC Calculator

Clinical pharmacokinetic calculator for therapeutic drug monitoring (TDM) of intravenous busulfan in once-daily (q24h) regimens.

## Live Demo

[https://andre890127.github.io/busulfan-tdm/](https://andre890127.github.io/busulfan-tdm/)

---

## Features

- Trapezoidal AUC calculation
- Terminal phase extrapolation (AUC∞)
- Automatic conversion to µM·min
- Elimination half-life estimation
- R² terminal fit evaluation
- Interactive concentration–time curve
- Dose adjustment suggestion based on linear proportionality
- Responsive interface
- Pure HTML/CSS/JavaScript
- No backend required

---

## Pharmacokinetic Methods

The calculator performs:

- Linear trapezoidal integration
- Terminal elimination slope estimation using log-linear regression
- AUC extrapolation:
  
  ```text
  AUCtail = Clast / λz
  ```

- Half-life estimation:
  
  ```text
  t½ = ln(2) / λz
  ```

- Conversion from mcg·min/mL to µM·min using busulfan molecular weight:
  
  ```text
  MW = 246.3 g/mol
  ```

---

## Sampling Schedule

Default concentration sampling times:

```text
0, 30, 60, 90, 120, 180, 240, 300, 360, 420, 480 min
```

---

## Therapeutic Targets (q24h)

| AUC (µM·min) | Interpretation |
|---|---|
| < 4000 | Underexposure |
| 4000–6000 | Therapeutic target |
| 6000–7000 | Toxicity warning zone |
| > 7000 | High toxicity risk |

---

## References

- Domingos V et al. *A practical guide to therapeutic drug monitoring in busulfan: recommendations from the Pharmacist Committee of the European Society for Blood and Marrow Transplantation (EBMT).* Bone Marrow Transplant. 2024;59(12):1641–1653.
- Russell JA et al. Busulfan pharmacokinetics and exposure targets in hematopoietic stem cell transplantation.

---

## Disclaimer

This tool is intended for clinical decision support only and does not replace physician judgment, institutional protocols, or pharmacist review.

All dose adjustments must be validated by qualified healthcare professionals.

---

## License

MIT License
