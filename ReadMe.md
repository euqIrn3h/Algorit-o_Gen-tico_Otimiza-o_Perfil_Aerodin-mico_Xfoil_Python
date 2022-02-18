O algoritmo utiliza a técnica de algoritmos genéticos cartesianos prpoposta por Miller para fazer a otimização
do perfil aerodinâmico em questão. Basicamente o que o algoritmo faz é utilizar um perfil base que inicialmente
é tomado como Pai, e dele é gerado quatro Filhos contendo modificações em seus genes. Para o caso de perfis
aerodinâmicos os genes são os pares ordenados que definem a sua geometria. Após serem gerados esses perfis são
analisados no software Xfoil e seu coeficiente de eficiencia é definido. Cada um dos perfis Filhos são comparados
ao perfil Pai, caso o perfil Filho tenha um coeficiente de eficiencia melhor que o Pai ele o substitui como o
gerador da próxima geração de Filhos.

Para que o algoritmo funcione é necessário que o arquivo Evo.py esteja dentro da mesma pasta do Xfoil.exe. Também
é necessário que nessa pasta tenha os arquivos Son.txt, Script.txt, ScriptFinal.txt, Mae.txt e um arquivo de texto
contendo o perfil base que você utilizará como ponto de partida, que no nosso caso foi o Naca0010.txt. O arquivo 
Polar.txt será criado e excluido em tempo de exucução, não sendo necessário sua criação.

No algoritmo são necessários os requesitos gerações, que setam a quantidade maxima de gerações para a otimização, 
reynolds, que determina o número de reynolds para escoamentos viscosos, e faixa angular, que define o espaço angular
contendo 16 ângulos de ataque do inicial ao final e o incremento entre os ângulos. 