# Análise Exploratória - Campeonato Espanhol de Futebol (La Liga)

## 📋 Descrição do Projeto

Este projeto realiza uma análise exploratória completa dos dados do Campeonato Espanhol de Futebol (La Liga) entre as temporadas 2015/2016 e 2023/2024. O objetivo é investigar padrões históricos, verificar citações comuns do futebol e analisar o desempenho dos times campeões espanhóis.

## 🎯 Objetivos

A análise busca responder às seguintes perguntas:

- **Quais são os 10 clubes com mais vitórias no histórico do campeonato?**
- **Qual o total de gols marcados por times da casa em comparação com times visitantes?**
- **Qual é a média de gols por partida e como esses gols se distribuem?**
- **Qual é a distribuição percentual de vitórias da casa, empates e vitórias do visitante?**
- **Como as médias de cartões amarelos, vermelhos, faltas, escanteios, chutes ao gol, tiro livre, bolas na trave e impedimento variaram ao longo das temporadas?**
- **A porcentagem de vitórias dos times da casa mudou significativamente ao longo das temporadas?**

## 📊 Dataset

### Fonte dos Dados
Os dados foram obtidos do [football-data.co.uk](https://www.football-data.co.uk/brazil.php), contendo informações detalhadas sobre o campeonato espanhol de futebol.

### Período Analisado
- **Temporadas**: 2015/2016 a 2023/2024
- **Total de partidas**: 3.420 jogos
- **Divisão**: Primeira Divisão (La Liga)

### Dicionário dos Dados

#### Resultados das Partidas:
- `Div` = Divisão da Liga
- `Date` = Data da Partida (dd/mm/aa)
- `Time` = Horário de início da partida
- `HomeTeam` = Time da Casa (Mandante)
- `AwayTeam` = Time Visitante
- `FTHG` e `HG` = Gols do Time da Casa ao Final do Jogo
- `FTAG` e `AG` = Gols do Time Visitante ao Final do Jogo
- `FTR` e `Res` = Resultado Final (H=Vitória da Casa, D=Empate, A=Vitória do Visitante)
- `HTHG` = Gols do Time da Casa no Primeiro Tempo
- `HTAG` = Gols do Time Visitante no Primeiro Tempo
- `HTR` = Resultado no Primeiro Tempo (H=Vitória da Casa, D=Empate, A=Vitória do Visitante)

#### Estatísticas da Partida:
- `Attendance` = Público Presente
- `Referee` = Árbitro da Partida
- `HS` = Chutes (Finalizações) do Time da Casa
- `AS` = Chutes (Finalizações) do Time Visitante
- `HST` = Chutes a Gol do Time da Casa
- `AST` = Chutes a Gol do Time Visitante
- `HHW` = Bolas na Trave do Time da Casa
- `AHW` = Bolas na Trave do Time Visitante
- `HC` = Escanteios do Time da Casa
- `AC` = Escanteios do Time Visitante
- `HF` = Faltas Cometidas pelo Time da Casa
- `AF` = Faltas Cometidas pelo Time Visitante
- `HFKC` = Tiros Livres Sofridos pelo Time da Casa
- `AFKC` = Tiros Livres Sofridos pelo Time Visitante
- `HO` = Impedimentos do Time da Casa
- `AO` = Impedimentos do Time Visitante
- `HY` = Cartões Amarelos do Time da Casa
- `AY` = Cartões Amarelos do Time Visitante
- `HR` = Cartões Vermelhos do Time da Casa
- `AR` = Cartões Vermelhos do Time Visitante
- `HBP` = Pontos de Cartão do Time da Casa (10 = amarelo, 25 = vermelho)
- `ABP` = Pontos de Cartão do Time Visitante (10 = amarelo, 25 = vermelho)

## 🔍 Principais Descobertas

### Top 10 Clubes com Mais Vitórias
1. **Barcelona** - 351 vitórias
2. **Real Madrid** - 335 vitórias
3. **Atlético Madrid** - 329 vitórias
4. **Sevilla** - 234 vitórias
5. **Athletic Bilbao** - 207 vitórias

### Análise de Gols
- **Mandantes** marcam significativamente mais gols que visitantes
- **50% das partidas** têm 2 gols ou menos
- **25% das partidas** têm 4 gols ou mais
- Média de **23 chutes por equipe** por partida
- Média de **8 chutes no alvo** por equipe por partida

### Fator Casa
- **Aproveitamento médio do mandante**: 54,27%
- **Maior aproveitamento**: 56,22% (temporada 2015/2016)
- **Menor aproveitamento**: 51,14% (temporada 2020/2021)
- Historicamente, **vitórias do mandante > empates > derrotas**

### Estatísticas de Jogo
- **Média de faltas**: 28 por equipe por jogo
- **Cartões amarelos**: 75% das partidas têm 3 ou menos
- **Cartões vermelhos**: Relativamente baixos na maioria dos jogos

## 🛠️ Tecnologias Utilizadas

- **Python** 3.x
- **Pandas** - Manipulação e análise de dados
- **Matplotlib** - Criação de gráficos
- **Seaborn** - Visualizações estatísticas
- **NumPy** - Computação numérica
- **Gradio** - Dashboard interativo

## 📁 Estrutura do Projeto

```
projeto-gol/
├── README.md                    # Este arquivo
├── aula.ipynb                   # Notebook principal com a análise
├── dados-20250813T122016Z-1-001.zip  # Arquivo compactado com os dados
└── dashboard.py                 # Script do dashboard interativo (se aplicável)
```

## 🚀 Como Executar

### Pré-requisitos
```bash
pip install pandas matplotlib seaborn numpy gradio
```

### Executando a Análise
1. **Extraia os dados** do arquivo `dados-20250813T122016Z-1-001.zip`
2. **Abra o notebook** `aula.ipynb` no Jupyter ou Google Colab
3. **Execute as células** sequencialmente para reproduzir a análise

### Dashboard Interativo
O projeto inclui um dashboard interativo criado com Gradio que permite:
- Visualizar os top 10 clubes com mais vitórias
- Analisar distribuição de gols
- Explorar estatísticas das partidas
- Verificar o desempenho dos mandantes ao longo das temporadas

## 📈 Visualizações Incluídas

1. **Gráfico de Barras** - Top 20 clubes com mais vitórias
2. **Comparação de Gols** - Mandante vs. Visitante
3. **Boxplot e Histograma** - Distribuição de gols por partida
4. **Boxplots Múltiplos** - Estatísticas de jogo (faltas, cartões, chutes, etc.)
5. **Gráficos Temporais** - Desempenho dos mandantes por temporada

## 🤝 Contribuições

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 👨‍💻 Autor

Desenvolvido como parte de um projeto de análise de dados esportivos.

---

**Nota**: Este projeto foi desenvolvido para fins educacionais e de análise exploratória. Os dados utilizados são de domínio público e foram obtidos de fontes confiáveis. 
