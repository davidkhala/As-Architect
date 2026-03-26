# Business Process Model and Notation (BPMN)
- business workflow model
- maintained by Object Management Group

## History
- 1.0 (2004)
- 2.0 (2011)

## Desc
1. 流程的推進（Sequence Flow）
符號：實線 + 實心箭頭。
用法：用於同一個「池」（Pool）內，表示活動執行的先後順序。
規則：它不能跨越池的邊界（不能直接從一個公司連到另一個公司）。
2. 訊息的發送（Message Flow）
符號：虛線 + 空心三角形箭頭（起點通常帶有一個小圓圈）。
用法：用於跨池（不同參與者/組織）之間的通信。
規則：它代表的是「訊息傳遞」（如：發送郵件、API 調用），只能連在池與池之間。
3. 人與步驟的關係（Association）
符號：點狀虛線（通常不帶箭頭，或僅用於數據流向）。
用法：稱為「關聯」。在 BPMN 中，人通常是以「泳道 (Lane)」來呈現，步驟（Task）直接擺放在所屬角色的道內。
補充：如果你是要把「文件」或「註釋」連結到步驟上，也是使用這種點狀虛線。

