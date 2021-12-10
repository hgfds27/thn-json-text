# thn-json-text 各文件說明
## A區塊：修飾原文 (日文 => 日文)
### textSubtitle.json
此為修飾原文部分句子的文件，作用為將翻譯機無法正確翻譯的句子改寫成翻譯機看得懂的形式，取代時機為原文被B區塊取代前

### textJp.json
此為修飾原文詞彙的文件，作用為將翻譯機無法正確翻譯的詞彙取代為翻譯機看得懂的同義詞，取代時機為原文被B區塊取代前

### textJp2.json
此為修飾原文詞彙的文件，作用為將翻譯機無法正確翻譯的詞彙取代為翻譯機看得懂的同義詞，取代時機為原文被B區塊取代後

## B區塊：取代詞彙 (日文、英文 => 中文)
### textForceOverwrite.json
此為強制轉換整句的文件，對象句子需與此文件「完全符合」才會生效，用途為取代翻譯機完全不會翻譯的句子，英文不需要此文件

### textChName.json
此為產生臨時NPC名字的文件，臨時產生的名字會被儲存在textNameTemporary.json裡，英文不需要此文件

### textMap.json
此為地圖名字的文件，textMap、textName、textOther讀取後會合併成一個陣列

### textName.json
此為NPC名字和專有名詞的文件，textMap、textName、textOther讀取後會合併成一個陣列

### textNameTemporary.json
此為用來儲存尚未分類的臨時名字

### textOther.json
此為其他名字的文件，textMap、textName、textOther讀取後會合併成一個陣列

### textAfterTranslated.json
此為翻譯後最後修飾用的文件，也可以用來校正翻譯機不會翻譯的詞彙

## C區塊：各項參數 (日文)
### textException.json
此為無視名單，若原文含有在此文件內的任一句子皆會被略過不顯示

### player.json
此為存放玩家名字的文件

### textKana.json
此為日文假名文件，平常沒有更動的必要

### listForHira.json
此為說話會夾雜片假名或是全都片假名的NPC名單  
在此名單內的NPC對話都會先轉換成平假名再翻譯

### listOfCrystalium.json
此為隸屬水晶城的NPC名單  
因為在這裡的NPC都稱呼「水晶公」為「公」  
但「公」在日文有公共、公眾的意思  
翻譯機也都如此翻譯，導致無法翻譯出正確的意思  
因此在此名單的NPC說的「公」都會被取代成「水晶公」
