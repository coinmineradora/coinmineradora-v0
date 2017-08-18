# CoinMineradora-v0.1
CoinMineradora-v0.1 é um software de mineração totalmente automatizado que monitora o pool da **www.CoinMineradora.com.br** em tempo real para procurar o algoritmo mais rentável no momento. Benchmarks para selecionar o software de mineração mais adequado ao seu equipamento. Download automático de todos os softwares de mineração necessários. **CONFIGURE, ESQUEÇA E RECEBA SEUS PAGAMENTOS EM BITCOIN (BTC)!**


**COMO CONFIGURAR E EXECUTAR**
- Abra o arquivo 'start.bat' em um editor de textos.
- Substitua o parâmetro 'wallet' pela **sua carteira Bitcoin (BTC Wallet)**.
- Começe a minerar! :-D


**NOTAS IMPORTANTES**
- Não é recomendado, mas para atualizar de uma versão anterior você pode simplesmente copiar a pasta '/Stats'
- Se você usa Windows 7, por favor atualize o PowerShell: 
https://www.microsoft.com/en-us/download/details.aspx?id=50395
- CCMiner pode precisar do arquivo 'MSVCR120.dll'. Nesse caso instale o 'Visual C++ Redistributable Packages for Visual Studio 2013' tanto na versão 32bits como 64bits: 
https://www.microsoft.com/en-gb/download/details.aspx?id=40784
- CCMiner pode precisar do arquivo 'VCRUNTIME140.DLL'. Nesse caso instale o 'Visual C++ Redistributable for Visual Studio 2015' tanto na versão 32bits como 64bits: 
https://www.microsoft.com/en-us/download/details.aspx?id=48145


**PERGUNTAS FREQUENTES (v1.0):**

P1. Um minerador trava ou não funciona corretamente no meu computador e eu quero excluí-lo da mineração. O que devo fazer?

R1. Localize o arquivo de configuração desse minerador dentro da pasta '/Miners' e apague o arquivo ou exclua totalmente o algoritmo (veja a pergunta 3 abaixo). Esses arquivos possuem extensão '.ps1'. Por favor note que alguns softwares de mineração podem possuir vários arquivos de configuração e/ou vários algotirmos habilitados.

P2. Um software de mineração diz que um dispositivo CL (CL device) está faltando ou não foi encontrado (missing or not found). Como resolvo isso?

R2. É bem provável que você só tenha placas da NVIDIA no seu computador. Abra o arquivo 'start.bat' em um editor de textos, procure pela parte '-type -amd,nvidia' e troque por '-type nvidia'. Isso vai desabilitar os softwares exclusivos para placas AMD.

P3. Eu quero minerar somente alguns algoritmos, mesmo que não seja o mais lucrativo. Quero excluir algum algoritmo. Como faço?

R3. Abra o arquivo 'start.bat' em um editor de textos, procure pela parte '-algorithm keccak,lbry,myr-gr,skunk,tribus' e apague os algoritmos que você não deseja minerar. Isso também pode salvar algum tempo de benchmarking.

P4. Quero executar novamente os benchmarks (alteração nas configs de overclock, novas placas, etc...)

R4. Localize a pasta '/Stats' e apague todos os arquivos que estão lá dentro. Isso vai forçar o software controlador do **Coin Mineradora** a executar novamente todos os benchmarks. Se vocẽ deseja executar o benchmark somente para um minerador ou algoritmo, localize e apague somente o arquivo correspondente. Por favor note que alguns softwares de mineração podem possuir vários arquivos de benchmark pelo fato de serem utilizados para mais de um algoritmo.

P5. Quanto tempo leva pra tarefa de benchmark terminar?

R5. O tempo de benchmark depende muito de quantos algoritmos w softwares de mineração foram configurados no arquivo 'start.bat'. Por padrão, cada teste de benchmark leva 90 segundos. Você pode acelerar o processo de benchmarking removendo os algoritmos ou softwares de mineração que não são otimizados para o seu equipamento. Por exemplo, se você tem um computador com placas AMD é recomendado remover os softwares específicos para NVIDIA (veja a pergunta 2).

P6. É possível escolher quantas GPUs serão alocadas para o processo de mineração?

R6. Essa funcionalidade será implementada no futuro com o lançamento da nova interface gráfica do software controlador do **Coin Mineradora**.

