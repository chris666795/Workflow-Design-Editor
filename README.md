# UML Editor（Java Swing）

本專案為使用 Java Swing 實作的 UML 編輯器，支援 UML 物件建立、連線繪製、選取操作，以及點擊 port 進行連線 highlight。

---

## 📁 專案結構

```
.
├── src/
│   ├── bgWork/
│   ├── mod/
│   ├── Listener/
│   ├── Define/
│   ├── MsgBox/
│   └── Pack/
├── bin/
├── icon/
```

---

## 🛠 環境需求

- Java JDK 8 以上
- macOS / Linux / Windows

---

## 🚀 執行方式


### 1. 編譯

```bash
javac -d bin $(find src -name "*.java")
```

### 2. 執行

```bash
java -cp bin bgWork.Launcher
```

---

## 🧠 執行說明

主程式位於：

```
src/bgWork/Launcher.java
```

編譯後：

```
bin/bgWork/Launcher.class
```

因此需使用：

```bash
java -cp bin bgWork.Launcher
```

---

## 🖥 功能介紹

### UML 物件
- Class（矩形）
- Use Case（橢圓）

### UML 連線
- Association
- Generalization
- Composition
- Dependency（可擴充）

### 操作功能
- 點擊選取
- 拖曳移動
- 框選
- 群組 / 取消群組

### Highlight 功能（重點）

在 Select 模式下：

1. 點擊物件的 port（上下左右）
2. 對應連線會被 highlight（變色）
3. 點擊空白處會取消 highlight

---

## 🧩 系統架構

- Core / CoreMgr：系統初始化與控制
- CanvasPanelHandler：畫布操作（物件、連線、highlight）
- FuncPanelHandler：工具列控制
- Line Classes：各類 UML 線條

---

## 📌 注意事項

- 請確保 `icon/` 資料夾與專案在同一層
- 請在專案根目錄執行程式

---

## 🎯 Demo 操作流程

1. 選擇工具（左側）
2. 點擊畫布建立物件
3. 拖曳建立連線
4. 切換 Select 模式
5. 點擊 port → highlight
6. 點擊空白 → 清除

