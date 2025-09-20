# SpeakerBeam-VC: Noise-Robust Voice Conversion with Speaker Enrollment — Demos   <!-- omit in toc -->
Authors: Hiroki Kanagawa, Yusuke Ijima, Kenichi Fujita, Takafumi Moriya, Taichi Asami  
Affiliation: NTT, Inc., Japan


# Comparison VCs

<style>
/* --- Responsive table wrapper --- */
.table-scroll {
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  margin: 1em 0;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
}

/* --- Base table styles --- */
table.comp {
  border-collapse: collapse;
  font-size: 0.95rem;
  width: 100%;
  min-width: 720px; /* allow horizontal scroll on small screens */
}
table.comp th, table.comp td {
  border: 1px solid #ddd;
  padding: 8px 10px;
  text-align: left; /* ← 左寄せに変更 */
  white-space: nowrap;
}
table.comp th {
  background: #f4f4f4;
  position: sticky;
  top: 0;
  z-index: 1;
}
table.comp tr.ours {
  background: #fff9e6; /* Highlight our method in pale yellow */
  font-weight: 600;
}

/* --- Small-screen tweaks --- */
@media (max-width: 640px) {
  table.comp { font-size: 0.9rem; }
  table.comp th, table.comp td { padding: 6px 8px; }
}
</style>

<div class="table-scroll">
<table class="comp">
  <thead>
    <tr>
      <th>System</th>
      <th>Speech enhancement <br>(SE) Preprocessing</th>
      <th>Speaker Enrollment</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>VanillaVC</td>
      <td>✘</td>
      <td>✘</td>
      <td>Standard VC without SE or enrollment.</td>
    </tr>
    <tr>
      <td>SE+VC</td>
      <td>✔︎</td>
      <td>✘</td>
      <td>VC with speech enhancement applied as preprocessing.</td>
    </tr>
    <tr class="ours">
      <td>SpkBeamVC (ours)</td>
      <td>✘</td>
      <td>✔︎</td>
      <td>Proposed SpeakerBeam-VC: Noise-robust VC with speaker enrollment.</td>
    </tr>
    <tr>
      <td>SE+SpkBeamVC</td>
      <td>✔︎</td>
      <td>✔︎</td>
      <td>Proposed variant: SE preprocessing combined with enrollment.</td>
    </tr>
  </tbody>
</table>
</div>


# Speech samples
If you are having trouble listening to the audios, try refreshing the page.  
All source and target speaker pairs are chosen from unseen test data.  
Each audio sample is spoken in Japanese with the utterance “ずいぶんの情熱とエネルギーをもって勉強され研究された.” (in English as “It was studied and researched with considerable passion and energy.”)

## Female-to-Female

| SNR | Mode | VanillaVC | SE+VC | SpkBeamVC | SE+SpkBeamVC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| inf | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| inf | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| 20 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 20 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 10 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 10 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 5 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
| 5 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
## Male-to-Female

| SNR | Mode | VanillaVC | SE+VC | SpkBeamVC | SE+SpkBeamVC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| inf | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| inf | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2female@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| 20 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 20 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2female@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 10 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 10 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2female@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 5 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
| 5 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2female@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
## Male-to-Male

| SNR | Mode | VanillaVC | SE+VC | SpkBeamVC | SE+SpkBeamVC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| inf | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| inf | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| 20 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 20 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 10 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 10 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 5 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
| 5 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__male2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
## Female-to-Male

| SNR | Mode | VanillaVC | SE+VC | SpkBeamVC | SE+SpkBeamVC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| inf | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| inf | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2male@1__NR@NO_NOISE@infdB.wav" preload="metadata"></audio> |
| 20 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 20 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2male@1__NR@SE_RESTAURANT@20dB.wav" preload="metadata"></audio> |
| 10 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 10 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2male@1__NR@SE_RESTAURANT@10dB.wav" preload="metadata"></audio> |
| 5 | Offline | <audio controls controlslist="nodownload" src="wav/vanillavc.offline__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.offline__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.offline__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.offline__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
| 5 | Stream | <audio controls controlslist="nodownload" src="wav/vanillavc.stream__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_vc.stream__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/spkbeamvc.stream__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> | <audio controls controlslist="nodownload" src="wav/se_spkbeamvc.stream__female2male@1__NR@SE_RESTAURANT@5dB.wav" preload="metadata"></audio> |
