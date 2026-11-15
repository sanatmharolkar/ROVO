# Competency Questions: Remote Operator Situation Awareness Module (ROVO-op)

Layer: S = static knowledge, R = runtime data, S+R = static definitions evaluated against runtime data.

## A. Operator, mode and engagement

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-01 | Which remote operator is responsible for vehicle V, and in which mode: remote monitoring, remote assistance or remote driving, and, for remote driving, event-based or continuous remote driving? | R | AM22, BSI1886, STVF, BR26, SHI26 |
| SA-02 | Which kinds of task does O's mode give O for V, and which of them does O hold: DDT subtasks (lateral control, longitudinal control, OEDR, DDT fallback) in remote driving, decision-making and cue interpretation (answering V's requests, e.g. classifying an object or authorizing a path) in remote assistance, or observation only in remote monitoring? | S+R | J3016, AM22 |
| SA-03 | If V requested the engagement (event-based remote driving or remote assistance), what did V request (a takeover or a kind of assistance), for what reason (e.g. sensor failure, plan failure, perception error, an object it cannot classify), and which elements is the request about? If O took over from an on-board driver, for what reason (the driver asked, or was unable to drive)? | R | MU21, TL22, AM22 |
| SA-04 | When did O's engagement with V begin, from which earlier engagement with V, if any, did O move on, how long did O's SA build-up take, and how long has O been in the maintenance phase since? | R | MU21, LU17, HA24 |
| SA-05 | How many vehicles is O responsible for at the same time? | R | ME24, STVF |
| SA-06 | In what operating environment (e.g. public road, warehouse, port, construction or mining site) and for what driving task does O operate V? | S | WO25, HN25b, LV21, BR26 |

## B. Perception

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-07 | Which situation elements around V has O perceived, when, and through which information channel? | R | EN95a, MU21b, LV21 |

## C. Information age, latency and staleness

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-08 | From which sensor frames, sensed when, was the scene currently shown to O derived? | R | MU21, TL22, GF20 |
| SA-09 | What is the information age of the scene shown to O, i.e. the time from an event in front of V's sensors to its display at the station, and is it above the maximum information age configured for O's mode (or a stricter one for O's teleoperation setup)? | S+R | GF20, MU21, AM22, NE19 |
| SA-10 | How long does O's control input take to act at V (actuator latency), which O must anticipate in addition to the information age? | R | GF20, NE19, MA25, TANG26 |
| SA-11 | Is O's perception of element E stale, i.e. has E's state changed since the moment shown in the frames O perceived it in? | R | MU21 |

## D. Maintaining SA over time

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-12 | How long has O been remote driving since O's last break of at least the configured minimum length (time without an engagement, including time fallback-ready), and does that exceed the limit configured for the mode of O's current or, if O is not driving now, most recent remote drive? | S+R | HA24, ME24, TANG26 |
| SA-13 | Which required elements in V's scene has O not rechecked within their recheck interval (SA-22), although O had perceived them before (SA lapse)? | S+R | EN95a, TANG26 |
| SA-14 | Has the information age changed since O adapted to it, by more than the limit configured for the mode? | S+R | HA24, NE19 |

## E. Information channels and cues

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-15 | Which information channels (camera views, audio, haptic or force feedback, motion feedback, map, sensor overlays) are available to O for V right now? | R | TL22, LV21 |
| SA-16 | Which cues an in-vehicle driver would have are missing for O (e.g. vestibular and acceleration cues, speed sense, road or ground inclination, engine, ambient and warning sounds, pedal feel)? | S+R | TL22, LV21, ME24, MU21, WO26, WO25 |
| SA-17 | What share of an in-vehicle driver's field of view do O's camera views cover? | S+R | AM22, TL22, ME24, WO26, WO25, HA24 |

## F. Operator state

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-18 | What is O's current workload, and is it outside the acceptable band for O's mode, or for the fallback-ready state (overload or underload)? | R | HS88, MU21, ME24 |
| SA-19 | Does operator monitoring show signs of impairment in O: fatigue, distraction or motion sickness? | R | HA24, ME24, TL22 |
| SA-20 | Is O fallback-ready (waiting to take over, not engaged with a vehicle), and since when? If O is engaged, what were O's workload and impairment when the current engagement began? | R | MU21, ME24, EN95a |

## G. SA requirements and sufficiency (reasoning outputs)

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-21 | Which SA type (operational, supervisory, decision-support) does mode M require? | S | EN95a, AM22, TANG26 |
| SA-22 | Which types of situation elements must O have perceived for SA type T (in an operating environment or for a driving task, where the requirement is limited to one; for decision-support SA, for the type of request and the elements it is about), and how recently (recheck interval)? | S | EN95a, LV21 |
| SA-23 | Is O's current SA sufficient for the SA type of O's mode, i.e. is every required element perceived within its recheck interval and not stale, and if not, which requirements are unmet? | S+R | EN95a, MU21 |
| SA-24 | Given current degradations (information age, actuator latency, workload, impairment) and V's capabilities, which modes can O still perform for V, e.g. dropping from remote driving to remote assistance, which a vehicle without an ADS does not offer? | S+R | AM22, BR26 |

## H. Evidence

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| SA-25 | What evidence supports the estimate of what O has perceived (eye fixation, SAGAT or SPAM probe answer, control input, self-report), and how reliable is it? | R | EN95b, LV21, MZ25 |

## References

Full citations for the source keys used above and in the `dct:source` annotations of `ROVO-op.ttl`, in IEEE format.

| Key | Reference |
|---|---|
| AM22 | O. Amador, M. Aramrattana, and A. Vinel, "A survey on remote operation of road vehicles," *IEEE Access*, vol. 10, pp. 130135–130154, 2022, doi: 10.1109/ACCESS.2022.3229168. |
| BR26 | L. J. Brettin, N. F. Salem, O. Hans, and M. Maurer, "Teleoperation operational design domain based on minimal risk maneuver capability," arXiv:2605.29818 (v3, Oct. 2026), submitted to *Reliab. Eng. Syst. Saf.* |
| EN95a | M. R. Endsley, "Toward a theory of situation awareness in dynamic systems," *Hum. Factors*, vol. 37, no. 1, pp. 32–64, 1995, doi: 10.1518/001872095779049543. |
| EN95b | M. R. Endsley, "Measurement of situation awareness in dynamic systems," *Hum. Factors*, vol. 37, no. 1, pp. 65–84, 1995, doi: 10.1518/001872095779049499. |
| GF20 | J.-M. Georg, J. Feiler, S. Hoffmann, and F. Diermeyer, "Sensor and actuator latency during teleoperation of automated vehicles," in *Proc. IEEE Intell. Vehicles Symp. (IV)*, 2020, pp. 760–766, doi: 10.1109/IV47402.2020.9304802. |
| HA24 | B. Hardin, P. Salvini, M. Jirotka, and L. Kunze, "How well do drivers adapt to remote operation? Learning from remote drivers with on-road experience," in *Proc. IEEE Intell. Vehicles Symp. (IV)*, 2024, pp. 23–28, doi: 10.1109/IV55156.2024.10588556. |
| HN25b | O. Hans, B. Walter, and J. Adamy, "Evaluation of remote driver performance in urban environment operational design domains," *IEEE Open J. Intell. Transp. Syst.*, vol. 6, pp. 722–737, 2025, doi: 10.1109/OJITS.2025.3574692. |
| HS88 | S. G. Hart and L. E. Staveland, "Development of NASA-TLX (Task Load Index): Results of empirical and theoretical research," in *Human Mental Workload* (Advances in Psychology, vol. 52), P. A. Hancock and N. Meshkati, Eds. Amsterdam, The Netherlands: North-Holland, 1988, pp. 139–183, doi: 10.1016/S0166-4115(08)62386-9. |
| LU17 | Z. Lu, X. Coster, and J. de Winter, "How much time do drivers need to obtain situation awareness? A laboratory-based study of automated driving," *Appl. Ergonom.*, vol. 60, pp. 293–304, Apr. 2017, doi: 10.1016/j.apergo.2016.12.003. |
| LV21 | V. Linkov and M. Vanžura, "Situation awareness measurement in remotely controlled cars," *Front. Psychol.*, vol. 12, Art. no. 592930, 2021, doi: 10.3389/fpsyg.2021.592930. |
| MA25 | C. Maag, S. Gary, N. Merkel, and A. Neukum, "Studying effects of up- and downlink latency on remote driving using teledriving simulation," in *Proc. IEEE Intell. Vehicles Symp. (IV)*, 2025, pp. 1321–1326, doi: 10.1109/IV64158.2025.11097757. |
| ME24 | A. Meir, E. Grimberg, and O. Musicant, "The human-factors' challenges of (tele)drivers of autonomous vehicles," *Ergonomics*, vol. 68, no. 6, pp. 947–967, 2025, doi: 10.1080/00140139.2024.2346552. |
| MU21 | C. Mutzenich, S. Durant, S. Helman, and P. Dalton, "Updating our understanding of situation awareness in relation to remote operators of autonomous vehicles," *Cogn. Res.: Princ. Implic.*, vol. 6, no. 1, Art. no. 9, 2021, doi: 10.1186/s41235-021-00271-8. |
| MU21b | C. Mutzenich, S. Durant, S. Helman, and P. Dalton, "Situation awareness in remote operators of autonomous vehicles: Developing a taxonomy of situation awareness in video-relays of driving scenes," *Front. Psychol.*, vol. 12, Art. no. 727500, 2021, doi: 10.3389/fpsyg.2021.727500. |
| MZ25 | B. Metz, J. Wörle, M. Metzulat, and A. Neukum, "How to assess situation awareness while driving with automation? Impact of visual attention during AD mode on measures of situation awareness," *Accid. Anal. Prev.*, vol. 220, Art. no. 108142, Sep. 2025, doi: 10.1016/j.aap.2025.108142. |
| NE19 | S. Neumeier, P. Wintersberger, A.-K. Frison, A. Becher, C. Facchi, and A. Riener, "Teleoperation: The holy grail to solve problems of automated driving? Sure, but latency matters," in *Proc. 11th Int. Conf. Automot. User Interfaces Interact. Veh. Appl. (AutomotiveUI '19)*, Utrecht, The Netherlands, 2019, pp. 186–197, doi: 10.1145/3342197.3344534. |
| SHI26 | E. Shi, M.-M. Wolf, N. Theobald, B. Abendroth, E. Wige, J. Springer, K. Hottelart, A. Schrank, T. Brandt, M. Oehl, F. Diermeyer, and L. Plum, "Towards a joint understanding of remote operation for vehicles in public road traffic," arXiv:2606.11336, Jun. 2026, doi: 10.48550/arXiv.2606.11336. |
| TANG26 | S. Tang, P. Jain, N. Deshpande, and G. Huang, "Human factors in remote driving and remote assistance: A systematic review for road transport automation," *Cogn. Technol. Work*, vol. 28, no. 3, pp. 725–743, Sep. 2026, doi: 10.1007/s10111-026-00887-0. |
| TL22 | F. Tener and J. Lanir, "Driving from a distance: Challenges and guidelines for autonomous vehicle teleoperation interfaces," in *Proc. CHI Conf. Hum. Factors Comput. Syst. (CHI '22)*, New Orleans, LA, USA, 2022, pp. 1–13, doi: 10.1145/3491102.3501827. |
| WF25 | M.-M. Wolf, N. Krauss, A. Schmidt, and F. Diermeyer, "Control center framework for teleoperation support of automated vehicles on public roads," in *Proc. IEEE Intell. Vehicles Symp. (IV)*, 2025, pp. 2538–2545, doi: 10.1109/IV64158.2025.11097634. |
| WO25 | J. Wörle, S. Mharolkar, D. Kircali, M. Raubal, and D. Wang, "Teleoperation in a cold storage warehouse: A qualitative case study on usability and acceptance of remotely controlled forklifts," in *Adjunct Proc. 4th Annu. Symp. Human-Computer Interaction for Work (CHIWORK '25 Adjunct)*, New York, NY, USA: ACM, Jun. 2025, doi: 10.1145/3707640.3731918. |
| WO26 | J. Wörle, S. Mharolkar, D. Kircali, Z. Zhou, M. Raubal, and D. Wang, "Remote driving as a mediated driving experience: Presence, spatial awareness, and driving behaviour in a teleoperation test-track study," *Comput. Hum. Behav. Rep.*, vol. 23, Art. no. 101292, Aug. 2026, doi: 10.1016/j.chbr.2026.101292. |
| ZH24 | L. Zhao, M. Nybacka, M. Aramrattana, M. Rothhämel, A. Habibovic, L. Drugge, and F. Jiang, "Remote driving of road vehicles: A survey of driving feedback, latency, support control, and real applications," *IEEE Trans. Intell. Veh.*, vol. 9, no. 10, pp. 6086–6107, Oct. 2024, doi: 10.1109/TIV.2024.3362597. |

### Standards and regulation

| Key | Reference |
|---|---|
| BSI1886 | BSI, *System aspects for remote operation of vehicles – Guide*, BSI Flex 1886 v2.0:2024-09 (v1.0: 2023-08). |
| J3016 | SAE International, *Taxonomy and Definitions for Terms Related to Driving Automation Systems for On-Road Motor Vehicles*, SAE J3016_202104, 2021. |
| STVF | Germany, *Straßenverkehr-Fernlenk-Verordnung (StVFernLV)*, in force since 1 December 2025. |
