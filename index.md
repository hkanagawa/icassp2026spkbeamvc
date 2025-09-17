# SpeakerBeam-VC: Noise-Robust Voice Conversion with Speaker Enrollment — Demos   <!-- omit in toc -->
Authors: Hiroki Kanagawa, Yusuke Ijima, Kenichi Fujita, Takafumi Moriya, Taichi Asami  
Affiliation: NTT, Inc., Japan

# Contents  <!-- omit in toc -->
- [Comparison VCs (Reference: Table 1 in paper)](#comparison-vcs-reference-table-1-in-paper)
- [Speech samples](#speech-samples)

# Comparison VCs (Reference: Table 1 in paper)

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
  text-align: center;
  white-space: nowrap; /* keep columns compact */
}
table.comp th {
  background: #f4f4f4;
  position: sticky;   /* keep header visible while scrolling horizontally */
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
      <th>SE Preprocessing</th>
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
      <td>EnrollVC (ours)</td>
      <td>✘</td>
      <td>✔︎</td>
      <td>Proposed method: noise-robust VC using source speaker embedding.</td>
    </tr>
    <tr>
      <td>SE+EnrollVC</td>
      <td>✔︎</td>
      <td>✔︎</td>
      <td>Proposed variant: SE preprocessing combined with enrollment.</td>
    </tr>
  </tbody>
</table>
</div>

# Speech samples
If you are having trouble listening to the audios, try refreshing the page.
All speakers in this page are chosen from unseen test data

<!-- <audio controls controlslist="nodownload" src="./data/orgwav/FMH.20243Q_interact@10_tsukareta@117-0.wav" preload="metadata"></audio> -->

