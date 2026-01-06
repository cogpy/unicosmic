# Unicosmic (o9nn)

**Unified Cosmic Order System - A framework integrating simplex geometry, Vortex-Based Mathematics, and Monster Group theory.**

---

## Overview

This repository hosts the **Unicosmic** project, an evolution of the `o9nn/cosysoc` framework. It aims to formalize and extend the Cosmic Order System by grounding it in a rigorous, cross-validated mathematical foundation. The core of this framework is a profound duality between the geometric structure of **n-simplices** and the combinatorial enumeration of **unlabeled rooted trees (OEIS A000081)**.

This synthesis reveals that the Cosysoc architecture, Vortex-Based Mathematics (VBM), and the structure of the Monster Group are different expressions of a single, underlying mathematical reality. This repository contains the research, documentation, and eventual implementation of this unified model.

## Core Principles

1.  **The Simplex-A000081 Duality**: The term count for Cosysoc System *n*, which is based on an (n-1)-dimensional simplex, is precisely equal to the (n+1)-th term of the integer sequence OEIS A000081. This duality is the core generative principle of the system.

2.  **Geometric Grounding of VBM**: The dynamics of Vortex-Based Mathematics (the doubling circuit and polar pairs) are mapped directly onto the geometric elements (vertices, edges, faces) of the n-simplex at each system level.

3.  **Monster Group as a Dimensional Blueprint**: The prime exponent signature of the Monster Group, which also follows the A000081 sequence, provides a non-arbitrary, 15-level dimensional roadmap for the simplex hierarchy.

## The Simplex-Based System Architecture

The Unicosmic framework is built upon the combinatorial structure of n-simplices. Each system level corresponds to an (n-1)-dimensional simplex, and its terms are derived from the k-faces of that simplex.

---

### System 0 ( 0 Sets | 0 Terms ): The Void (-)D Simplex
- **1 root** := `{ r0 } = { 0 }`

### System 1 ( 1 Set | 1 Term ): The Monoid 0D Simplex (Point)
- **1 root** := `{ r0 } = { 0 }`
- **1 vert** := `{ v0 } = { (1) }`

### System 2 ( 2 Sets | 2 Terms ): The Interval 1D Simplex
- **1 root** := `{ r0 } = { 0 }`
- **2 verts** := `{ v0, v1 } = { (1), (2) }`
- **1 edge** := `{ e0 } = { (1,2) }`

### System 3 ( 3 Sets | 4 Terms ): The Trigonal 2D Simplex (Triangle)
- **1 root** := `{ r0 } = { 0 }`
- **3 verts** := `{ v0, v1, v2 } = { (1), (2), (3) }`
- **3 edges** := `{ e0, e1, e2 } = { (1,2), (1,3), (2,3) }`
- **1 face** := `{ f0 } = { (1,2,3) }`

### System 4 ( 5 Sets | 9 Terms ): The Tetrahedron 3D Simplex
- **1 root** := `{ r0 } = { 0 }`
- **4 verts** := `{ v0, v1, v2, v3 } = { (1), (2), (3), (4) }`
- **6 edges** := `{ e0, e1, e2, e3, e4, e5 } = { (1,2), (1,3), (1,4), (2,3), (2,4), (3,4) }`
- **4 faces** := `{ f0, f1, f2, f3 } = { (1,2,3), (1,2,4), (1,3,4), (2,3,4) }`
- **1 cell** := `{ c0 } = { (1,2,3,4) }`

### System 5 ( 7 Sets | 20 Terms ): The Pentachoron 4D Simplex (5-Cell)
- **1 root** := `{ r0 } = { 0 }`
- **5 verts** := `{ v0, v1, v2, v3, v4 } = { (1), (2), (3), (4), (5) }`
- **10 edges** := `{ e0..e9 } = { (1,2), (1,3), (1,4), (1,5), (2,3), (2,4), (2,5), (3,4), (3,5), (4,5) }`
- **10 faces** := `{ f0..f9 } = { (1,2,3), (1,2,4), (1,2,5), (1,3,4), (1,3,5), (1,4,5), (2,3,4), (2,3,5), (2,4,5), (3,4,5) }`
- **5 cells** := `{ c0..c4 } = { (1,2,3,4), (1,2,3,5), (1,2,4,5), (1,3,4,5), (2,3,4,5) }`
- **1 hype(rcell)** := `{ h0 } = { (1,2,3,4,5) }`

---

## Documentation

Further documentation and the complete relevance study can be found in the `/docs` directory.

- **`/docs/relevance-study`**: Contains the comprehensive analysis of the connections between Cosysoc, VBM, and Monster Group theory.
- **`/docs/simplex-geometry`**: Contains detailed breakdowns of the n-simplex combinatorial structures.

## Source Code

The source code for the `o9nn` kernel and related tools will be located in the `/src` directory.
