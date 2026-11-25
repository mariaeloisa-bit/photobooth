<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Web Photo Booth</title>
  <style>
    :root {
      --bg: #121212;
      --surface: #1e1e1e;
      --primary: #ff4757;
      --primary-hover: #ff6b81;
      --accent: #2ed573;
      --text: #f1f2f6;
      --muted: #a4b0be;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    }

    body {
      background-color: var(--bg);
      color: var(--text);
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1rem;
    }

    header {
      text-align: center;
      margin-bottom: 1.5rem;
    }

    header h1 {
      font-size: 1.8rem;
      letter-spacing: 1px;
    }

    header p {
      color: var(--muted);
      font-size: 0.9rem;
      margin-top: 0.25rem;
    }

    .booth-container {
      background: var(--surface);
      padding: 1.25rem;
      border-radius: 16px;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.5);
      max-width: 720px;
      width: 100%;
    }

    .viewport-wrapper {
      position: relative;
      width: 100%;
      aspect-ratio: 4 / 3;
      background: #000;
      border-radius: 12px;
      overflow: hidden;
    }

    video {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: filter 0.25s ease;
    }

    .mirrored {
      transform: scaleX(-1);
    }

    #countdown {
      position: absolute;
      inset: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 6rem;
      font-weight: 800;
      color: #fff;
      text-shadow: 0 4px 20px rgba(0, 0, 0, 0.7);
      pointer-events: none;
      opacity: 0;
      transition: opacity 0.2s;
    }

    #flash {
      position: absolute;
      inset: 0;
      background: #fff;
      opacity: 0;
      pointer-events: none;
    }

    .flash-active {
      animation: flashAnim 0.4s ease-out;
    }

    @keyframes flashAnim {
      0% { opacity: 0.95; }
      100% { opacity: 0; }
    }

    #statusToast {
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(18, 18, 18, 0.85);
      color: var(--accent);
      border: 1px solid rgba(46, 213, 115, 0.4);
      padding: 0.4rem 0.9rem;
      border-radius: 999px;
      font-size: 0.8rem;
      font-weight: 600;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.25s ease;
      white-space: nowrap;
    }

    #statusToast.show {
      opacity: 1;
    }

    .filters-bar {
      display: flex;
      gap: 0.5rem;
      overflow-x: auto;
      padding: 1rem 0;
      scrollbar-width: thin;
    }

    .filter-btn {
      background: #2f3542;
      color: var(--text);
      border: 2px solid transparent;
      padding: 0.5rem 1rem;
      border-radius: 20px;
      cursor: pointer;
      font-size: 0.85rem;
      white-space: nowrap;
      transition: all 0.2s;
    }

    .filter-btn:hover {
      background: #3d4454;
    }

    .filter-btn.active {
      border-color: var(--primary);
      background: rgba(255, 71, 87, 0.15);
      font-weight: 600;
    }

    .controls {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      margin-top: 0.5rem;
      gap: 0.75rem;
    }

    .control-btn {
      background: #2f3542;
      color: var(--text);
      border: none;
      padding: 0.65rem 1rem;
      border-radius: 8px;
      cursor: pointer;
      font-size: 0.88rem;
      transition: background 0.2s;
    }

    .control-btn:hover {
      background: #3d4454;
    }

    .control-btn.active-toggle {
      outline: 2px solid var(--accent);
      color: var(--accent);
      font-weight: 600;
    }

    .snap-btn {
      background: var(--primary);
      color: #fff;
      border: none;
      padding: 0.8rem 2rem;
      border-radius: 50px;
      font-size: 1rem;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 4px 15px rgba(255, 71, 87, 0.4);
      transition: transform 0.15s, background 0.2s;
    }

    .snap-btn:hover {
      background: var(--primary-hover);
      transform: scale(1.03);
    }

    .snap-btn:active {
      transform: scale(0.97);
    }

    .gallery-section {
      max-width: 720px;
      width: 100%;
      margin-top: 2rem;
    }

    .gallery-section h2 {
      font-size: 1.2rem;
      margin-bottom: 1rem;
      color: var(--muted);
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
      gap: 1rem;
    }

    .photo-card {
      background: var(--surface);
      padding: 0.5rem;
      border-radius: 10px;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
    }

    .photo-card img {
      width: 100%;
      border-radius: 6px;
      display: block;
    }

    .photo-actions {
      display: flex;
      justify-content: space-between;
      gap: 0.4rem;
    }

    .photo-actions a,
    .photo-actions button {
      flex: 1;
      text-align: center;
      font-size: 0.75rem;
      padding: 0.4rem;
      border-radius: 5px;
      text-decoration: none;
      border: none;
      cursor: pointer;
    }

    .download-link {
      background: var(--accent);
      color: #121212;
      font-weight: 600;
    }

    .delete-btn {
      background: #2f3542;
      color: var(--text);
    }

    canvas {
      display: none;
    }
  </style>
</head>
<body>

  <header>
    <h1>📸 Photo Booth</h1>
    <p>Pick a filter, strike a pose, and snap away</p>
  </header>

  <main class="booth-container">
    <div class="viewport-wrapper">
      <video id="video" class="mirrored" autoplay playsinline></video>
      <div id="countdown"></div>
      <div id="flash"></div>
      <div id="statusToast">Saved to Downloads!</div>
    </div>

    <!-- Filter Selector -->
    <div class="filters-bar" id="filtersBar">
      <button class="filter-btn active" data-filter="none">Normal</button>
      <button class="filter-btn" data-filter="grayscale(100%) contrast(115%)">B&W Classic</button>
      <button class="filter-btn" data-filter="sepia(85%) contrast(105%)">Vintage Sepia</button>
      <button class="filter-btn" data-filter="contrast(130%) saturate(140%)">Vivid Pop</button>
      <button class="filter-btn" data-filter="hue-rotate(180deg) saturate(120%)">Cyber Invert</button>
      <button class="filter-btn" data-filter="sepia(30%) saturate(160%) hue-rotate(-15deg)">Warm Sunset</button>
      <button class="filter-btn" data-filter="brightness(110%) contrast(90%) saturate(80%)">Soft Pastel</button>
      <button class="filter-btn" data-filter="invert(100%)">X-Ray</button>
    </div>

    <!-- Main Controls -->
    <div class="controls">
      <button class="control-btn" id="mirrorBtn">🪞 Mirror: ON</button>
      <button class="control-btn active-toggle" id="autoSaveBtn">💾 Auto-Save: ON</button>
      <button class="snap-btn" id="snapBtn">Take Photo</button>
      <button class="control-btn" id="timerBtn">⏱️ Timer: Off</button>
    </div>
  </main>

  <section class="gallery-section">
    <h2>Captured Photos (<span id="photoCount">0</span>)</h2>
    <div class="gallery-grid" id="gallery"></div>
  </section>

  <canvas id="canvas"></canvas>

  <script>
    const video = document.getElementById('video');
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');
    const snapBtn = document.getElementById('snapBtn');
    const mirrorBtn = document.getElementById('mirrorBtn');
    const autoSaveBtn = document.getElementById('autoSaveBtn');
    const timerBtn = document.getElementById('timerBtn');
    const countdownEl = document.getElementById('countdown');
    const flashEl = document.getElementById('flash');
    const statusToast = document.getElementById('statusToast');
    const gallery = document.getElementById('gallery');
    const photoCountEl = document.getElementById('photoCount');
    const filterButtons = document.querySelectorAll('.filter-btn');

    let currentFilter = 'none';
    let isMirrored = true;
    let autoSave = true;
    let timerSeconds = 0; // 0, 3, or 5
    let isCountingDown = false;
    let toastTimeout = null;

    function showToast(message) {
      statusToast.textContent = message;
      statusToast.classList.add('show');
      clearTimeout(toastTimeout);
      toastTimeout = setTimeout(() => {
        statusToast.classList.remove('show');
      }, 2000);
    }

    function triggerDownload(dataUrl, filename) {
      const link = document.createElement('a');
      link.href = dataUrl;
      link.download = filename;
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }

    // 1. Initialize Webcam
    async function startCamera() {
      try {
        const stream = await navigator.mediaDevices.getUserMedia({
          video: { width: { ideal: 1280 }, height: { ideal: 960 }, facingMode: 'user' },
          audio: false
        });
        video.srcObject = stream;
      } catch (err) {
        alert('Camera access denied or unavailable. Please run via localhost or HTTPS and allow camera permissions.');
        console.error(err);
      }
    }

    // 2. Filter Selection
    filterButtons.forEach(btn => {
      btn.addEventListener('click', () => {
        filterButtons.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        currentFilter = btn.dataset.filter;
        video.style.filter = currentFilter;
      });
    });

    // 3. Mirror Toggle
    mirrorBtn.addEventListener('click', () => {
      isMirrored = !isMirrored;
      video.classList.toggle('mirrored', isMirrored);
      mirrorBtn.textContent = `🪞 Mirror: ${isMirrored ? 'ON' : 'OFF'}`;
    });

    // 4. Auto-Save Toggle
    autoSaveBtn.addEventListener('click', () => {
      autoSave = !autoSave;
      autoSaveBtn.classList.toggle('active-toggle', autoSave);
      autoSaveBtn.textContent = `💾 Auto-Save: ${autoSave ? 'ON' : 'OFF'}`;
    });

    // 5. Timer Toggle (Off -> 3s -> 5s)
    timerBtn.addEventListener('click', () => {
      if (timerSeconds === 0) timerSeconds = 3;
      else if (timerSeconds === 3) timerSeconds = 5;
      else timerSeconds = 0;

      timerBtn.textContent = `⏱️ Timer: ${timerSeconds === 0 ? 'Off' : timerSeconds + 's'}`;
    });

    // 6. Capture Logic with Optional Countdown
    snapBtn.addEventListener('click', () => {
      if (isCountingDown) return;

      if (timerSeconds === 0) {
        takeSnapshot();
      } else {
        runCountdown(timerSeconds);
      }
    });

    function runCountdown(seconds) {
      isCountingDown = true;
      let remaining = seconds;
      countdownEl.textContent = remaining;
      countdownEl.style.opacity = '1';

      const interval = setInterval(() => {
        remaining--;
        if (remaining > 0) {
          countdownEl.textContent = remaining;
        } else {
          clearInterval(interval);
          countdownEl.style.opacity = '0';
          isCountingDown = false;
          takeSnapshot();
        }
      }, 1000);
    }

    function takeSnapshot() {
      if (!video.videoWidth || !video.videoHeight) {
        showToast('Camera not ready yet');
        return;
      }

      // Trigger flash animation
      flashEl.classList.remove('flash-active');
      void flashEl.offsetWidth; // trigger reflow
      flashEl.classList.add('flash-active');

      // Match canvas dimensions to actual video stream
      canvas.width = video.videoWidth;
      canvas.height = video.videoHeight;

      ctx.save();
      ctx.filter = currentFilter;

      // Apply horizontal flip to match mirrored preview
      if (isMirrored) {
        ctx.translate(canvas.width, 0);
        ctx.scale(-1, 1);
      }

      ctx.drawImage(video, 0, 0, canvas.width, canvas.height);
      ctx.restore();

      const imageDataUrl = canvas.toDataURL('image/png');
      const filename = `photobooth-${Date.now()}.png`;

      addPhotoToGallery(imageDataUrl, filename);

      if (autoSave) {
        triggerDownload(imageDataUrl, filename);
        showToast('Saved to Downloads!');
      } else {
        showToast('Captured in gallery');
      }
    }

    // 7. Gallery Management
    function addPhotoToGallery(dataUrl, filename) {
      const card = document.createElement('div');
      card.className = 'photo-card';

      const img = document.createElement('img');
      img.src = dataUrl;
      img.alt = 'Photo booth capture';

      const actions = document.createElement('div');
      actions.className = 'photo-actions';

      const downloadBtn = document.createElement('a');
      downloadBtn.href = dataUrl;
      downloadBtn.download = filename;
      downloadBtn.className = 'download-link';
      downloadBtn.textContent = 'Download';

      const deleteBtn = document.createElement('button');
      deleteBtn.className = 'delete-btn';
      deleteBtn.textContent = 'Delete';
      deleteBtn.onclick = () => {
        card.remove();
        updatePhotoCount();
      };

      actions.appendChild(downloadBtn);
      actions.appendChild(deleteBtn);
      card.appendChild(img);
      card.appendChild(actions);

      gallery.prepend(card);
      updatePhotoCount();
    }

    function updatePhotoCount() {
      photoCountEl.textContent = gallery.children.length;
    }

    startCamera();
  </script>
</body>
</html>
