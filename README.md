<p align="center">
  <strong>SA_LPP</strong><br />
  Benchmark instances for the Selection and Allocation of Land Parcels Problem.
</p>

<p align="center">
  <img alt="DAT instances" src="https://img.shields.io/badge/format-DAT-2f6f4e" />
  <img alt="Instances 27" src="https://img.shields.io/badge/instances-27-444444" />
</p>

<p align="center">
  <code>SA-LPP</code> | <code>Land Use</code> | <code>2OPP</code> | <code>Optimization</code>
</p>

---

`sa_lpp` contains benchmark instances for the Selection and Allocation of Land Parcels Problem. The instances support research on land parcel selection and allocation for food production in small available areas.

The associated work models SA-LPP as a variant of the two-dimensional orthogonal packing problem named Group-2OPP. This repository provides the data files, not the optimization implementation.

## Product Surface

| Area | Contract |
| --- | --- |
| Runtime | None; static benchmark files |
| Data format | Plain-text `.dat` instances |
| Data path | External MILP model or metaheuristic reads files directly |
| Storage | Git-tracked `.dat` files |
| Documentation | This README |
| Distribution | GitHub repository |

## Runtime Shape

```mermaid
flowchart LR
  researcher["Researcher"] --> repo["SA_LPP"]:::primary
  repo --> instances["27 DAT instances"]
  instances --> model["MILP or metaheuristic"]

  classDef primary fill:#2f6f4e,stroke:#173927,color:#ffffff,stroke-width:2px
```

## Responsibilities

- Preserve SA-LPP benchmark instances for reproducible experiments.
- Store size and variant information through file naming.
- Provide input data for exact methods, constructive heuristics, and metaheuristics.
- Keep solver implementation and result analysis outside the repository.

## How It Is Built

| File Pattern | Role |
| --- | --- |
| `rnd<size>_<variant>.dat` | Land parcel selection and allocation instance. |
| `README.md` | Data contract and usage notes. |

The repository includes sizes from 10 to 50, with three variants per size.

## Platform and Service Dependencies

<table>
  <tr>
    <th>Service / Object</th>
    <th>Provider</th>
    <th>Usage</th>
    <th>Purpose</th>
  </tr>
  <tr>
    <td><code>rnd*.dat</code></td>
    <td>Repository files</td>
    <td>Read by external optimization models or experiment scripts.</td>
    <td>Provides reproducible SA-LPP benchmark inputs.</td>
  </tr>
</table>

## File Structure

Each instance is a plain-text data file. The first line provides instance-level parameters, followed by numerical parcel or group data used by optimization models.

## Reference

The instances support the study "A Mixed Integer Linear Programming Model and a Metaheuristic Approach for the Selection and Allocation of Land Parcels Problem", by Alejandro Fernandez Gil, Mariam Gomez Sanchez, Carlos Castro, and Alain Perez-Alonso.

## Verification

No automated tests are defined. Recommended manual verification is to parse at least one instance per size group.

## Secret Handling

The repository contains benchmark data only and should not store private land ownership data or credentials.
