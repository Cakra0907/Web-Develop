# Web-Develop
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ucapan Ulang Tahun</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f9;
            color: #333;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 8px;
            background-color: #fff;
        }
        #message {
            white-space: pre-wrap; /* Agar spasi dan line break tetap terjaga */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>KEPADA KELAS A</h1>
        <div id="message"></div>
    </div>

    <script>
        function tampilkanPesan(teks, delay) {
            let index = 0;
            const elemenPesan = document.getElementById('message');
            
            function tampilkanHuruf() {
                if (index < teks.length) {
                    elemenPesan.textContent += teks[index];
                    index++;
                    setTimeout(tampilkanHuruf, delay);
                }
            }

            tampilkanHuruf();
        }

        const namaPenerima = 'SMANTI';
        const namaPengirim = 'ABEL CAKRA';
        const pesan = `
SMANTI NIH BOS, ${namaPenerima}!

GIGIT KELAK

${namaPengirim}
`;

        tampilkanPesan(pesan, 50); // Delay 50 ms antara huruf
    </script>
</body>
</html>
