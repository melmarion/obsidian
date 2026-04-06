````markdown
```dataview  
table  
    Metatype,  
    Agency,  
    Temp,  
    file.mtime as "Last Updated"  
from #people  
sort file.name  
```  

# [Name]  
[CONTEXT: How you know them (work, friend, enemy)]  
### **Metatype:** 🎭 [Charmer/Narcissist/Martyr/Pawn]  
**Context:** [How you know them]

People_DB/  
├── 🟢 _Allies/  
├── 🟠 _Neutrals/  
├── 🔴 _Adversaries/  
└── 🧠 _Templates/  

- Record covert voice memos during conversations (e.g., with Otter.ai).
    
- Drag the file into their profile note.
    
- **Why?** Tone analysis reveals hidden tells.
## 🔍 Core Traits  
- **Agency**:: [High/Med/Low]  
- **Temp**:: [Hot/Cold]  
- **Tells**:: ["Actually,", nervous laugh, etc.]  
- **Craves**:: [Validation/Control/Chaos]  
- **Fears**:: [Exposure/Irrelevance/Boredom]  

CORE TRAITS:  
- Agency: [High/Medium/Low]  
- Emotional Temp: [Hot/Cold]  
- Locus of Control: [Internal/External]  
- Tells: [Their verbal/physical tics]  
## ⚠️ Confirmed Weaknesses  
1. [ ] Hates being ignored  
2. [ ] Crumbles under public accountability  
3. [ ] Overreacts to [trigger]  

WEAKNESSES:  
1. [What makes them squirm?]  
2. [What do they overcompensate for?]  

POWER LEVERS:  
1. [What do they crave?]  
2. [What would they hate to lose?]  

RECENT TEST:  
- [What did you try on them?]  
- [How did they react?]  

NEXT MOVE:  
- [What’s your strategic play?]  
## **Strategic Log**  
- 2024-05-20: Tested w/ [method]. Result: [reaction].  
- NEXT: [planned move]  

## 📜 Strategic Log  
table date, Test, Result  
from "People_DB"  
where contains(file.name, this.file.name)  
sort date desc   
## **Linked Profiles**  
- [[Person X]] (their ally)  
- [[Person Y]] (their rival)  
## 🔗 Linked Profiles  
- Allies:: [[Person X]]  
- Rivals:: [[Person Y]]  