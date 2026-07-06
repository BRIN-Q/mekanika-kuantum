# AI Agent Prompt: Generate a Computational Quantum Mechanics Jupyter Notebook

## Role

You are an expert in **Quantum Mechanics**, **Dirac notation**, **linear algebra**, **scientific computing**, and **Python programming**. Your task is to create a complete **Jupyter Notebook (`.ipynb`)** based on the lecture module provided in **`FILE.pdf`**.

The notebook should not merely summarize the lecture. Instead, it should serve as an **interactive computational companion** that reconstructs every important mathematical derivation, explains each step in detail, and verifies the results numerically using Python.

Use **`file.ipynb`** as the reference for notebook organization, Markdown formatting, explanation style, and code structure.

---

# Objective

Create a fully executable Jupyter Notebook that systematically reconstructs every important concept contained in `FILE.pdf` using:

- Dirac notation
- Matrix mechanics
- Linear algebra
- Numerical verification with Python
- Visualizations whenever appropriate

The notebook should be suitable for undergraduate students studying quantum mechanics and should bridge the gap between abstract mathematics and computational implementation.

---

# Expected Notebook Structure

Organize the notebook according to the subsection structure of the lecture module.

Each subsection should follow the workflow below.

---

# 1. Section Title

Create a Markdown heading using exactly the same subsection title as in the lecture module.

Example

```markdown
# 2.3 Jones Matrix Representation
```

---

# 2. Rewrite the Original Equations

Rewrite every important equation from the lecture module.

Requirements:

- Preserve the original notation.
- Use proper LaTeX formatting.
- Maintain the original equation numbering whenever possible.
- Include all intermediate equations.
- Preserve the logical derivation order.

Do **not** skip equations, even if they appear trivial.

---

# 3. Conceptual Explanation

Before beginning the derivation, explain:

- What the equation represents.
- Why it is important.
- The physical interpretation.
- Any assumptions involved.
- The connection to previous equations.

The explanation should be concise but mathematically rigorous.

---

# 4. Matrix-Based Proof (Most Important Section)

Re-derive every equation entirely using matrix mechanics.

Do **NOT** simply copy the derivation from the lecture notes.

Instead:

- Convert every ket into its column vector.
- Convert every bra into its row vector.
- Convert every operator into its matrix representation.
- Show every matrix multiplication explicitly.
- Show every intermediate calculation.
- Never jump directly to the final answer.

Whenever Dirac notation appears, always provide the equivalent matrix representation.

For example,

Instead of writing

\[
|H\rangle\langle H|\psi\rangle
\]

write

\[
|H\rangle=
\begin{bmatrix}
1\\
0
\end{bmatrix}
\]

\[
\langle H|=
\begin{bmatrix}
1&0
\end{bmatrix}
\]

\[
|H\rangle\langle H|=
\begin{bmatrix}
1&0\\
0&0
\end{bmatrix}
\]

Then explicitly perform

\[
\begin{bmatrix}
1&0\\
0&0
\end{bmatrix}
\begin{bmatrix}
a\\
b
\end{bmatrix}
=
\begin{bmatrix}
a\\
0
\end{bmatrix}
\]

Never omit intermediate calculations.

Every mathematical step should be visible.

---

# 5. Connect the Matrix Proof to Dirac Notation

After completing the matrix derivation, explain how each matrix operation corresponds to Dirac notation.

Discuss concepts such as:

- Inner products
- Outer products
- Projection operators
- Identity operator
- Basis vectors
- Basis transformations
- Expectation values
- Eigenvalue equations

Demonstrate that the matrix derivation is mathematically equivalent to the original Dirac notation.

---

# 6. Numerical Verification with Python

After every important derivation, create Python code that numerically verifies the result.

Requirements:

Use

```python
import numpy as np
```

Avoid symbolic computation unless absolutely necessary.

Each code block should:

- Define basis vectors.
- Define operators.
- Perform the required matrix operations.
- Print intermediate matrices.
- Print final results.
- Verify analytical identities using

```python
np.allclose(...)
```

Whenever appropriate, also compute:

- Eigenvalues
- Eigenvectors
- Probabilities
- Projection results
- Expectation values
- Measurement outcomes

Code should be clean, readable, and well-commented.

---

# 7. Interpretation of Numerical Results

After every code cell, explain:

- What the numerical output demonstrates.
- Why it agrees with the mathematical proof.
- The physical meaning of the result.

Avoid merely repeating the printed numbers.

---

# 8. Visualizations (Whenever Appropriate)

Whenever a concept benefits from visualization, include plots such as:

- State vectors
- Polarization vectors
- Jones vector diagrams
- Matrix heatmaps
- Probability distributions
- Rotation transformations
- Bloch sphere (if applicable)

Use

```python
import matplotlib.pyplot as plt
```

Plots should include:

- Titles
- Axis labels
- Legends (when appropriate)

Keep visualizations simple and educational.

---

# Mathematical Topics to Cover

Whenever these topics appear in the lecture module, derive them completely using both Dirac notation and matrix mechanics.

Examples include:

- Dirac notation
- Bra-ket algebra
- Inner products
- Outer products
- Projection operators
- Identity operator
- Orthonormal basis
- Completeness relation
- Matrix representation of operators
- Hermitian operators
- Unitary operators
- Eigenvalues
- Eigenvectors
- Measurement postulate
- Expectation values
- Probability amplitudes
- Polarization states
- Jones vectors
- Jones matrices
- Rotation matrices
- Change of basis
- Operator algebra

---

# Notebook Style

Alternate between Markdown cells and Python code cells.

A typical section should look like:

1. Markdown — Section title
2. Markdown — Original equations
3. Markdown — Conceptual explanation
4. Markdown — Matrix derivation
5. Python — Numerical verification
6. Markdown — Interpretation
7. Python — Visualization (optional)
8. Markdown — Summary

The notebook should read like an interactive textbook.

---

# Level of Detail

Assume the reader is encountering the material for the first time.

Therefore:

- Never skip algebraic steps.
- Never assume a result is obvious.
- Explain why each mathematical manipulation is valid.
- Clearly distinguish between mathematical identities and physical interpretations.

The notebook should be significantly more detailed than the original lecture notes.

---

# Code Quality Requirements

All Python code must:

- Run from top to bottom without modification.
- Follow clean coding practices.
- Use descriptive variable names.
- Include comments explaining each step.
- Avoid unnecessary complexity.
- Be easy for students to understand.

---

# Markdown Quality Requirements

All Markdown should:

- Use proper LaTeX for equations.
- Include explanatory text.
- Organize information with headings and subheadings.
- Be easy to read.
- Maintain consistent formatting throughout the notebook.

---

# Reference Notebook

Use `file.ipynb` as a template for:

- Notebook organization
- Markdown formatting
- Writing style
- Code style
- Explanation quality

However, expand upon the reference whenever additional explanation would improve understanding.

---

# Final Deliverable

Produce a single, fully executable **Jupyter Notebook (`.ipynb`)** that:

- Covers every subsection of `FILE.pdf`.
- Rewrites all important equations in LaTeX.
- Reconstructs every derivation using explicit matrix mechanics.
- Explains every mathematical step.
- Connects matrix operations with Dirac notation.
- Includes numerical verification using Python after every major derivation.
- Includes visualizations whenever appropriate.
- Is educational, rigorous, and suitable as a computational companion to the lecture module.
- Requires no manual modifications before execution.