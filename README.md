<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pianificazione Lezioni</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 20px;
            background-color: #f4f4f9;
        }
        h1 {
            color: #333;
        }
        form {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        input, textarea, select {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        button {
            background-color: #80dd06;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        h1, h2 {
            color: #333;
        }
        form {
            margin-bottom: 20px;
            padding: 20px;
            background: #fff;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        label {
            font-weight: bold;
        }
        select, button {
            padding: 10px;
            margin-top: 10px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            width: 100%;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #4CAF50;
            color: white;
        }
        .average {
            font-weight: bold;
            color: #4CAF50;
        }
        input, select, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: center;
        }
        select, input, textarea, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        form {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
        }
        select, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .report-header {
            font-weight: bold;
            margin: 20px 0 10px;
        }
        input, textarea, select, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .message-preview {
            margin-top: 20px;
            padding: 15px;
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        input, select, textarea, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <h1>Pianificazione Lezioni</h1>
    <form action="/programma-lezione" method="POST">
        <label for="data">Data della Lezione:</label>
        <input type="date" id="data" name="data" required>

        <label for="ora">Ora della Lezione:</label>
        <input type="time" id="ora" name="ora" required>

        <label for="classe">Classe:</label>
        <select id="classe" name="classe" required>
            <option value="">Seleziona la classe</option>
            <option value="1D">1D</option>
            <option value="2D">2D</option>
            <option value="3D">3D</option>
            <option value="4D">4D</option>
            <!-- Aggiungi altre classi qui -->
        </select>

        <label for="materia">Materia:</label>
        <select id="materia" name="materia" required>
            <option value="">Seleziona la materia</option>
            <option value="Economia e Diritto">Economia e Diritto</option>
            <option value="Educazione alla Cittadinanza">Educazione alla Cittadinanza</option>
            <option value="Educazione Motoria">Educazione Motoria</option>
            <option value="Informatica">Informatica</option>
            <option value="Laboratorio Hardware">Laboratorio Hardware</option>
            <option value="Laboratorio Reti e Sistemi">Laboratorio Reti e Sistemi</option>
            <option value="Lingua Inglese">Lingua Inglese</option>
            <option value="Lingua Italiana">Lingua Italiana</option>
            <option value="Linguaggi di Programmazione">Linguaggi di Programmazione</option>
            <option value="Matematica">Matematica</option>
            <option value="Religione Cattolica-Alternativa">Religione Cattolica-Alternativa</option>
            <option value="Ricerca Attiva del Lavoro">Ricerca Attiva del Lavoro</option>
            <option value="Scienze">Scienze</option>
            <option value="Storia-Geografia">Storia e Geografia</option>
            <option value="Tecnologia Informatica e Sistemi Operativi(teoria)">Tecnologia Informatica e Sistemi Operativi(teoria)</option>
            <!-- Aggiungi altre materie qui -->
        </select>

        <label for="argomento">Argomento della Lezione:</label>
        <textarea id="argomento" name="argomento" rows="5" placeholder="Inserisci l'argomento della lezione..." required></textarea>


        <button type="submit">Salva Pianificazione</button>
    </form>

    <h1>Inserimento Voti</h1>
    <form action="/registra-voto" method="POST">
        <label for="studente">Studente:</label>
        <select id="studente" name="studente" required>
            <option value="">Seleziona uno studente</option>
            <option value="Jibran Abbas">Jibran Abbas</option>
            <option value="Ali Abdelkader">Ali Abdelkader</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi</option>
            <option value="Alessandro Belloni">Alessandro Belloni</option>
            <option value="Giulia Brambilla">Giulia Brambilla</option>
            <option value="Maira Cozzolino">Maira Cozzolino</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro</option>
            <option value="Anthony De Lucia">Anthony De Lucia</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia</option>
            <option value="Mattia Franco">Mattia Marino</option>
            <option value="Rifat Hossein">Rifat Hossein</option>
            <option value="Mattia Marino">Mattia Marino</option>
            <option value="Dylan Moffa">Dylan Moffa</option>
            <option value="Matteo Molica">Matteo Molica</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa</option>
            <option value="Ruben Natale">Ruben Natale</option>
            <option value="Karim Ramoun">Karim Ramoun</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk"></option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elasyed Ahmed Mohamed Sallam</option>
            <option value="Abu Talha">Abu Talha</option>
            <!-- Aggiungi altri studenti qui -->
        </select>

        <label for="classe">Classe:</label>
        <select id="classe" name="classe" required>
            <option value="">Seleziona la classe</option>
            <option value="1D">1D</option>
            <option value="2D">2D</option>
            <option value="3D">3D</option>
            <option value="4D">4D</option>
            <!-- Aggiungi altre classi qui -->
        </select>

        <label for="tipo-valutazione">Tipo di Valutazione:</label>
        <select id="tipo-valutazione" name="tipo-valutazione" required>
            <option value="">Seleziona il tipo</option>
            <option value="Verifica">Verifica</option>
            <option value="Interrogazione">Interrogazione</option>
            <option value="Progetto">Progetto</option>
            <option value="Altro">Altro</option>
        </select>

        <label for="voto">Voto:</label>
        <input type="number" id="voto" name="voto" min="30" max="100" step="6" placeholder="Inserisci il voto (es. 56)" required>

        <label for="commento">Commento:</label>
        <textarea id="commeno"t name="commento" rows="3" placeholder="Inserisci commenti..."></textarea>

        <button type="submit">Registra Voto</button>
    </form>
    <h1>Tracciamento Valutazioni</h1>
    <form action="/consulta-valutazioni" method="GET">
        <label for="studente">Seleziona Studente:</label>
        <select id="studente" name="studente" required>
            <option value="">Scegli uno studente</option>
            <option value="Jibran Abbas">Jibran Abbas</option>
            <option value="Ali Abdelkader">Ali Abdelkader</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi</option>
            <option value="Alessandro Belloni">Alessandro Belloni</option>
            <option value="Giulia Brambilla">Giulia Brambilla</option>
            <option value="Maira Cozzolino">Maira Cozzolino</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro</option>
            <option value="Anthony De Lucia">Anthony De Lucia</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia</option>
            <option value="Mattia Franco">Mattia Marino</option>
            <option value="Rifat Hossein">Rifat Hossein</option>
            <option value="Mattia Marino">Mattia Marino</option>
            <option value="Dylan Moffa">Dylan Moffa</option>
            <option value="Matteo Molica">Matteo Molica</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa</option>
            <option value="Ruben Natale">Ruben Natale</option>
            <option value="Karim Ramoun">Karim Ramoun</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk"></option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elasyed Ahmed Mohamed Sallam</option>
            <option value="Abu Talha">Abu Talha</option>
            <!-- Aggiungi altri studenti qui -->
        </select>

        <button type="submit">Consulta Storico</button>
    </form>

    <h2>Voti dei Studenti</h2>
    <title>Inserimento Voti</title>
         pause
    <table>
        <thead>
            <tr>
                <th>Data</th>
                <th>Materia</th>
                <th>Tipo di Valutazione</th>
                <th>Voto</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>10/01/2025</td>
                <td>Matematica</td>
                <td>Verifica</td>
                <td>8.5</td>
            </tr>
            <tr>
                <td>05/01/2025</td>
                <td>Italiano</td>
                <td>Interrogazione</td>
                <td>7.0</td>
            </tr>
            <tr>
                <td>20/12/2024</td>
                <td>Inglese</td>
                <td>Progetto</td>
                <td>9.0</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="3" class="average">Media:</td>
                <td class="average">8.2</td>
            </tr>
        </tfoot>
    </table>
    <h1>Registrazione Presenze</h1>
    <form action="/registra-presenze" method="POST">
        <label for="classe">Classe:</label>
        <select id="classe" name="classe" required>
            <option value="">Seleziona la classe</option>
            <option value="1D">1D</option>
            <option value="2D">2D</option>
            <option value="3D">3D</option>
            <option value="4D">4D</option>
            <!-- Aggiungi altre classi qui -->
        </select>

        <label for="data">Data:</label>
        <input type="date" id="data" name="data" required>

        <table>
            <thead>
                <tr>
                    <th>Studente</th>
                    <th>Presente</th>
                    <th>Assente</th>
                    <th>Ritardo</th>
                    <th>Uscita Anticipata</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Jibran Abbas</td>
                    <td><input type="radio" name="stato[1]" value="Presente" required></td>
                    <td><input type="radio" name="stato[1]" value="Assente" required></td>
                    <td><input type="radio" name="stato[1]" value="Ritardo" required></td>
                    <td><input type="radio" name="stato[1]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Ali Abdelkader</td>
                    <td><input type="radio" name="stato[2]" value="Presente" required></td>
                    <td><input type="radio" name="stato[2]" value="Assente" required></td>
                    <td><input type="radio" name="stato[2]" value="Ritardo" required></td>
                    <td><input type="radio" name="stato[2]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Andrea Vittorio Anastasi</td>
                    <td><input type="radio" name="stato[3]" value="Presente" required></td>
                    <td><input type="radio" name="stato[3]" value="Assente" required></td>
                    <td><input type="radio" name="stato[3]" value="Ritardo" required></td>
                    <td><input type="radio" name="stato[3]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                <td>Alessandro Belloni</td>
                    <td><input type="radio" name="stato[4]" value="Presente" required></td>
                    <td><input type="radio" name="stato[4]" value="Assente" required></td>
                    <td><input type="radio" name="stato[4]" value="Ritardo" required></td>
                    <td><input type="radio" name="stato[4]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Giulia Brambilla</td>
                        <td><input type="radio" name="stato[5]" value="Presente" required></td>
                        <td><input type="radio" name="stato[5]" value="Assente" required></td>
                        <td><input type="radio" name="stato[5]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[5]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Maira Cozzolino</td>
                        <td><input type="radio" name="stato[6]" value="Presente" required></td>
                        <td><input type="radio" name="stato[6]" value="Assente" required></td>
                        <td><input type="radio" name="stato[6]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[6]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Domenico Cutroneo</td>
                        <td><input type="radio" name="stato[7]" value="Presente" required></td>
                        <td><input type="radio" name="stato[7]" value="Assente" required></td>
                        <td><input type="radio" name="stato[7]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[7]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Michele D'Alessandro</td>
                        <td><input type="radio" name="stato[8]" value="Presente" required></td>
                        <td><input type="radio" name="stato[8]" value="Assente" required></td>
                        <td><input type="radio" name="stato[8]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[8]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Anthony De Lucia</td>
                        <td><input type="radio" name="stato[9]" value="Presente" required></td>
                        <td><input type="radio" name="stato[9]" value="Assente" required></td>
                        <td><input type="radio" name="stato[9]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[9]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Anthony Giuseppe Diaz Villoslado</td>
                        <td><input type="radio" name="stato[10]" value="Presente" required></td>
                        <td><input type="radio" name="stato[10]" value="Assente" required></td>
                        <td><input type="radio" name="stato[10]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[10]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Michelangelo Espinoza Valverde</td>
                        <td><input type="radio" name="stato[11]" value="Presente" required></td>
                        <td><input type="radio" name="stato[11]" value="Assente" required></td>
                        <td><input type="radio" name="stato[11]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[11]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Giovanni Ezechia</td>
                        <td><input type="radio" name="stato[12]" value="Presente" required></td>
                        <td><input type="radio" name="stato[12]" value="Assente" required></td>
                        <td><input type="radio" name="stato[12]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[12]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Rifat Hossein</td>
                        <td><input type="radio" name="stato[13]" value="Presente" required></td>
                        <td><input type="radio" name="stato[13]" value="Assente" required></td>
                        <td><input type="radio" name="stato[13]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[13]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Mattia Marino</td>
                        <td><input type="radio" name="stato[14]" value="Presente" required></td>
                        <td><input type="radio" name="stato[14]" value="Assente" required></td>
                        <td><input type="radio" name="stato[14]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[14]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Dylan Moffa</td>
                        <td><input type="radio" name="stato[15]" value="Presente" required></td>
                        <td><input type="radio" name="stato[15]" value="Assente" required></td>
                        <td><input type="radio" name="stato[15]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[15]" value="Uscita Anticipata" required></td>
                </tr>                                        
                <tr>
                    <td>Matteo Molica</td>
                        <td><input type="radio" name="stato[16]" value="Presente" required></td>
                        <td><input type="radio" name="stato[16]" value="Assente" required></td>
                        <td><input type="radio" name="stato[16]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[16]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Ayat Azab Gabr Abdelmaksoud Moussa</td>
                        <td><input type="radio" name="stato[17]" value="Presente" required></td>
                        <td><input type="radio" name="stato[17]" value="Assente" required></td>
                        <td><input type="radio" name="stato[17]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[17]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Ruben Natale</td>
                        <td><input type="radio" name="stato[18]" value="Presente" required></td>
                        <td><input type="radio" name="stato[18]" value="Assente" required></td>
                        <td><input type="radio" name="stato[18]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[18]" value="Uscita Anticipata" required></td>
                </tr> 
                <tr>
                    <td>Karim Ramoun</td>
                        <td><input type="radio" name="stato[19]" value="Presente" required></td>
                        <td><input type="radio" name="stato[19]" value="Assente" required></td>
                        <td><input type="radio" name="stato[19]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[19]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Amro Kamel Abdeltawwab Abdelaziz Rezk</td>
                        <td><input type="radio" name="stato[20]" value="Presente" required></td>
                        <td><input type="radio" name="stato[20]" value="Assente" required></td>
                        <td><input type="radio" name="stato[20]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[20]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Zeyad Elsayed Ahmed Mohamed Sallam</td>
                        <td><input type="radio" name="stato[21]" value="Presente" required></td>
                        <td><input type="radio" name="stato[21]" value="Assente" required></td>
                        <td><input type="radio" name="stato[21]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[21]" value="Uscita Anticipata" required></td>
                </tr>
                <tr>
                    <td>Abu Talha</td>
                        <td><input type="radio" name="stato[22]" value="Presente" required></td>
                        <td><input type="radio" name="stato[22]" value="Assente" required></td>
                        <td><input type="radio" name="stato[22]" value="Ritardo" required></td>
                        <td><input type="radio" name="stato[22]" value="Uscita Anticipata" required></td>
                </tr>
                <!-- Aggiungi altri studenti qui -->
            </tbody>
        </table>

        <button type="submit">Registra Presenze</button>
    </form>
</body>
</html>

<body>
    <h1>Inserimento Motivazioni Assenze</h1>
    <form action="/inserisci-motivazione" method="POST">
        <label for="studente">Seleziona Studente:</label>
        <select id="studente" name="studente" required>
            <option value="Jibran Abbas">Jibran Abbas</option>
            <option value="Ali Abdelkader">Ali Abdelkader</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi</option>
            <option value="Alessandro Belloni">Alessandro Belloni</option>
            <option value="Giulia Brambilla">Giulia Brambilla</option>
            <option value="Maira Cozzolino">Maira Cozzolino</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro</option>
            <option value="Anthony De Lucia">Anthony De Lucia</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia</option>
            <option value="Mattia Franco">Mattia Marino</option>
            <option value="Rifat Hossein">Rifat Hossein</option>
            <option value="Mattia Marino">Mattia Marino</option>
            <option value="Dylan Moffa">Dylan Moffa</option>
            <option value="Matteo Molica">Matteo Molica</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa</option>
            <option value="Ruben Natale">Ruben Natale</option>
            <option value="Karim Ramoun">Karim Ramoun</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk"></option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elasyed Ahmed Mohamed Sallam</option>
            <option value="Abu Talha">Abu Talha</option>
            <!-- Aggiungi altri studenti qui -->
        </select>

        <label for="data">Data dell'Assenza:</label>
        <input type="date" id="data" name="data" required>

        <label for="tipo-assenza">Tipo di Assenza:</label>
        <select id="tipo-assenza" name="tipo-assenza" required>
            <option value="Assenza">Assenza</option>
            <option value="Ritardo">Ritardo</option>
            <option value="Uscita Anticipata">Uscita Anticipata</option>
        </select>

        <label for="motivazione">Motivazione:</label>
        <textarea id="motivazione" name="motivazione" rows="4" placeholder="Inserisci la motivazione fornita dallo studente..." required></textarea>

        <button type="submit">Registra Motivazione</button>
    </form>

    <h2>Motivazioni Inserite</h2>
    <table>
        <tbody>
            <tr>
                <label for="studente">Seleziona Studente:</label>
        <select id="studente" name="studente" required>
            <option value="Jibran Abbas">Jibran Abbas</option>
            <option value="Ali Abdelkader">Ali Abdelkader</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi</option>
            <option value="Alessandro Belloni">Alessandro Belloni</option>
            <option value="Giulia Brambilla">Giulia Brambilla</option>
            <option value="Maira Cozzolino">Maira Cozzolino</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro</option>
            <option value="Anthony De Lucia">Anthony De Lucia</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia</option>
            <option value="Rifat Hossein">Rifat Hossein</option>
            <option value="Mattia Marino">Mattia Marino</option>
            <option value="Dylan Moffa">Dylan Moffa</option>
            <option value="Matteo Molica">Matteo Molica</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa</option>
            <option value="Ruben Natale">Ruben Natale</option>
            <option value="Karim Ramoun">Karim Ramoun</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk"></option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elasyed Ahmed Mohamed Sallam</option>
            <option value="Abu Talha">Abu Talha</option>
                <label for="data">Data dell'Assenza:</label>
            </tr>
                <label for="data">Data:</label>
                <input type="date" id="data" name="data" required>
                <label for="Tipo">Tipo:</label>
        <select id="Tipo" name="Tipo" required>
            <option value="Quale Tipo">Quale TIpo</option>
            <option value="Presente">Presente</option>
            <option value="Assente">Assente</option>
            <option value="Ritardo">Ritardo</option>
            <option value="Uscita Anticipata">Uscita Anticipata</option>
                <textarea id="Motivo" name="Motivo" rows="3" placeholder="Inserisci Motivo..."></textarea>            
            </tr>

<body>
    <h1>Riepilogo Frequenza</h1>
    
        <select id="classe" name="classe">
            <option value="">Seleziona una classe</option>
            <option value="1D">1D</option>
            <option value="2D">2D</option>
            <option value="3D">3D</option>
            <option value="4D">4D</option>
            <!-- Altre classi -->
        </select>

        <label for="studente">Studente (se applicabile):</label>
        <select id="studente" name="studente">
            <option value="">Seleziona uno studente</option>
            <option value="Jibran Abbas">Jibran Abbas</option>
            <option value="Ali Abdelkader">Ali Abdelkader</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi</option>
            <option value="Alessandro Belloni">Alessandro Belloni</option>
            <option value="Giulia Brambilla">Giulia Brambilla</option>
            <option value="Maira Cozzolino">Maira Cozzolino</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro</option>
            <option value="Anthony De Lucia">Anthony De Lucia</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia</option>
            <option value="Mattia Franco">Mattia Marino</option>
            <option value="Rifat Hossein">Rifat Hossein</option>
            <option value="Mattia Marino">Mattia Marino</option>
            <option value="Dylan Moffa">Dylan Moffa</option>
            <option value="Matteo Molica">Matteo Molica</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa</option>
            <option value="Ruben Natale">Ruben Natale</option>
            <option value="Karim Ramoun">Karim Ramoun</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk"></option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elasyed Ahmed Mohamed Sallam</option>
            <option value="Abu Talha">Abu Talha</option>
            <!-- Altri studenti -->
        </select>

        <button type="submit">Visualizza Report</button>
    </form>

    <!-- Sezione del report di frequenza -->
    <h2>Report di Frequenza</h2>
    <div class="report-header">Classe: 2D | Periodo: 2024/2025
        </div>
    <table>
        <thead>
            <tr>
                <th>Studente</th>
                <th>Assenze</th>
                <th>Ritardi</th>
                <th>Uscite Anticipate</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Jibran Abbas</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Ali Abdelkader</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Andrea Vittorio Anastasi</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Alessandro Belloni</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Giulia Brambilla</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Maira Cozzolino</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Domenico Cutroneo</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Michele D'Alessandro</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Anthony De Lucia</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Anthony Giuseppe Diaz Villoslado</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Michelangelo Espinoza Valverde</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Giovanni Ezechia</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Mattia Franco</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>

            <tr>
                <td>Rifat Hossein</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Mattia Marino</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Dylan Moffa</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Matteo Molica</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Ayat Azab Gabr Abdelmaksoud Moussa</td>
                <td>65</td>
                <td>1</td>
                <td>4</td>
            </tr>
            <tr>
                <td>Ruben Natale</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Karim Ramoun</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Amro Kamel Abdeltawwab Abdelaziz Rezk</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Zeyad Elsayed Ahmed Mohamed Sallam</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>Abu Talha</td>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <!-- Altri studenti -->
        </tbody>
    </table>
</body>
</html>

<body>
    <h1>Invio Comunicazioni agli Studenti</h1>
    
    <!-- Form per invio comunicazioni -->
    <form id="comunicazioni-form" action="/invia-comunicazione" method="POST">
        <label for="classe">Classe:</label>
        <select id="classe" name="classe" required>
            <option value="">Seleziona una classe</option>
            <option value="1D">1D</option>
            <option value="2D">2D</option>
            <option value="3D">3D</option>
            <option value="4D">4D</option>
            <!-- Aggiungi altre classi -->
        </select>

        <label for="destinatario">Destinatario:</label>
        <select id="destinatario" name="destinatario" required>
            <option value="tutti">Tutti gli studenti</option>
            <option value="Jibran Abbas">Jibran Abbas</option>
            <option value="Ali Abdelkader">Ali Abdelkader</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi</option>
            <option value="Alessandro Belloni">Alessandro Belloni</option>
            <option value="Giulia Brambilla">Giulia Brambilla</option>
            <option value="Maira Cozzolino">Maira Cozzolino</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro</option>
            <option value="Anthony De Lucia">Anthony De Lucia</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia</option>
            <option value="Mattia Franco">Mattia Marino</option>
            <option value="Rifat Hossein">Rifat Hossein</option>
            <option value="Mattia Marino">Mattia Marino</option>
            <option value="Dylan Moffa">Dylan Moffa</option>
            <option value="Matteo Molica">Matteo Molica</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa</option>
            <option value="Ruben Natale">Ruben Natale</option>
            <option value="Karim Ramoun">Karim Ramoun</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk"></option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elasyed Ahmed Mohamed Sallam</option>
            <option value="Abu Talha">Abu Talha</option>
            <!-- Aggiungi altri studenti -->
        </select>

        <label for="oggetto">Oggetto:</label>
        <input type="text" id="oggetto" name="oggetto" placeholder="Inserisci l'oggetto della comunicazione" required>

        <label for="messaggio">Messaggio:</label>
        <textarea id="messaggio" name="messaggio" rows="5" placeholder="Scrivi il tuo messaggio qui..." required></textarea>

<html lang="it">
<head>
<body>
    <h1>Invia Comunicazioni ai Genitori</h1>
    
    <!-- Form per invio comunicazioni ai genitori -->
    <form id="comunicazioni-genitori-form" action="/invia-comunicazione-genitori" method="POST">
        <label for="classe">Classe:</label>
        <select id="classe" name="classe" required>
            <option value="">Seleziona una classe</option>
            <option value="1D">1D</option>
            <option value="2D">2D</option>
            <option value="3D">3D</option>
            <option value="4D">4D</option>
            <!-- Aggiungi altre classi -->
        </select>

        <label for="genitore">Genitore:</label>
        <select id="genitore" name="genitore" required>
            <option value="Jibran Abbas">Jibran Abbas (Genitore di Jibran Abbas)</option>
            <option value="Ali Abdelkader">Ali Abdelkader (Genitore di Ali Abdelkader)</option>
            <option value="Andrea Vittorio Anastasi">Andrea Vittorio Anastasi (Genitore di Andrea Vittorio Anastasi)</option>
            <option value="Alessandro Belloni">Alessandro Belloni (Genitore di Alessandro Belloni)</option>
            <option value="Giulia Brambilla">Giulia Brambilla (Genitore di Giulia Brambilla)</option>
            <option value="Maira Cozzolino">Maira Cozzolino (Genitore di Maira Cozzolino)</option>
            <option value="Domenico Cutroneo">Domenico Cutroneo (Genitore di Domenico Cutroneo)</option>
            <option value="Michele D'Alessandro">Michele D'Alessandro (Genitore di Michele D'Alessandro)</option>
            <option value="Anthony De Lucia">Anthony De Lucia (Genitore di Anthony De Lucia)</option>
            <option value="Anthony Giuseppe Diaz Villoslado">Anthony Giuseppe Diaz Villoslado (Genitore di Anthony Giuseppe Diaz Villoslado)</option>
            <option value="Michelangelo Espinoza Valverde">Michelangelo Espinoza Valverde (Genitore di Michelangelo Espinoza Valverde)</option>
            <option value="Giovanni Ezechia">Giovanni Ezechia (Genitore di Giovanni Ezechia)</option>
            <option value="Mattia Franco">Mattia Franco (Genitore di Mattia Franco)</option>
            <option value="Rifat Hossein">Rifat Hossein (Genitore di Rifat Hossein)</option>
            <option value="Mattia Marino">Mattia Marino (Genitore di Mattia Marino)</option>
            <option value="Dylan Moffa">Dylan Moffa (Genitore di Dylan Moffa)</option>
            <option value="Matteo Molica">Matteo Molica (Genitore di Matteo Molica)</option>
            <option value="Ayat Azab Gabr Abdelmaksoud Moussa">Ayat Azab Gabr Abdelmaksoud Moussa (Genitore di Ayat Azab Gabr Abdelmaksoud Moussa)</option>
            <option value="Ruben Natale">Ruben Natale (Genitore di Ruben Natale)</option>
            <option value="Karim Ramoun">Karim Ramoun (Genitore di Karim Ramoun)</option>
            <option value="Amro Kamel Abdeltawwab Abdelaziz Rezk">Amro Kamel Abdeltawwab Abdelaziz Rezk (Genitore di Amro Kamel Abdeltawwab Abdelaziz Rezk)</option>
            <option value="Zeyad Elsayed Ahmed Mohamed Sallam">Zeyad Elsayed Ahmed Mohamed Sallam (Genitore di Zeyad Elsayed Ahmed Mohamed Sallam)</option>
            <option value="Abu Talha">Abu Talha (Genitore di Abu Talha)</option>
            <!-- Aggiungi altri genitori -->
        </select>

        <label for="tipo-comunicazione">Tipo di Comunicazione:</label>
        <select id="tipo-comunicazione" name="tipo-comunicazione" required>
            <option value="valutazioni">Valutazioni</option>
            <option value="comportamento">Comportamento</option>
            <option value="Colloquio">Colloquio</option>
            <option value="evento">Evento scolastico</option>
        </select>

        <label for="messaggio">Messaggio:</label>
        <textarea id="messaggio" name="messaggio" rows="5" placeholder="Scrivi il tuo messaggio qui..." required></textarea>

        <button type="submit">Invia Comunicazione</button>
    </form>
