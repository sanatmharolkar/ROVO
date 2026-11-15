# R.O.V.O: Remote Operation of Vehicles Ontology

R.O.V.O is an ontology of the remote driving (road vehicle teleoperation) context. It describes the remote operator's situation awareness and the communication link between the vehicle and the remote station. Version 1.0.

## Modules

| Module | IRI | File | Content |
|---|---|---|---|
| <a id="op"></a>Operator awareness | `https://w3id.org/rovo/op` | [ROVO-op.ttl](ROVO-op.ttl) | What information is available to the remote operator, what the operator has perceived from it, how delayed it is, and whether it is sufficient for the operator's mode |
| <a id="link"></a>Communication link | `https://w3id.org/rovo/link` | [ROVO-link.ttl](ROVO-link.ttl) | Sessions, end-to-end latency and its parts, latency limits per setup, connection loss, predictions, admissible speed and adaptations |
| <a id="core"></a>Upper alignment | `https://w3id.org/rovo/core` | [ROVO-core.ttl](ROVO-core.ttl) | Alignments with EDMC AUTO (SAE J3016) and A.U.T.O. |
| <a id="op-shapes"></a>Operator awareness shapes | `https://w3id.org/rovo/op-shapes` | [ROVO-op-shapes.ttl](ROVO-op-shapes.ttl) | SHACL shapes for `ROVO-op` data |
| <a id="link-shapes"></a>Communication link shapes | `https://w3id.org/rovo/link-shapes` | [ROVO-link-shapes.ttl](ROVO-link-shapes.ttl) | SHACL shapes for `ROVO-link` data |

`ROVO-link` and `ROVO-core` import `ROVO-op`. All modules stay within the OWL 2 RL profile.

## Documentation

Each module has a page that lists its classes, properties and individuals with their definitions:

- [Operator awareness module](docs/op/index-en.html), with its competency questions and references
- [Communication link module](docs/link/index-en.html), with its competency questions and references
- [Upper alignment module](docs/core/index-en.html)

To rebuild the pages after a change to a Turtle file or a competency-question file, run [docs/make_docs.py](docs/make_docs.py).

## Competency questions

Each module answers a list of competency questions, which also resolve the source keys used in the ontology files:

- [Operator awareness](competency-questions/remote-operator-sa-cqs.md): SA-01 to SA-25
- [Communication link](competency-questions/communication-link-cqs.md): LK-01 to LK-12

## Use

Each IRI above returns the Turtle file to RDF clients. `https://w3id.org/rovo/{core,op,link,op-shapes,link-shapes}.ttl` always returns the Turtle file.

To work on a local copy without fetching the imports, open the files with [catalog-v001.xml](catalog-v001.xml) in the same folder (read by Protégé and other tools that support OASIS XML catalogs).

## License

[Apache License 2.0](LICENSE). Creator: Sanat Mharolkar (Nanyang Technological University, Singapore).
