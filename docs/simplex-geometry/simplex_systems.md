# Simplex-Based System Specification

This document provides the formal specification for the n-simplex combinatorial structures that form the foundation of the Unicosmic/Cosysoc framework.

---

## Overview

Each Cosysoc System *n* is based on an (n-1)-dimensional simplex. The **terms** of the system are derived from the k-faces of that simplex. A remarkable property of this construction is that the term count for System *n* equals the (n+1)-th term of OEIS A000081 (the number of unlabeled rooted trees).

| System | Dimension | Simplex Name | Sets | Terms | A000081(n+1) |
|:------:|:---------:|:-------------|:----:|:-----:|:------------:|
| 0 | -1 | Void | 0 | 0 | 1 |
| 1 | 0 | Point (Monoid) | 1 | 1 | 1 |
| 2 | 1 | Interval | 2 | 2 | 2 |
| 3 | 2 | Triangle (Trigon) | 3 | 4 | 4 |
| 4 | 3 | Tetrahedron | 5 | 9 | 9 |
| 5 | 4 | Pentachoron (5-Cell) | 7 | 20 | 20 |

---

## System 0: The Void (-)D Simplex

**Sets**: 0 | **Terms**: 0

The void represents the state before any distinction. It contains only the root, which is the ground of all subsequent elaboration.

```
Elements:
- roots := { r0 } = { 0 }
```

---

## System 1: The Monoid 0D Simplex (Point)

**Sets**: 1 | **Terms**: 1

A single point, the first distinction from the void. This is the monadic unit.

```
Elements:
- roots := { r0 } = { 0 }
- verts := { v0 } = { (1) }
```

---

## System 2: The Interval 1D Simplex

**Sets**: 2 | **Terms**: 2

Two points connected by a single edge. The first dyadic relationship.

```
Elements:
- roots := { r0 } = { 0 }
- verts := { v0, v1 } = { (1), (2) }
- edges := { e0 } = { (1,2) }
```

---

## System 3: The Trigonal 2D Simplex (Triangle)

**Sets**: 3 | **Terms**: 4

Three vertices, three edges, and one triangular face. The first triadic structure.

```
Elements:
- roots := { r0 } = { 0 }
- verts := { v0, v1, v2 } = { (1), (2), (3) }
- edges := { e0, e1, e2 } = { (1,2), (1,3), (2,3) }
- faces := { f0 } = { (1,2,3) }
```

---

## System 4: The Tetrahedron 3D Simplex

**Sets**: 5 | **Terms**: 9

Four vertices, six edges, four triangular faces, and one tetrahedral cell. This structure maps directly to the 9-position Enneagram and the 9 digital roots of Vortex-Based Mathematics.

```
Elements:
- roots := { r0 } = { 0 }
- verts := { v0, v1, v2, v3 } = { (1), (2), (3), (4) }
- edges := { e0, e1, e2, e3, e4, e5 } = { (1,2), (1,3), (1,4), (2,3), (2,4), (3,4) }
- faces := { f0, f1, f2, f3 } = { (1,2,3), (1,2,4), (1,3,4), (2,3,4) }
- cells := { c0 } = { (1,2,3,4) }
```

### VBM Mapping for System 4

The 6 edges of the tetrahedron form 3 pairs of opposite, mutually orthogonal edges. These map to the 3 polar pairs of VBM:

| Polar Pair | VBM Sum | Tetrahedron Edges | Cosysoc Dimension |
|:----------:|:-------:|:-----------------:|:-----------------:|
| 1-8 | 9 | (1,2) ↔ (3,4) | Performance [S-M] |
| 2-7 | 9 | (1,3) ↔ (2,4) | Potential [D-T] |
| 4-5 | 9 | (1,4) ↔ (2,3) | Commitment [P-O] |

---

## System 5: The Pentachoron 4D Simplex (5-Cell)

**Sets**: 7 | **Terms**: 20

Five vertices, ten edges, ten triangular faces, five tetrahedral cells, and one 4D hypercell. This is the first system to extend into a higher dimension.

```
Elements:
- roots := { r0 } = { 0 }
- verts := { v0, v1, v2, v3, v4 } = { (1), (2), (3), (4), (5) }
- edges := { e0, e1, e2, e3, e4, e5, e6, e7, e8, e9 }
        = { (1,2), (1,3), (1,4), (1,5), (2,3), (2,4), (2,5), (3,4), (3,5), (4,5) }
- faces := { f0, f1, f2, f3, f4, f5, f6, f7, f8, f9 }
        = { (1,2,3), (1,2,4), (1,2,5), (1,3,4), (1,3,5), (1,4,5), (2,3,4), (2,3,5), (2,4,5), (3,4,5) }
- cells := { c0, c1, c2, c3, c4 }
        = { (1,2,3,4), (1,2,3,5), (1,2,4,5), (1,3,4,5), (2,3,4,5) }
- hypes := { h0 } = { (1,2,3,4,5) }
```

### Structural Properties of System 5

The 5 tetrahedral cells of the pentachoron represent all possible "views" of the system with one vertex (service) suppressed. Each cell is a complete System 4 structure.

| Cell | Vertices | Excluded Vertex |
|:----:|:--------:|:---------------:|
| c0 | (1,2,3,4) | v4 (5) |
| c1 | (1,2,3,5) | v3 (4) |
| c2 | (1,2,4,5) | v2 (3) |
| c3 | (1,3,4,5) | v1 (2) |
| c4 | (2,3,4,5) | v0 (1) |

---

## General Formula

For an (n-1)-simplex (System *n*), the number of k-faces is given by the binomial coefficient:

```
Number of k-faces = C(n, k+1)
```

The total number of elements (excluding the root) is `2^n - 1`.

The **term count** for System *n* is `A000081(n+1)`.
