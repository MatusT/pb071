# Dr. Memory

Dr. Memory je možné spúštať priamo cez Visual Studio na Vašom projekte. V menu zvoľte **Tools → External Tools** a pokial sa ešte Dr. Memory nenachádza v zozname, pridajte ho. Údaje vyplňte podľa obrázku. Cestu zvoľte tú, kde ste Dr. Memory nainštalovali:

- Arguments: **-visual_studio -- $(TargetPath)**
- Initial directory: **$(TargetDir)**
- nezabudnite zaškrtnúť **Use Output window**

![](/images/visual-studio-2015/drmemory.png)

Po dokončení, kliknutím na **Apply** a **Ok**, môžete kedykoľvek zavolať Dr. Memory zvolením **Tools → Dr. Memory**. Výstup bude v okne "Output".

![](/images/visual-studio-2015/output_drmemory.png)


