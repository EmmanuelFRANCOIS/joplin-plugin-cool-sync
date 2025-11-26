# 🧊 Cool-Sync — Joplin Plu­g­in

**Smart unidirectional sync of a spe­cif­ic Joplin note­book to a lo­cal fold­er and/or ZIP archive**

Cool-Sync is A Joplin plugin to synchronise unidirectionally a Joplin Notebook and its entire sub-tree of elements into a local folder on hard drive...  
It pro­vides **flex­i­ble**, **se­cure**, and **au­tomat­able** syncs while main­tain­ing a na­tive Joplin look & feel.

## ✨ Key Fea­tures

- 🔄 **Three syn­chro­niza­tion modes**
    - **Spe­cif­ic Fold­er**
    - **ZIP File**
    - **Spe­cif­ic Fold­er + ZIP File**
        
- 📁 **Full struc­ture ex­port**: note­books, sub-note­books, notes (Mark­down/HTML/Text), and all as­sets.
    
- 🧠 **Se­lec­tive sync**: only new/mod­i­fied items are copied; delet­ed items are also re­moved from the tar­get di­rec­to­ry.
    
- 🔐 **Se­cure ZIP mode** with op­tion­al pass­word pro­tec­tion.
    
- 🌍 **Full in­ter­na­tion­al­iza­tion**:  
    fr-FR, en-US, de-DE, es-ES, it-IT, pt-PT, uk-UA  
    → Trans­lat­ed UI + lo­cal­ized dates/num­bers  
    (de­fault lo­cale if un­sup­port­ed: **en-US**)
    
- 🖥️ **Desk­top only** (Lin­ux, Win­dows, ma­cOS)
    
- 🛠️ **Joplin-in­te­grat­ed UI**:
    - Cool-Sync pan­el
    - Con­text menu ac­tions on note­books
    - Edit/Cre­ate di­alogs
    - Au­to­mat­ic sync tog­gle
        
- ⚙️ **Ad­vanced con­fig­u­ra­tion**:  
    ZIP com­pres­sion lev­el, sta­t­ic site gen­er­a­tion, post-back­up scripts, sync in­ter­val, at­tach­ment in­clu­sion, GitHub up­load, and more.
    
- 📦 **Mul­ti­ple Cool-Sync pro­files sup­port­ed**


## 📂 Out­put Di­rec­to­ry Struc­ture

Ex­am­ple struc­ture gen­er­at­ed on syn­chro­niza­tion:

```DOS
[target-folder]/
│   ├── ZIP/
│   │   ├── backup - Main Notebook - YYYY MM DD - hh-mm-ss.zip
│   │   ├── backup - Main Notebook - YYYY MM DD - hh-mm-ss.zip
│   │   └── ...
│   └── DATA/
│       └── [Main Notebook]/
│           ├── [Notebook]/
│           │   ├── Note.md
│           │   └── ...
│           └── ...
```

- **DATA/** → Un­en­crypt­ed fold­er-based syn­chro­niza­tion
- **ZIP/** → His­to­ry of com­pressed back­ups
- ZIP file­name pat­tern is user-con­fig­urable, e.g.:  `Cool-Sync - [Notebook] - [YYYYMMDD-HHmmss].zip`
    
## 🧭 Joplin UI In­te­gra­tion

### 📌 Menus & Ac­tions
- **Tools → Cool-Sync**
- **Note­book ac­tion bar** (next to “Col­lapse All”)
- Smooth **slide down/up an­i­ma­tion** on open/close

### 📌 Note­book con­text menu
- **Cool-Sync now!**
- **Edit Cool-Sync**

### 📌 Note­book right-side icons
- ▶️ Ex­e­cute Cool-Sync
- ✏️ Edit Cool-Sync
- 🔄 Tog­gle au­to­mat­ic sync

## 🪟 The Cool-Sync Pan­el
Docked above the note ed­i­tor.

### **Main con­tent**
A re­spon­sive grid/flexbox list of Cool-Sync pro­files:

| Note­book | Type | Tar­get | In­ter­val | Last Sync | Sta­tus | Ac­tions |
| --- | --- | --- | --- | --- | --- | --- |

Ac­tions per pro­file:  
▶️ Run • ✏️ Edit • 🗑️ Delete

When no pro­files ex­ist:  
**“No Cool-Sync cre­at­ed yet!”** (cen­tered)

### **Glob­al ac­tions**
- ➕ Cre­ate Cool-Sync
- ❌ Delete all Cool-Sync pro­files
    
### **Be­hav­ior**
- Auto-re­fresh on pan­el open
- Re­fresh af­ter cre­ate/edit/delete
- Man­u­al open/close via tool­bar icon or Tools menu

## 🪟 "Edit Cool-Sync" Di­a­log
Al­lows full con­fig­u­ra­tion of a Cool-Sync pro­file.

### **Lay­out**
Re­spon­sive lay­out with:
- Head­er (icon + ti­tle on the left, note­book ti­tle cen­tered, close but­ton right)
- Scrol­lable set­tings sec­tion
- Bot­tom ac­tion bar: **Test**, **Save**, **Can­cel**

### **1\. Source**
- Note­book pick­er
- Dis­play of note­book UUID (info icon/la­bel)

### **2\. Tar­get**
- **Lo­cal Fold­er** (de­fault)
    - Fold­er path field + fold­er choos­er
- **GitHub** (op­tion­al)
    - Cre­den­tials + repos­i­to­ry fields
    - ZIP mode rec­om­mend­ed for GitHub up­loads

### **3\. Syn­chro­niza­tion Type**
- Spe­cif­ic Fold­er
- ZIP File
- Fold­er + ZIP File

### **4\. Syn­chro­niza­tion Struc­ture**
- **Fold­ers/Files** (de­fault)
- **Sta­t­ic Site** (se­lect one):
    - Hugo
    - Eleven­ty
    - Gats­by
    - Jekyll

### **5\. ZIP Set­tings**
(En­abled for ZIP or Fold­er + ZIP modes)
- Keep last **N** ZIP back­ups
- File­name pat­tern (e.g. `[Cool-Sync] - [YYYYMMDD-HHmmss].zip`)
- Com­pres­sion lev­el:  
    copy / fastest / fast / **nor­mal (de­fault)** / max­i­mum / ul­tra
- Pass­word pro­tec­tion:
    - Pass­word
    - Pass­word re­peat

### **6\. Oth­er Set­tings**
- Note for­mat: Mark­down / HTML (Sin­gle file) / Plain text
- Au­to­mat­ic sync in­ter­val (min­utes) — de­fault: **30 min**
- In­clude at­tach­ments
- Post-back­up script (file pick­er)
    - Ex­am­ple: GitHub push script

## 🛠️ De­vel­op­ment Struc­ture
- Mod­u­lar ar­chi­tec­ture un­der `src/`:
    - `panel/`, `dialogEdit/`, etc.
- Clean file sep­a­ra­tion: `.html`, `.css`, `.js`, `.ts`
- Per­sis­tent stor­age via **SQLite/JSON + se­cure se­crets**
- Vi­su­al de­sign aligned with Joplin and ex­ist­ing plu­g­ins
- Tem­po­rary Cool-Sync icon in­clud­ed (fi­nal icon not yet cre­at­ed)

## 💻 Com­pat­i­bil­i­ty
| Plat­form | Sup­port­ed |
| --- | --- |
| Win­dows | ✔️  |
| Lin­ux | ✔️  |
| ma­cOS | ✔️  |
| An­droid | ❌   |
| iOS | ❌   |

## 🌐 In­ter­na­tion­al­iza­tion
Cool-Sync au­to­mat­i­cal­ly adapts to the cur­rent Joplin lo­cale: **fr-FR / en-US / de-DE / es-ES / it-IT / pt-PT / uk-UA**
- Ful­ly trans­lat­ed UI
- Lo­cal­ized date/time/num­ber for­mats
- De­fault lo­cale if un­sup­port­ed: **en-US**

## 📥 In­stal­la­tion
1.  Down­load the `.jpl` file from the re­lease page.
2.  In Joplin: **Tools → Op­tions → Plu­g­ins**
3.  In­stall from file
4.  Restart Joplin.

## 🚀 Quick Start
1.  Right-click a note­book → **Cool-Sync now!**
2.  Or open the pan­el via **Tools → Cool-Sync**
3.  Cre­ate a pro­file:
    - Se­lect note­book
    - Choose tar­get fold­er / ZIP / both
    - Con­fig­ure struc­ture and op­tions
4.  Run man­u­al­ly or ac­ti­vate au­to­mat­ic sync.

## 📝 Li­cense
To be de­fined...