
1) Télécharger le repertoire TP 1 Hadoop 

2) S'assurer de donner les droits d'exécutions sur les fichier mapper.py et reducer.py

3) La chaine d'exécutions du job MapRedudce 

hadoop jar /usr/lib/hadoop-mapreduce/hadoop-streaming.jar \
-input /user/hadoop/wc/input \
-output /user/hadoop/wc/output \
-file /home/hadoop/mapper.py \
-mapper /home/hadoop/mapper.py \
-file /home/hadoop/reducer.py \
-reducer /home/hadoop/reducer.py

4 ) Faire un benchmark en faisant varier le nombre de reduce tasks suivant la chaine d'exécution ci-dessous

hadoop jar /usr/lib/hadoop-mapreduce/hadoop-streaming.jar \
-input /user/hadoop/wc/input \
-output /user/hadoop/wc/output \
-file /home/hadoop/mapper.py \
-mapper /home/hadoop/mapper.py \
-file /home/hadoop/reducer.py \
-reducer /home/hadoop/reducer.py \
-jobconf mapred.reduce.tasks=3

