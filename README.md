# RDOnto: Remote Driving Ontology

RDOnto is an ontology of the remote driving (road vehicle teleoperation) context. It describes the remote operator's situation awareness and the communication link between the vehicle and the remote station. Version 1.0.

## Modules

| Module | IRI | File | Content |
|---|---|---|---|
| <a id="op"></a>Operator awareness | `https://w3id.org/rdonto/op` | [RDOnto-op.ttl](RDOnto-op.ttl) | What information is available to the remote operator, what the operator has perceived from it, how delayed it is, and whether it is sufficient for the operator's mode |
| <a id="link"></a>Communication link | `https://w3id.org/rdonto/link` | [RDOnto-link.ttl](RDOnto-link.ttl) | Sessions, end-to-end latency and its parts, latency limits per setup, connection loss, predictions, admissible speed and adaptations |
| <a id="core"></a>Upper alignment | `https://w3id.org/rdonto/core` | [RDOnto-core.ttl](RDOnto-core.ttl) | Alignments with EDMC AUTO (SAE J3016) and A.U.T.O. |
| <a id="op-shapes"></a>Operator awareness shapes | `https://w3id.org/rdonto/op-shapes` | [RDOnto-op-shapes.ttl](RDOnto-op-shapes.ttl) | SHACL shapes for `RDOnto-op` data |
| <a id="link-shapes"></a>Communication link shapes | `https://w3id.org/rdonto/link-shapes` | [RDOnto-link-shapes.ttl](RDOnto-link-shapes.ttl) | SHACL shapes for `RDOnto-link` data |

`RDOnto-link` and `RDOnto-core` import `RDOnto-op`. All modules stay within the OWL 2 RL profile.

## Competency questions

Each module answers a list of competency questions, which also resolve the source keys used in the ontology files:

- [Operator awareness](competency-questions/remote-operator-sa-cqs.md): SA-01 to SA-25
- [Communication link](competency-questions/communication-link-cqs.md): LK-01 to LK-12

## Use

Each IRI above returns the Turtle file to RDF clients. `https://w3id.org/rdonto/{core,op,link,op-shapes,link-shapes}.ttl` always returns the Turtle file.

To work on a local copy without fetching the imports, open the files with [catalog-v001.xml](catalog-v001.xml) in the same folder (read by Protégé and other tools that support OASIS XML catalogs).

## License

[Apache License 2.0](LICENSE). Creator: Sanat Mharolkar (Nanyang Technological University, Singapore).
