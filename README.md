# SA-LPP Instances

This repository contains benchmark instances for the Selection and Allocation of Land Parcels Problem (SA-LPP).

The instances support the study "A Mixed Integer Linear Programming Model and a Metaheuristic Approach for the Selection and Allocation of Land Parcels Problem", by Alejandro Fernandez Gil, Mariam Gomez Sanchez, Carlos Castro, and Alain Perez-Alonso.

## Problem Context

SA-LPP addresses the selection and allocation of land parcels for food production in small available areas. The problem is motivated by land-use planning, agricultural logistics, and the reduction of transportation-related environmental impact.

The associated work models SA-LPP as a variant of the two-dimensional orthogonal packing problem, named Group-2OPP, and evaluates both mathematical programming and metaheuristic approaches.

## Contents

The repository includes 27 `.dat` instances:

- Sizes from 10 to 50.
- Three variants per size.
- Filenames follow the pattern `rnd<size>_<variant>.dat`.

## File Structure

Each instance is a plain-text data file containing numerical parameters for land parcel selection and allocation. The first line provides instance-level parameters, followed by parcel or group data used by optimization models.

## Suggested Use

These files are intended for computational experiments with exact optimization models, constructive heuristics, and metaheuristics for land parcel selection and allocation.
