Регулярное выражение для того, чтобы убрать из экспортированного файла “? и /”:
Поиск : ^.*\t[?/]\s*
Замена: (пусто)

Код для выполнения остальной части задания:

words = open("Puschino_aid2008-pos.txt", encoding="utf-8").read().splitlines()
my_stem = open("my_stem.txt", encoding="utf-8").read().splitlines()

lemmas = []
morphs = []

for a, b in zip(words, my_stem):
    a_parts = a.split("\t")
    b_parts = b.split("\t")
    layer = a_parts[0].split("@")[1]
    start, end = a_parts[1], a_parts[2]
    lemma, morph = b_parts[1], b_parts[2]


    lemmas.append(f"lemma@{layer}\t{start}\t{end}\t{lemma}")
    morphs.append(f"morph@{layer}\t{start}\t{end}\t{morph}")

open("lemma.txt", "a", encoding="utf-8").write("\n".join(lemmas))
open("morph.txt", "a", encoding="utf-8").write("\n".join(morphs))

print("Япи-япи!")



Морфологический анализатор прекрасно справился с "нормальными", "словарными" словами, но вот при анализе окказионализмов (линды, подготовишке) и нестандартно записанных междометий возникают ошибки (ааа)
P.S. (хотя со словами "музыкалке" и "ковид" справился (правильно сработала аналогия))
