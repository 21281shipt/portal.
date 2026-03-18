# portal.<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>V. Ambrošić | Legacy Vault</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { background-color: #000; color: #d4af37; font-family: 'Segoe UI', sans-serif; }
        .gold-border { border: 1px solid #d4af37; }
        #display-id { letter-spacing: 2px; }
    </style>
</head>
<body class="p-6">

    <div class="max-w-md mx-auto gold-border p-8 rounded-3xl bg-[#050505] shadow-2xl text-center">
        
        <h1 class="text-2xl tracking-[5px] uppercase font-bold mb-1">Veljko Ambrošić</h1>
        <p class="text-[10px] text-zinc-500 tracking-[3px] uppercase mb-8">Legacy • Berlin • Vienna • Paris</p>

        <div class="bg-[#111] border-l-4 border-[#d4af37] p-4 mb-8 text-left">
            <p class="text-white text-[11px] leading-relaxed uppercase tracking-wider">
                "Access is restricted. Please follow the protocol."<br>
                <span class="text-zinc-500 normal-case text-[10px] italic">(Pristup je ograničen. Pratite protokol za autorizaciju.)</span>
            </p>
        </div>

        <a href="https://ig.me/m/veljko_ambrosic" class="bg-[#d4af37] text-black block text-center py-4 rounded-xl font-bold uppercase text-sm mb-8 hover:scale-[1.02] transition">
            💎 SEND PROOF TO DM (POŠALJI DOKAZ) 💎
        </a>

        <div class="space-y-6 text-left">
            <h3 class="text-[#d4af37] border-b border-[#d4af37] pb-1 text-xs uppercase mb-3 text-center tracking-[4px]">Access / Pristup</h3>
            
            <div id="unlock-card" onclick="revealAndCopy()" class="bg-[#151515] p-6 border border-dashed border-[#d4af37] rounded-2xl cursor-pointer text-center group">
                <p id="label" class="text-zinc-500 text-[9px] uppercase mb-2 tracking-[2px]">Click to reveal ID / Klikni za prikaz</p>
                <div id="display-id" class="text-white text-lg font-mono tracking-tighter">•••• •••• •••• •••• •••• ••</div>
                <p id="bank-info" class="text-[9px] mt-2 text-zinc-600 uppercase tracking-widest"></p>
                <span id="copy-status" class="block mt-2 text-[9px] text-[#d4af37] opacity-0 uppercase">Copied! / Kopirano!</span>
            </div>

            <div class="grid grid-cols-2 gap-3 mt-4">
                <div class="bg-zinc-900/50 p-3 rounded-xl border border-zinc-800">
                    <p class="text-[9px] text-zinc-500 uppercase">Regional (Balkan)</p>
                    <p class="text-white font-bold text-lg">15 EUR</p>
                </div>
                <div class="bg-zinc-900/50 p-3 rounded-xl border border-zinc-800">
                    <p class="text-[9px] text-zinc-500 uppercase">Global (World)</p>
                    <p class="text-white font-bold text-lg">35-45 EUR</p>
                </div>
            </div>
        </div>

        <div class="mt-10 pt-6 border-t border-zinc-900 text-[10px] text-zinc-500 text-left space-y-3">
            <p><strong>Verification:</strong> Send screenshot to DM.<br>
            <span class="italic text-zinc-600">(Pošaljite screenshot uplate u DM.)</span></p>
        </div>

        <div class="mt-12 text-center text-[9px] text-zinc-700 tracking-[4px] uppercase">
            V. AMBROŠIĆ | SINCE 1960
        </div>
    </div>

    <script>
        function revealAndCopy() {
            const rawId = "RS35265001000002742438";
            const formattedId = "RS35 2650 0100 0002 7424 38";
            document.getElementById('display-id').innerText = formattedId;
            document.getElementById('label').innerText = "AUTHORIZATION ID";
            document.getElementById('bank-info').innerText = "Raiffeisen Bank";
            
            const el = document.createElement("textarea");
            el.value = rawId;
            document.body.appendChild(el);
            el.select();
            document.execCommand("copy");
            document.body.removeChild(el);

            const status = document.getElementById('copy-status');
            status.style.opacity = '1';
            setTimeout(() => { status.style.opacity = '0'; }, 2000);
        }
    </script>
</body>
</html>
