# portal.<!DOCTYPE html>
<html lang="sr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>V. Ambrošić | Arhiv</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { background-color: #000; color: #d4af37; font-family: 'Segoe UI', sans-serif; }
        .gold-border { border: 1px solid #d4af37; }
    </style>
</head>
<body class="p-6">
    <div class="max-w-md mx-auto gold-border p-8 rounded-2xl bg-[#050505] shadow-2xl text-center">
        
        <h1 class="text-2xl tracking-[4px] uppercase font-bold mb-1">Veljko Ambrošić</h1>
        <p class="text-[10px] text-zinc-500 tracking-[2px] uppercase mb-8">Nasleđe • Berlin • Beč • Pariz</p>

        <div class="bg-[#111] border-l-4 border-[#d4af37] p-4 mb-8 text-left">
            <p class="text-white text-xs leading-relaxed italic">
                "Pristup digitalnom arhivu porodice Ambrošić je ograničen. Molimo pratite protokol za autorizaciju."
            </p>
        </div>

        <a href="https://ig.me/m/veljko_ambrosic" class="bg-[#d4af37] text-black block text-center py-4 rounded-lg font-bold uppercase text-sm mb-8 hover:opacity-90">
            💎 POŠALJI POTVRDU U DM 💎
        </a>

        <div class="space-y-6 text-left">
            <h3 class="text-[#d4af37] border-b border-[#d4af37] pb-1 text-sm uppercase mb-3 text-center tracking-widest">Procedura</h3>
            
            <div id="unlock-card" onclick="revealData()" class="bg-[#1a1a1a] p-5 border border-dashed border-[#d4af37] rounded-lg cursor-pointer text-center">
                <p id="label" class="text-zinc-500 text-[10px] uppercase mb-2 tracking-widest">Kliknite za prikaz ID-a</p>
                <div id="display-id" class="text-white text-lg font-mono tracking-tighter">•••• •••• •••• •••• •••• ••</div>
                <p id="bank-name" class="text-[10px] mt-2 text-zinc-600 uppercase"></p>
            </div>

            <div class="text-[11px] text-zinc-400 space-y-2 mt-4 px-2">
                <p>• <strong>Regional (Srbija/Balkan):</strong> 15 v-r-e-d-n-o-s-t</p>
                <p>• <strong>Global (International):</strong> 35-45 v-r-e-d-n-o-s-t</p>
            </div>
        </div>

        <div class="mt-10 pt-6 border-t border-zinc-900 text-[11px] text-zinc-500 text-left italic">
            <strong>Napomena:</strong> Nakon uplate, sistemu je potrebno do 30 minuta za verifikaciju. Pošaljite screenshot u DM.
        </div>
    </div>

    <script>
        function revealData() {
            const id = "RS35 2650 0100 0002 7424 38";
            document.getElementById('display-id').innerText = id;
            document.getElementById('label').innerText = "ID KOPIRAN!";
            document.getElementById('bank-name').innerText = "Sistem: Raiffeisen";
            
            // Automatsko kopiranje
            const el = document.createElement("textarea");
            el.value = id.replace(/\s/g, '');
            document.body.appendChild(el);
            el.select();
            document.execCommand("copy");
            document.body.removeChild(el);
        }
    </script>
</body>
</html>
