# Competency Questions: Communication Link Module (RDOnto-link)

Layer: S = static knowledge, R = runtime data, S+R = static definitions evaluated against runtime data.

## A. Session

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| LK-01 | Which teleoperation session connects operator O's station to vehicle V, since when, which engagement of `RDOnto-op` (mode) does it currently carry, and, after an operator handover at the same or another station, which session does it follow? | R | GA21b, MA25, BR26 |
| LK-02 | Which streams does the session carry (sensor and video feeds and proposed trajectories from V to O, control commands and trajectory input from O to V), and which of them does the current mode depend on? | S+R | GA23, NE19b, FE26 |

## B. Latency and its effect on driving

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| LK-03 | What is the current end-to-end latency, and how much of it is sensor (glass-to-glass) latency and how much actuator latency (from O's command to the actuator response at V)? | R | GF20, ZH24, MA25 |
| LK-04 | Is the end-to-end latency acceptable for the current setup, mode and speed, i.e. is the distance travelled during the latency within the setup's tolerance (or within the setup's reference budgets, where it has them), and which source sets the limit? | S+R | GA21b, NE19b, NE19, SC22 |
| LK-05 | How stable is the latency: how much has it varied over the recent window, what share of video frames or commands missed their deadline, has it changed since the session began, and does its variation exceed the limit configured for the mode? | R | NE19b, NE19, FE26, JI25 |
| LK-06 | Is the available data rate from V to the station enough for the camera views the operator currently needs? | R | NE19b, SH21, FE26 |

## C. Connection loss and prediction

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| LK-07 | Has the connection been lost (no data, for longer than the configured timeout, on a continuously sent stream that the mode needs), since when (the last data), when was the loss detected, and which minimal risk manoeuvre has V started? | S+R | BR26, KO21, NE19b |
| LK-08 | What link quality is predicted for the coming horizon or along the planned route, from which source, and does the warning come early enough for V to react at its current speed? | R | KO21, BZ21, GA23, SC22 |

## D. Adaptation (reasoning outputs)

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| LK-09 | What is the highest speed at which V can still be driven remotely in its setup, given the current and predicted latency (travel tolerance divided by latency, or the setup's reference budgets)? | S+R | GA21b, JI25, KO21, NE19b |
| LK-10 | Which adaptations are available for the current or predicted degradation (latency over budget, unstable latency, insufficient data rate, connection loss): lower video quality or fewer camera views, reduce speed, reroute, switch from remote driving to remote assistance, hand back to the ADS where it is within its ODD and able to drive, hand back to the on-board driver where that driver can take over, let the ADS continue without the operator, stop; and which is recommended? | S+R | GA23, GA21b, NE19b, SH21, BR26 |

## E. Interface to the operator

| ID | Competency question | Layer | Sources |
| --- | --- | --- | --- |
| LK-11 | Is O being shown the current link state (latency level, predicted degradation)? | R | NE19, GA23 |
| LK-12 | Does the sensor latency measured for the link agree with the information age `RDOnto-op` computes for the scene currently shown to O (SA-09), and if not, by how much do they differ? | R | GF20, GA21b, FE26 |

## References

Full citations for the source keys used above and in the `dct:source` annotations of `RDOnto-link.ttl`, in IEEE format.

| Key | Reference |
|---|---|
| BR26 | L. J. Brettin, N. F. Salem, O. Hans, and M. Maurer, "Teleoperation operational design domain based on minimal risk maneuver capability," arXiv:2605.29818 (v3, Oct. 2026), submitted to *Reliab. Eng. Syst. Saf.* |
| BZ21 | M. Boban, M. Giordani, and M. Zorzi, "Predictive quality of service: The next frontier for fully autonomous systems," *IEEE Netw.*, vol. 35, no. 6, pp. 104–110, Nov. 2021, doi: 10.1109/MNET.001.2100237. |
| FE26 | R. A. K. Fezeu, J. Carpenter, R. Zende, S. G. L. Divakarla, N. Varyani, F. Bilal, S. Sleder, N. Naik, D. Joly, E. Ramadan, A. K. Gurumadaiah, and Z.-L. Zhang, "Teleoperating autonomous vehicles over commercial 5G networks: Are we there yet?," *IEEE Trans. Netw.*, vol. 34, pp. 4913–4928, 2026, doi: 10.1109/TON.2026.3686751. |
| GA21b | 5GAA, "Tele-operated driving (ToD): System requirements analysis and architecture," 5G Automotive Association, Tech. Rep. (ToD XWI deliverable D2), Version 1.02, Sep. 2021. [Online]. Available: https://5gaa.org/content/uploads/2021/09/5GAA_ToD_System_Requirements_Architecture_TR.pdf |
| GA23 | 5GAA, "Predictive QoS and V2X service adaptation (PRESA)," 5G Automotive Association, Tech. Rep., Version 2, Jan. 2023. [Online]. Available: https://5gaa.org/content/uploads/2023/01/5gaa-wi-presa-tr-predictive-qos-and-v2x-service-adaptation.pdf |
| GF20 | J.-M. Georg, J. Feiler, S. Hoffmann, and F. Diermeyer, "Sensor and actuator latency during teleoperation of automated vehicles," in *Proc. IEEE Intell. Vehicles Symp. (IV)*, 2020, pp. 760–766, doi: 10.1109/IV47402.2020.9304802. |
| JI25 | X. A. Ji, S. S. Avedisov, M. I. Khan, I. Vörös, O. Altintas, and G. Orosz, "On the effects of latency in teleoperated driving: Stability and performance analysis," *Veh. Syst. Dyn.*, vol. 64, no. 11, pp. 2742–2764, 2026 (online Jul. 2025), doi: 10.1080/00423114.2025.2537409. |
| KO21 | A. Kousaridas, R. P. Manjunath, J. Perdomo, C. Zhou, E. Zielinski, S. Schmitz, and A. Pfadler, "QoS prediction for 5G connected and automated driving," *IEEE Commun. Mag.*, vol. 59, no. 9, pp. 58–64, Sep. 2021, doi: 10.1109/MCOM.110.2100042. |
| MA25 | C. Maag, S. Gary, N. Merkel, and A. Neukum, "Studying effects of up- and downlink latency on remote driving using teledriving simulation," in *Proc. IEEE Intell. Vehicles Symp. (IV)*, 2025, pp. 1321–1326, doi: 10.1109/IV64158.2025.11097757. |
| NE19 | S. Neumeier, P. Wintersberger, A.-K. Frison, A. Becher, C. Facchi, and A. Riener, "Teleoperation: The holy grail to solve problems of automated driving? Sure, but latency matters," in *Proc. 11th Int. Conf. Automot. User Interfaces Interact. Veh. Appl. (AutomotiveUI '19)*, Utrecht, The Netherlands, 2019, pp. 186–197, doi: 10.1145/3342197.3344534. |
| NE19b | S. Neumeier, E. A. Walelgne, V. Bajpai, J. Ott, and C. Facchi, "Measuring the feasibility of teleoperated driving in mobile networks," in *Proc. Netw. Traffic Meas. Anal. Conf. (TMA)*, Paris, France, 2019, pp. 113–120, doi: 10.23919/TMA.2019.8784466. |
| SC22 | H. Schippers, C. Schüler, B. Sliwa, and C. Wietfeld, "System modeling and performance evaluation of predictive QoS for future tele-operated driving," in *Proc. IEEE Int. Syst. Conf. (SysCon)*, 2022, pp. 1–8, doi: 10.1109/SysCon53536.2022.9773810. |
| SH21 | A. Schimpe, S. Hoffmann, and F. Diermeyer, "Adaptive video configuration and bitrate allocation for teleoperated vehicles," in *Proc. IEEE Intell. Vehicles Symp. Workshops (IV Workshops)*, 2021, pp. 148–153, doi: 10.1109/IVWorkshops54471.2021.9669258. |
| ZH24 | L. Zhao, M. Nybacka, M. Aramrattana, M. Rothhämel, A. Habibovic, L. Drugge, and F. Jiang, "Remote driving of road vehicles: A survey of driving feedback, latency, support control, and real applications," *IEEE Trans. Intell. Veh.*, vol. 9, no. 10, pp. 6086–6107, Oct. 2024, doi: 10.1109/TIV.2024.3362597. |
