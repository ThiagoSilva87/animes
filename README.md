# animes
html para um site informativo sobre animes.
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Animes de 2023</title>
    <style>
        /* Estilos básicos - personalize conforme necessário */
        body {
            font-family: Arial, sans-serif;
        }

        header {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
        }

        h1 {
            margin: 0;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        li {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Principais Animes de 2023</h1>
    </header>

    <div class="container">
        <input type="text" id="search" placeholder="Pesquisar por anime...">
        <ul id="anime-list">
            <li>Nome do Anime 1</li>
            <li>Nome do Anime 2</li>
            <li>Nome do Anime 3</li>
            <!-- Adicione mais animes à medida que necessário -->
        </ul>
    </div>

    <script>
        // JavaScript para a barra de pesquisa
        const searchInput = document.getElementById('search');
        const animeList = document.getElementById('anime-list');

        searchInput.addEventListener('input', function () {
            const searchTerm = searchInput.value.toLowerCase();
            const items = animeList.getElementsByTagName('li');

            for (let i = 0; i < items.length; i++) {
                const item = items[i];
                const text = item.textContent.toLowerCase();

                if (text.includes(searchTerm)) {
                    item.style.display = 'block';
                } else {
                    item.style.display = 'none';
                }
            }
        });
    </script>
</body>
</html>
