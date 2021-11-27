# hse21_hw3
# Часть 1
Коллаб https://colab.research.google.com/drive/1gY2I3TDNYukWHnAc8PJXUjXa6dHRLBvZ#scrollTo=eXp-rVG3iBw9

# Проверка качества чтений из fastQC: сравнительная статистика из multiQC:
![142776373-05b11b52-924e-477f-8e98-42420cdf1f3f](https://user-images.githubusercontent.com/93148512/143722372-04590e78-573e-4513-86ab-c4cc3656eadf.png)
![142776385-9d5c4216-6283-468f-9622-ac1eb94a5b9c](https://user-images.githubusercontent.com/93148512/143722374-c4974061-71a8-42f5-8694-c50b41a2e184.png)
![142776392-b85c6c14-fe13-4f48-be6e-edde19a727b2](https://user-images.githubusercontent.com/93148512/143722377-31417bd9-3be2-4a40-b3ce-2da9d587dd84.png)
![142776411-a7a90224-7d31-4d85-8d1f-66c6afb5d872](https://user-images.githubusercontent.com/93148512/143722382-293eaade-0ed8-4726-a605-9734a4f9cbda.png)
![142776399-529eb5f7-c2de-4830-9b3b-dfb4bdf5523c-2](https://user-images.githubusercontent.com/93148512/143722435-54ab074e-297c-47d7-bd96-02550439861f.png)
![142776415-668765df-9d25-47c0-8ac1-cab95c8999c5](https://user-images.githubusercontent.com/93148512/143722385-79344ffe-30b1-402a-8664-5d1db810b3e1.png)
![142776424-64035515-e04f-4b67-a028-cbc9a12bd12f](https://user-images.githubusercontent.com/93148512/143722423-c80779a2-0a0c-4ee3-a6a0-aaa311acca24.png)

# Суммарная статистика
![142776458-f388e537-633f-4e17-bf85-0fc809f3e379](https://user-images.githubusercontent.com/93148512/143722439-6f3bf42f-4a5b-4a39-b75f-de1938112636.png)

# Количество уникально картированных чтений по каждому образцу

<img width="434" alt="Снимок экрана 2021-11-28 в 01 44 53" src="https://user-images.githubusercontent.com/93148512/143722455-536e7fe5-96c2-4d7b-8fe3-dc098a6322da.png">

# Из статистики HTSeq узнаем количество чтений соответствует участкам генома, где не аннотировано ни одного экзона и количество чтений, которые могут принадлежать разным генам

<img width="325" alt="Снимок экрана 2021-11-28 в 01 47 56" src="https://user-images.githubusercontent.com/93148512/143722508-4b832b2a-32e7-4378-ab88-b63b0c4cec8d.png">
<img width="348" alt="Снимок экрана 2021-11-28 в 01 48 14" src="https://user-images.githubusercontent.com/93148512/143722509-151c33c8-64c0-463e-a91b-abdcf2ec8995.png">

# С помощью данных, приведенных выше, можно посчитать количество чтений, соответствующих хотя бы одному гену

<img width="654" alt="Снимок экрана 2021-11-28 в 01 51 09" src="https://user-images.githubusercontent.com/93148512/143722564-759451c8-a53a-45f6-afee-81d5af887650.png">

# Наглядная статистика по каждому из 6 образцов

Образец | Тип | Количество чтений | Успешно откартированные | Уникально откартированные | Чтений на один ген
-|-|-|-|-|-
SRR3414629 | перепрограмированный | 21106089 |	20510113 (97.18%)	|	18375888 (87.06%)  | 16049609
SRR3414630 | перепрограмированный |	15244711 | 14832680 (97.30%)	|	13186139 (86.50%) |	11465324
SRR3414631 | перепрограмированный | 24244069 | 23547686 (97.13%) | 20928945 (86.33%) |	18408851
SRR3414635 | контроль | 20956475 |	20395865 (97.32%)	| 18428317 (87.94%) |	16275997
SRR3414636 | контроль | 20307147 |	19757059 (97.29%)	| 17825380 (87.78%) |	15757580
SRR3414637 | контроль | 20385570 |	19847291 (97.36%)	| 17844858 (87.54%) |	15736978

# Объединяем файлы с прочтениями в один - all_counts (столбцы - образцы, при чем c1, c2, c3 - контрольные образцы; r1, r2, r3 - перепрограммированные образцы)
<img width="681" alt="Снимок экрана 2021-11-28 в 01 54 54" src="https://user-images.githubusercontent.com/93148512/143722626-df7e8ef9-ebf7-46e7-9021-ed10a4c46b08.png">

# Часть 2
Коллаб https://colab.research.google.com/drive/1berid2-bZpcvuhPHEAkPg5Ca2HIeC7SI#scrollTo=pbrtXwc5vkGG
# MA-plot, показывающий Log2FC для генов
<img width="681" alt="Снимок экрана 2021-11-28 в 01 54 54" src="https://user-images.githubusercontent.com/93148512/143722626-df7e8ef9-ebf7-46e7-9021-ed10a4c46b08.png">
Видно, что большее количество дифференциально экспрессированных генов увеличило свою экспрессию

# Heatmap, показывающий созависимость экспрессии генов из контрольных и репрограммированных образцов
![Без названия1](https://user-images.githubusercontent.com/93148512/143723465-0e15d381-dad2-4ef5-b1d7-4c6a8f599472.png)

Видно, что экспрессия генов одинакова в одной группе образцов и отличается между группами

# Heatmap для первых 20 наиболее дифференциально экспрессированных генов

![Без названия2](https://user-images.githubusercontent.com/93148512/143723494-80376052-f918-4b92-b6ee-3f8e43e71f31.png)

Видно, что большее количество дифференциально экспрессированных генов увеличило свою экспрессию

# Графики со значениями "Normalized counts" в контрольных и перепрограммированных образцах
<img width="676" alt="Снимок экрана 2021-11-28 в 02 40 22" src="https://user-images.githubusercontent.com/93148512/143723542-e0bd5959-c215-49be-bc51-0478549e3295.png">
<img width="709" alt="Снимок экрана 2021-11-28 в 02 41 08" src="https://user-images.githubusercontent.com/93148512/143723554-4db22038-b767-4ce5-96ed-5d67d69930ed.png">
<img width="675" alt="Снимок экрана 2021-11-28 в 02 41 35" src="https://user-images.githubusercontent.com/93148512/143723580-0807730b-ed08-4532-ad2b-128f71aa629d.png">
<img width="703" alt="Снимок экрана 2021-11-28 в 02 42 34" src="https://user-images.githubusercontent.com/93148512/143723592-3c3ffa9c-fe62-4243-b1c7-00e9b54839a7.png">

Поиск генов производился с помощью сортировки по L2FC (notebook в папке source)
