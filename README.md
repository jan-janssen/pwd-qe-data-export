# Python Workflow Definition - Quantum Espresso - Data Export
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jan-janssen/pwd-qe-data-export/HEAD)

Extending the `JSON` format to support output and working directory. 

Run two Jupyter notebooks:
- [`create_workflow.ipynb`](create_workflow.ipynb) - define workflow in pyiron and export to Python Workflow Definition
- [`run_workflow.ipynb`](run_workflow.ipynb) - run the workflow with pyiron and store the output in modified Python Workflow Definition

Previously each node was stored as:
```json
{
    "id": 5,
    "type": "function",
    "value": "workflow.calculate_qe"
},
```

Updated with `output` and `working_directory`:
```json
{
    "id": 5,
    "type": "function",
    "value": "workflow.calculate_qe",
    "output": {
        "structure": "{\"immutable_id\": null, \"last_modified\": null, \"elements\": [\"Al\"], \"nelements\": 1, \"elements_ratios\": [1.0], \"chemical_formula_descriptive\": \"Al4\", \"chemical_formula_reduced\": \"Al\", \"chemical_formula_hill\": null, \"chemical_formula_anonymous\": \"A\", \"dimension_types\": [1, 1, 1], \"nperiodic_dimensions\": 3, \"lattice_vectors\": [[4.0451141729882245, 0.0, 0.0], [0.0, 4.0451141729882245, 0.0], [0.0, 0.0, 4.0451141729882245]], \"space_group_symmetry_operations_xyz\": null, \"space_group_symbol_hall\": null, \"space_group_symbol_hermann_mauguin\": null, \"space_group_symbol_hermann_mauguin_extended\": null, \"space_group_it_number\": null, \"cartesian_site_positions\": [[0.0, 0.0, 0.0], [0.0, 2.022557086494112, 2.022557086494112], [2.022557086494112, 0.0, 2.022557086494112], [2.022557086494112, 2.022557086494112, 0.0]], \"nsites\": 4, \"species\": [{\"name\": \"Al\", \"chemical_symbols\": [\"Al\"], \"concentration\": [1.0], \"mass\": null, \"original_name\": null, \"attached\": null, \"nattached\": null}], \"species_at_sites\": [\"Al\", \"Al\", \"Al\", \"Al\"], \"assemblies\": null, \"structure_features\": []}",
        "energy": -1074.9365273079682,
        "volume": 66.18999558704988
    },
    "working_directory": "/home/jovyan/calculate_qe_8649213786bf31b0c67e1cc4640b5cee_hdf5/calculate_qe_8649213786bf31b0c67e1cc4640b5cee"
},
```
