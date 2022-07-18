---
layout: post
---

<div style="text-align:right;"><a href="/d-d-d.html"><<< Back To Menu</a><br/></div>

# 領域模型 <br/>
  > 模型來自於專案成員的「概念」，包含「類別」和「主要操作」，
  > 用以承載**非程式碼**的設計

## 為何要使用領域模型?
  - 表達方式的差異會造成溝通鴻溝
    - 領域專家：使用**專業術語** <br/>
      -> 無法精確描述「想要」的東西
    - 開發人員：使用**描述性**、**功能性**的術語<br/>
      -> 領域專家無法理解其抽象概念
  - 翻譯成本：
    - 部分成員可以同時理解兩方敘述：容易成為資訊流的瓶頸，且翻譯不見得精確
    - 開發人員試圖理解領域知識：頂多形成模糊的認知
    - 開發人員彼此間可能各自使用不同的描述方式
    - 不同領域專家之間使用的術語不完全相同<br/>
    > 翻譯成本存在於**領域專家和領域專家**、**領域專家和開發人員**、**開發人員和開發人員**之間
  - 團隊中存在不通用的術語：<br/>
    **<font color="#FFA042">會使系統的各部分變得不相容，會造成混淆甚至導致錯誤的重構，</font>**<br/>
    **<font color="#FFA042">且對領域的深刻表述在溝通中累積</font>**
  
   > **為了建立共通語言而使用領域模型**
<br/>

---

## 如何建立團隊的共通語言(Ubiquitous Language)?
  **[基本工具範例]**
  1. UML圖<br/>
     易於表達關聯，但無法表示「概念」或「行為」，<br/> 適合用來快速理解要討論的範圍，但還需要其他輔助
  2. 程式碼<br/>
     明確且詳實的紀錄了所有細節，可信度最高，<br/>
     但不易理解，且難以用其他方式描述
  3. 文件<br/>
     輔助說明，目的在讓閱讀者快速建立「架構」認知，並知道專案和系統的「核心」和設計意圖， **不應用來記錄其他工具已經表達的內容**<br/>
     ※ 須留意：如文件術語不再出現在討論中，表示文件未發揮作用，<br/>
     **<font color="#FFA042">則應該要淘汰</font>** (保留須花費額外心力更新文件，不更新則會造成混淆而損害專案)<br/>
     ※ 如是因為共通語言逐漸建立而不再需要文件輔助，也可以進行淘汰
  4. 解釋性模型<br/>
     不需像領域模型經過嚴格的精練，表達形式自由，旨在容易理解，學習成本低，用以作為輔助領域模型的工具
     
  **<font color="#FFA042"> ※※※單一的使用任何方式都有其風險※※※ </font>**
  - 只用UML圖：太過詳盡反而無法消化，看不出重點，徒增溝通成本
  - 只用程式碼：對於非技術人員來說無法理解，且雖行為明確，但命名方式、撰寫風格可能不盡相同，就算使用大量的口語輔助，認知也往往只留在當下
  - 只使用文件：知識分散，無法將專案內容組織起來
  - 文件不同步問題：外在文件、註解都不影響程式碼的實際運作，往往疏於管理導致描述內容不同步

  > **建立共通語言，並使其成為領導專案討論的文件**

---

<div style="text-align:right;"><a href="/d-d-d.html"><<< Back To Menu</a><br/></div>