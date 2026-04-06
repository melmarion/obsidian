```dataview  
table  
    Metatype,  
    Agency,  
    Temp,  
    file.mtime as "Last Updated"  
from #people  
sort file.name  
```  

# {{title}}  
**Metatype:** 🎭 [Charmer/Narcissist/Martyr/Pawn]  
**Context:** [How you know them]  

## 🔍 Core Traits  
- **Agency**:: [High/Med/Low]  
- **Temp**:: [Hot/Cold]  
- **Tells**:: ["Actually,", nervous laugh, etc.]  
- **Craves**:: [Validation/Control/Chaos]  
- **Fears**:: [Exposure/Irrelevance/Boredom]  

## ⚠️ Confirmed Weaknesses  
1. [ ] Hates being ignored  
2. [ ] Overreacts to [trigger]  

## 📜 Strategic Log  
```dataview  
table date, Test, Result  
from "People_DB"  
where contains(file.name, this.file.name)  
sort date desc  
```  

## 🔗 Linked Profiles  
- Allies:: [[Person X]]  
- Rivals:: [[Person Y]]  