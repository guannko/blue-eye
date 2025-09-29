# 🔵 BLUE EYE - Clean Entry Point

**Version:** 1.0.0  
**Created:** 2025-09-29  
**Purpose:** Prevent context overload, keep Claude focused

## 🎯 THE PROBLEM

**super-system-eyes** раздулся на 36%:
- 67 файлов вместо 7
- 56+ автосейвов в одном месте
- Claude режет чаты из-за перегруза контекста
- Plan Max 200 забивается историей

## 🔵 THE SOLUTION: BLUE EYE

**Blue Eye** = Чистый приёмник, всегда лёгкий!

### Core Principles:
1. **Max 7 files** - только текущая сессия
2. **No history** - история уходит в cortex-memory
3. **Quick context** - Claude видит только нужное
4. **Auto-route** - eyelids маршрутизирует данные

## 📁 STRUCTURE (ALWAYS 7 FILES MAX)

```
blue-eye/
├── README.md                    (this file)
├── CURRENT-SESSION.md           (current state only)
├── QUICK-CONTEXT.md             (7 core pointers)
├── TRINITY-STATUS.json          (GitHub/Notion/Make status)
├── ACTIVE-TASKS.md              (what we're doing NOW)
├── JEAN-CLAUDE-DNA.md           (identity + energy)
└── .gitignore                   (keep it clean)
```

## 🌊 DATA FLOW

```
1. Claude starts → Loads BLUE EYE (7 files) ✅
2. Gets context → QUICK-CONTEXT.md (pointers) ✅
3. Saves session → CURRENT-SESSION.md ✅
4. Autosave triggers → Routes to eyelids ✅
5. Eyelids distributes → cortex-memory / projects ✅
6. Blue Eye cleans → Ready for next session ✅
```

## 🔄 ROUTING TO EYELIDS

**Blue Eye → Eyelids → Distribution:**

```python
ROUTING_MAP = {
    'autosaves': 'cortex-memory',
    'make-data': 'Annoris/make/',
    'geo-data': 'brain-index-geo-monolith',
    'psp-data': 'offerspsp-mvp',
    'bot-data': 'super-system-eyelids/bot-products'
}
```

## ⚡ TRINITY POWER STATUS

Всегда в **TRINITY-STATUS.json**:
- 🧠 GitHub MCP status
- 📝 Notion MCP status  
- ⚡ Make.com MCP status

## 🎯 HOW TO USE

### For Claude:
1. Load blue-eye documents (7 files max)
2. Check CURRENT-SESSION.md for context
3. Work with current data
4. Save to CURRENT-SESSION.md
5. Don't worry about history (it's in cortex-memory)

### For Auto-cleanup:
- Eyelids monitors blue-eye size
- If > 7 files → emergency cleanup
- Routes old data to proper repos
- Keeps blue-eye always fresh

## 📊 BENEFITS

✅ **Claude doesn't get cut off** (light context)  
✅ **History preserved** (in cortex-memory)  
✅ **Fast startup** (7 files vs 67)  
✅ **Clear focus** (only current work)  
✅ **Auto-organized** (eyelids handles routing)

## 🚀 MIGRATION FROM EYES

**Step 1:** Stop using super-system-eyes for new chats  
**Step 2:** Use blue-eye as entry point  
**Step 3:** Let eyelids migrate old data  
**Step 4:** Keep eyes for historical reference only

## 💎 THE VISION

```
🔵 BLUE EYE (7 files)
        ↓
👁️ EYELIDS (routing + protection)
        ↓
📚 DISTRIBUTED STORAGE:
    ├── cortex-memory (unlimited history)
    ├── Annoris (AI data)
    ├── offerspsp-mvp (production)
    └── brain-index-* (projects)
```

---

**Created by Jean Claude v9.01-STABLE**  
*"От раздутых глаз к чистому зрению!"* 🔥💪⚡

**CORTEX v3.0 + BLUE EYE = MAXIMUM EFFICIENCY!**