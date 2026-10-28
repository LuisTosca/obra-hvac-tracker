* { box-sizing: border-box; }

html, body, #root {
  margin: 0;
  min-height: 100%;
  font-family: Inter, 'Segoe UI', sans-serif;
  background: #f4f7fb;
}

body {
  min-height: 100vh;
}

button, input, select, textarea {
  font: inherit;
}

button {
  cursor: pointer;
}

.app-shell {
  min-height: 100vh;
  background: #eef3fb;
  color: #18314f;
}

.app-shell.dark {
  background: #0f172a;
  color: #e2e8f0;
}

.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 18px 28px;
  background: rgba(255,255,255,0.75);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(15,23,42,0.08);
}

.dark .topbar {
  background: rgba(15, 23, 42, 0.7);
  border-color: rgba(148,163,184,0.2);
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 12px;
}

.brand-block small {
  display: block;
  color: #64748b;
  font-size: 0.68rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.brand-block h1 {
  margin: 2px 0 0;
  font-size: 1.3rem;
}

.logo-mini, .logo-preview {
  width: 42px;
  height: 42px;
  border-radius: 12px;
  object-fit: cover;
}

.logo-fallback, .logo-placeholder {
  width: 42px;
  height: 42px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  background: linear-gradient(135deg, #1d4ed8, #38bdf8);
  color: white;
  font-weight: 700;
}

.topbar-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.primary-btn, .secondary-btn, .ghost-btn, .danger-btn {
  border: none;
  border-radius: 10px;
  padding: 10px 14px;
  font-weight: 600;
  transition: transform 0.15s ease, opacity 0.15s ease;
}

.primary-btn {
  background: linear-gradient(135deg, #2563eb, #1d4ed8);
  color: white;
}

.secondary-btn {
  background: #e2e8f0;
  color: #0f172a;
}

.dark .secondary-btn {
  background: #1e293b;
  color: #e2e8f0;
}

.ghost-btn {
  background: transparent;
  color: inherit;
  border: 1px solid rgba(148,163,184,0.4);
}

.danger-btn {
  background: rgba(239, 68, 68, 0.08);
  color: #dc2626;
}

.primary-btn:hover, .secondary-btn:hover, .danger-btn:hover, .ghost-btn:hover {
  transform: translateY(-1px);
}

.status-pill, .small-tag {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  padding: 6px 10px;
  font-size: 0.72rem;
  font-weight: 700;
  background: rgba(37, 99, 235, 0.12);
  color: #2563eb;
}

.workspace {
  display: grid;
  grid-template-columns: 330px minmax(0, 1fr);
  gap: 24px;
  padding: 24px 28px 36px;
}

.project-sidebar, .card, .detail-panel {
  border: 1px solid rgba(148,163,184,0.2);
  border-radius: 18px;
  background: rgba(255,255,255,0.76);
  box-shadow: 0 10px 30px rgba(15,23,42,0.04);
}

.dark .project-sidebar,
.dark .card,
.dark .detail-panel {
  background: rgba(15,23,42,0.75);
  border-color: rgba(148,163,184,0.15);
}

.project-sidebar {
  padding: 18px;
}

.section-header {
  margin-bottom: 14px;
}

.project-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.project-card {
  border: 1px solid rgba(148,163,184,0.22);
  background: transparent;
  border-radius: 14px;
  padding: 14px;
  text-align: left;
  color: inherit;
}

.project-card.active {
  background: rgba(37,99,235,0.08);
  border-color: rgba(37,99,235,0.4);
}

.project-card-top,
.meta-row,
.detail-header,
.card-header-row,
.plan-header-row,
.issue-title-row,
.detail-metrics,
.modal-actions,
.attachment-row,
.form-grid {
  display: flex;
  justify-content: space-between;
  gap: 10px;
}

.project-card-top {
  align-items: center;
}

.project-card strong {
  display: block;
  margin-bottom: 4px;
}

.project-card small {
  color: #64748b;
}

.meta-row {
  margin-top: 10px;
  font-size: 0.74rem;
  color: #64748b;
}

.detail-panel {
  padding: 22px;
}

.detail-header {
  align-items: center;
  margin-bottom: 16px;
}

.eyebrow {
  display: block;
  font-size: 0.7rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #64748b;
  margin-bottom: 8px;
}

.detail-header h2 {
  margin: 0;
  font-size: 2rem;
}

.detail-metrics {
  align-items: center;
  gap: 12px;
  color: #64748b;
  font-size: 0.8rem;
}

.tabs {
  display: flex;
  gap: 10px;
  padding: 8px;
  border-radius: 12px;
  background: rgba(148,163,184,0.08);
  margin-bottom: 18px;
}

.tab {
  border: none;
  border-radius: 10px;
  padding: 10px 14px;
  background: transparent;
  color: inherit;
  font-weight: 600;
}

.tab.active {
  background: white;
  color: #1e3a8a;
}

.dark .tab.active {
  background: #111827;
  color: #bfdbfe;
}

.tab-content {
  display: grid;
  gap: 18px;
}

.overview-grid {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.card {
  padding: 18px;
}

.full-span {
  grid-column: 1 / -1;
}

.stat-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 12px;
}

.stat-box {
  padding: 16px;
  border-radius: 12px;
  background: rgba(148,163,184,0.08);
}

.stat-box span {
  display: block;
  color: #64748b;
  font-size: 0.76rem;
}

.stat-box strong {
  display: block;
  margin-top: 6px;
  font-size: 1.8rem;
}

.info-list {
  display: grid;
  gap: 12px;
}

.info-list div {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  padding-bottom: 10px;
  border-bottom: 1px solid rgba(148,163,184,0.18);
}

.info-list span {
  color: #64748b;
}

.quick-photo-form,
.issue-form {
  display: grid;
  gap: 12px;
}

textarea,
input,
select {
  width: 100%;
  border: 1px solid rgba(148,163,184,0.35);
  border-radius: 10px;
  padding: 10px 12px;
  background: rgba(248,250,252,0.7);
  color: inherit;
}

.dark textarea,
.dark input,
.dark select {
  background: rgba(15,23,42,0.9);
}

textarea {
  min-height: 90px;
  resize: vertical;
}

label {
  display: grid;
  gap: 8px;
  font-weight: 600;
}

.form-grid {
  display: grid;
  gap: 12px;
}

.two-col {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.three-col {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.upload-inline {
  position: relative;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: fit-content;
  border: 1px dashed rgba(59,130,246,0.7);
  background: rgba(59,130,246,0.08);
  border-radius: 10px;
  padding: 8px 12px;
  color: #2563eb;
  overflow: hidden;
}

.upload-inline input {
  position: absolute;
  inset: 0;
  opacity: 0;
  cursor: pointer;
}

.photo-gallery,
.attachment-list,
.issue-list,
.task-table,
.plan-list,
.report-list,
.mini-gallery {
  display: grid;
  gap: 12px;
}

.photo-item,
.issue-item,
.task-row {
  display: grid;
  gap: 10px;
  padding: 12px;
  border-radius: 12px;
  background: rgba(148,163,184,0.06);
}

.photo-item {
  grid-template-columns: 180px minmax(0, 1fr);
  align-items: center;
}

.photo-item img,
.mini-thumb,
.logo-preview {
  width: 100%;
  max-height: 180px;
  object-fit: cover;
  border-radius: 12px;
}

.photo-item p,
.issue-item p {
  margin: 0;
  color: #64748b;
}

.plan-item {
  display: flex;
  gap: 8px;
  align-items: center;
}

.plan-select {
  flex: 1;
  border: 1px solid rgba(148,163,184,0.2);
  border-radius: 10px;
  padding: 10px 12px;
  background: transparent;
  color: inherit;
  text-align: left;
}

.plan-item.selected .plan-select {
  background: rgba(37,99,235,0.08);
  border-color: rgba(37,99,235,0.5);
}

.small {
  padding: 8px 10px;
  font-size: 0.72rem;
}

.plans-grid {
  grid-template-columns: minmax(260px, 320px) minmax(0, 1fr) minmax(240px, 300px);
}

.plan-canvas-wrapper {
  min-height: 500px;
}

.plan-canvas {
  position: relative;
  width: 100%;
  height: 420px;
  border: 1px solid rgba(148,163,184,0.2);
  border-radius: 14px;
  overflow: hidden;
  background: linear-gradient(135deg, #e2e8f0, #f8fafc);
}

.dark .plan-canvas {
  background: linear-gradient(135deg, #0f172a, #1e293b);
}

.plan-canvas img,
.plan-canvas embed {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.issue-point {
  position: absolute;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  border: 3px solid white;
  transform: translate(-50%, -50%);
  box-shadow: 0 8px 18px rgba(15, 23, 42, 0.18);
}

.issue-list {
  max-height: 480px;
  overflow: auto;
}

.task-row {
  grid-template-columns: minmax(0, 1fr) auto auto;
  align-items: center;
}

.task-row strong,
.issue-title-row strong {
  display: block;
}

.task-row small,
.issue-item small {
  color: #64748b;
}

.report-list {
  margin: 0;
  padding-left: 18px;
  line-height: 1.7;
}

.company-preview {
  display: flex;
  align-items: center;
  gap: 16px;
}

.company-preview p,
.company-preview small {
  display: block;
  margin: 4px 0 0;
  color: #64748b;
}

.logo-preview {
  width: 72px;
  height: 72px;
}

.modal-backdrop {
  position: fixed;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(15,23,42,0.5);
  z-index: 1000;
}

.modal-card {
  width: min(700px, 90vw);
  padding: 20px;
  border-radius: 18px;
  background: white;
  color: #0f172a;
}

.dark .modal-card {
  background: #111827;
  color: #e2e8f0;
}

.empty-state {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 220px;
  font-size: 1.1rem;
  color: #64748b;
}

.attachment-item {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  border-radius: 10px;
  background: rgba(148,163,184,0.12);
  min-height: 80px;
}

.attachment-item img {
  max-width: 100%;
  max-height: 110px;
  object-fit: cover;
}

.file-pill,
.mini-file {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 8px 10px;
  border-radius: 8px;
  background: rgba(59,130,246,0.12);
  color: #1d4ed8;
  font-weight: 600;
}

.mini-gallery {
  grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
}

.mini-thumb-wrap {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 80px;
}

.mini-thumb {
  max-height: 80px;
}

@media (max-width: 1100px) {
  .workspace {
    grid-template-columns: 1fr;
  }

  .plans-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 720px) {
  .topbar,
  .detail-header,
  .card-header-row,
  .plan-header-row,
  .project-card-top,
  .info-list div,
  .detail-metrics,
  .modal-actions,
  .company-preview {
    flex-direction: column;
    align-items: flex-start;
  }

  .overview-grid,
  .two-col,
  .three-col {
    grid-template-columns: 1fr;
  }

  .photo-item {
    grid-template-columns: 1fr;
  }

  .task-row {
    grid-template-columns: 1fr;
  }
}
