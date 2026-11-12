<!-- ... existing code ... -->
    <!-- TELA INICIAL (MENU) -->
    <div id="menu-screen" class="fixed inset-0 z-30 flex items-center justify-center p-4 bg-slate-950/60 backdrop-blur-md">
        <div class="w-full max-w-md bg-gradient-to-b from-emerald-900/95 via-teal-900/95 to-slate-900/95 border-2 border-amber-400/50 rounded-3xl p-6 shadow-2xl text-white flex flex-col gap-4 max-h-[92vh] overflow-y-auto">
            
            <!-- Título / Logo -->
            <div class="text-center">
                <div class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-amber-400/20 border border-amber-300/40 text-amber-300 text-xs font-extrabold uppercase tracking-wider mb-1.5">
                    <span>🇧🇷</span> Rio de Janeiro Edition
                </div>
                <h1 class="game-title text-4xl sm:text-5xl font-black tracking-tight bg-gradient-to-r from-amber-300 via-yellow-200 to-emerald-300 bg-clip-text text-transparent drop-shadow">
                    BRAZIL SURF
                </h1>
                <p class="text-xs sm:text-sm text-emerald-100/85 mt-1 font-medium">
                    Corra pelos trilhos, suba nas rampas dos trens ou faça o desafio <strong>No Coins</strong>!
                </p>
            </div>

            <!-- Recorde Pessoal Local -->
            <div class="grid grid-cols-3 gap-2 bg-slate-950/60 rounded-2xl p-3 border border-white/10 text-center">
                <div>
                    <div class="text-[10px] uppercase font-bold text-slate-400">Seu Recorde</div>
                    <div id="menu-highscore" class="text-lg font-black text-amber-400">0</div>
                </div>
                <div class="border-x border-white/10">
                    <div class="text-[10px] uppercase font-bold text-slate-400">Melhor Tempo</div>
                    <div id="menu-besttime" class="text-lg font-black text-sky-400">00:00</div>
                </div>
                <div>
                    <div class="text-[10px] uppercase font-bold text-slate-400">No Coins</div>
                    <div id="menu-nocoins-best" class="text-lg font-black text-emerald-400">0</div>
                </div>
            </div>

            <!-- Seleção dos 3 Modos de Jogo -->
            <div class="flex flex-col gap-2.5">
                <div class="text-xs font-extrabold uppercase tracking-wider text-emerald-200/90 text-center">
                    Toque no modo para jogar:
                </div>

                <!-- Modo 1: Normal -->
                <button onclick="startGame('normal')" class="btn-press group relative flex items-center justify-between w-full p-3.5 rounded-2xl bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-400 hover:to-teal-500 border-2 border-emerald-300/60 shadow-lg text-left transition-all">
                    <div class="flex items-center gap-3">
                        <span class="text-3xl bg-white/15 p-2 rounded-xl">🚆</span>
                        <div>
                            <div class="font-black text-base text-white flex items-center gap-2">
                                MODO NORMAL
                                <span class="text-[10px] bg-black/30 px-2 py-0.5 rounded-full font-bold text-emerald-200">CLÁSSICO</span>
                            </div>
                            <div class="text-xs text-emerald-50/90 leading-snug">
                                Trens, rampas de subida e pistas livres para <strong>No Coins</strong>.
                            </div>
                        </div>
                    </div>
                    <span class="text-xl font-black text-white/90 group-hover:translate-x-1 transition-transform">▶</span>
                </button>

                <!-- Modo 2: Chão é Lava -->
                <button onclick="startGame('lava')" class="btn-press group relative flex items-center justify-between w-full p-3.5 rounded-2xl bg-gradient-to-r from-red-600 via-orange-600 to-amber-600 hover:from-red-500 hover:to-amber-500 border-2 border-amber-300/70 shadow-lg text-left transition-all">
                    <div class="flex items-center gap-3">
                        <span class="text-3xl bg-white/15 p-2 rounded-xl">🌋</span>
                        <div>
                            <div class="font-black text-base text-white flex items-center gap-2">
                                CHÃO É LAVA
                                <span class="text-[10px] bg-black/35 px-2 py-0.5 rounded-full font-bold text-amber-200">SUPER PULSO</span>
                            </div>
                            <div class="text-xs text-orange-50/95 leading-snug">
                                Encostou na lava? Dá um <strong>Super Pulso</strong> e volta pro trem!
                            </div>
                        </div>
                    </div>
                    <span class="text-xl font-black text-white/90 group-hover:translate-x-1 transition-transform">▶</span>
                </button>

                <!-- Modo 3: 3 Fileiras -->
                <button onclick="startGame('three_rows')" class="btn-press group relative flex items-center justify-between w-full p-3.5 rounded-2xl bg-gradient-to-r from-amber-500 via-yellow-500 to-orange-500 hover:from-amber-400 hover:to-orange-400 border-2 border-yellow-200/80 shadow-lg text-left transition-all">
                    <div class="flex items-center gap-3">
                        <span class="text-3xl bg-black/15 p-2 rounded-xl">🪙</span>
                        <div>
                            <div class="font-black text-base text-slate-950 flex items-center gap-2">
                                MODO 3 FILEIRAS
                                <span class="text-[10px] bg-slate-950/20 px-2 py-0.5 rounded-full font-extrabold text-slate-950">CHUVA DE OURO</span>
                            </div>
                            <div class="text-xs text-slate-900 font-semibold leading-snug">
                                Apenas 3 fileiras contínuas de moedas brilhantes nas pistas!
                            </div>
                        </div>
                    </div>
                    <span class="text-xl font-black text-slate-950 group-hover:translate-x-1 transition-transform">▶</span>
                </button>
            </div>

            <!-- Dica rápida de controles -->
            <div class="text-center text-[11px] text-emerald-100/75 bg-black/25 rounded-xl py-2 px-3 border border-white/5">
                📱 <strong>Celular:</strong> Deslize ⬅️ ➡️ ⬆️ ⬇️ &nbsp;|&nbsp; 💻 <strong>PC:</strong> Setas ou WASD
            </div>
        </div>
    </div>

    <!-- TELA DE PAUSA -->
    <div id="pause-screen" class="hidden fixed inset-0 z-30 flex items-center justify-center p-4 bg-slate-950/70 backdrop-blur-md">
        <div class="w-full max-w-sm bg-slate-900 border-2 border-emerald-400/50 rounded-3xl p-6 text-center text-white shadow-2xl flex flex-col gap-4">
            <h2 class="game-title text-3xl font-black text-amber-300">JOGO PAUSADO</h2>
            <p class="text-sm text-slate-300">Respire fundo e continue sua corrida pelo Rio!</p>
            <div class="flex flex-col gap-2.5 mt-2">
                <button onclick="resumeGame()" class="btn-press w-full py-3.5 rounded-2xl bg-emerald-500 hover:bg-emerald-400 font-black text-slate-950 text-base shadow-lg">
                    ▶ CONTINUAR
                </button>
                <button onclick="returnToMenu()" class="btn-press w-full py-3 rounded-2xl bg-slate-800 hover:bg-slate-700 font-bold text-slate-200 text-sm border border-white/10">
                    🏠 VOLTAR AO MENU
                </button>
            </div>
        </div>
    </div>

    <!-- TELA DE GAME OVER -->
    <div id="gameover-screen" class="hidden fixed inset-0 z-30 flex items-center justify-center p-4 bg-slate-950/75 backdrop-blur-md">
        <div class="w-full max-w-md bg-gradient-to-b from-slate-900 to-slate-950 border-2 border-rose-500/60 rounded-3xl p-6 text-center text-white shadow-2xl flex flex-col gap-4">
            <div>
                <span id="gameover-badge" class="inline-block px-3 py-1 rounded-full bg-rose-500/20 border border-rose-400/40 text-rose-300 text-xs font-extrabold uppercase mb-1">
                    Fim de Corrida
                </span>
                <h2 class="game-title text-3xl sm:text-4xl font-black text-white">BATEU!</h2>
                <p id="gameover-reason" class="text-xs text-slate-300 mt-1">Você colidiu com um obstáculo nos trilhos.</p>
            </div>

            <!-- Resumo da Partida -->
            <div class="grid grid-cols-3 gap-2 bg-black/40 p-3.5 rounded-2xl border border-white/10">
                <div>
                    <div class="text-[10px] font-bold uppercase text-slate-400">Pontuação</div>
                    <div id="final-score" class="text-xl font-black text-amber-400">0</div>
                </div>
                <div class="border-x border-white/10">
                    <div class="text-[10px] font-bold uppercase text-slate-400">Tempo</div>
                    <div id="final-time" class="text-xl font-black text-sky-400">00:00</div>
                </div>
                <div>
                    <div class="text-[10px] font-bold uppercase text-slate-400">Moedas</div>
                    <div id="final-coins" class="text-xl font-black text-yellow-300">0</div>
                </div>
            </div>

            <!-- Selo Novo Recorde ou No Coins -->
            <div id="gameover-highlight" class="hidden py-2 px-3 rounded-xl bg-emerald-500/20 border border-emerald-400/50 text-emerald-300 text-xs font-extrabold">
                🏆 NOVO RECORDE PESSOAL!
            </div>

            <!-- Ações -->
            <div class="flex flex-col gap-2.5 mt-1">
                <button onclick="restartCurrentMode()" class="btn-press w-full py-3.5 rounded-2xl bg-gradient-to-r from-emerald-500 to-teal-500 hover:from-emerald-400 hover:to-teal-400 font-black text-slate-950 text-base shadow-lg">
                    🔄 JOGAR NOVAMENTE
                </button>
                <button onclick="returnToMenu()" class="btn-press w-full py-3 rounded-2xl bg-slate-800 hover:bg-slate-700 font-bold text-slate-200 text-sm border border-white/10">
                    🏠 TROCAR DE MODO
                </button>
            </div>
        </div>
    </div>
<!-- ... existing code ... -->
        // ============================================================================
        // PERSISTÊNCIA LOCAL (RECORDE PESSOAL NO NAVEGADOR)
        // ============================================================================
        const STORAGE_KEY = 'brazil_surf_personal_stats_v1';
        let personalStats = {
            highScore: 0,
            bestTime: 0,
            noCoinsBest: 0
        };

        function loadPersonalStats() {
            try {
                const raw = localStorage.getItem(STORAGE_KEY);
                if (raw) {
                    const parsed = JSON.parse(raw);
                    personalStats.highScore = Number(parsed.highScore) || 0;
                    personalStats.bestTime = Number(parsed.bestTime) || 0;
                    personalStats.noCoinsBest = Number(parsed.noCoinsBest) || 0;
                }
            } catch (e) {
                console.warn('Erro ao carregar recordes locais:', e);
            }
        }

        function savePersonalStats() {
            try {
                localStorage.setItem(STORAGE_KEY, JSON.stringify(personalStats));
            } catch (e) {
                console.warn('Erro ao salvar recordes locais:', e);
            }
        }

        function formatTime(seconds) {
            const totalSecs = Math.floor(seconds);
            const mins = Math.floor(totalSecs / 60);
            const secs = totalSecs % 60;
            return `${String(mins).padStart(2, '0')}:${String(secs).padStart(2, '0')}`;
        }

        function updateMenuStatsUI() {
            const hsEl = document.getElementById('menu-highscore');
            const btEl = document.getElementById('menu-besttime');
            const ncEl = document.getElementById('menu-nocoins-best');
            if (hsEl) hsEl.textContent = Math.floor(personalStats.highScore).toLocaleString('pt-BR');
            if (btEl) btEl.textContent = formatTime(personalStats.bestTime);
            if (ncEl) ncEl.textContent = Math.floor(personalStats.noCoinsBest).toLocaleString('pt-BR');
        }
<!-- ... existing code ... -->
            window.addEventListener('resize', onWindowResize);
            setupInputListeners();
            loadPersonalStats();
            updateMenuStatsUI();
        }
<!-- ... existing code ... -->
            // Controles de Teclado (Setas, WASD, Espaço, ESC/P)
            window.addEventListener('keydown', (e) => {
                const code = e.code;
                if (code === 'Escape' || code === 'KeyP') {
                    if (gameState === 'PLAYING') pauseGame();
                    else if (gameState === 'PAUSED') resumeGame();
                    return;
                }
<!-- ... existing code ... -->
        function startGame(mode) {
            try {
                sound.init();
                currentMode = mode;
                clearWorldEntities();
<!-- ... existing code ... -->
                // Atualizar UI e garantir que o canvas 3D apareça imediatamente
                const menuEl = document.getElementById('menu-screen');
                menuEl.classList.add('hidden');
                menuEl.style.display = 'none';

                document.getElementById('gameover-screen').classList.add('hidden');
                document.getElementById('pause-screen').classList.add('hidden');
                document.getElementById('hud').classList.remove('hidden');

                const hint = document.getElementById('controls-hint');
<!-- ... existing code ... -->
        function triggerGameOver(reasonText) {
            gameState = 'GAMEOVER';
            sound.playCrash();
            cameraShake = 0.55;

            const finalScoreVal = Math.floor(score);
            const isNoCoinsRun = (runCoins === 0 && currentMode !== 'three_rows');
            let isNewRecord = false;

            if (finalScoreVal > personalStats.highScore) {
                personalStats.highScore = finalScoreVal;
                isNewRecord = true;
            }
            if (runElapsedTime > personalStats.bestTime) {
                personalStats.bestTime = runElapsedTime;
            }
            if (isNoCoinsRun && finalScoreVal > personalStats.noCoinsBest) {
                personalStats.noCoinsBest = finalScoreVal;
                isNewRecord = true;
            }
            savePersonalStats();

            document.getElementById('hud').classList.add('hidden');
            document.getElementById('gameover-reason').textContent = reasonText || 'Você colidiu com um obstáculo.';
            document.getElementById('final-score').textContent = finalScoreVal.toLocaleString('pt-BR');
            document.getElementById('final-time').textContent = formatTime(runElapsedTime);
            document.getElementById('final-coins').textContent = runCoins;

            const highlightEl = document.getElementById('gameover-highlight');
            if (isNewRecord) {
                highlightEl.textContent = isNoCoinsRun
                    ? '🏆 NOVO RECORDE PESSOAL (NO COINS)!'
                    : '🏆 NOVO RECORDE PESSOAL!';
                highlightEl.classList.remove('hidden');
            } else if (isNoCoinsRun) {
                highlightEl.textContent = '🚫 CORRIDA NO COINS CONCLUÍDA!';
                highlightEl.classList.remove('hidden');
            } else {
                highlightEl.classList.add('hidden');
            }

            document.getElementById('gameover-screen').classList.remove('hidden');
        }
<!-- ... existing code ... -->
