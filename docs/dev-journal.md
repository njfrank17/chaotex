# Development Journal  

*This journal will document both HOW I built this project and  
WHY I made the decisions I did*  

## Initial Project Setup  

**Structure:**  

- Used `Structure_initial-repo-skeleton` as a guide.  
- Verified structure with ChatGPT5.1 in Mentor mode before commit.  

**GitHub:**  

- Initial commit using best practice advice for message.  
- Added MIT License from GitHub template.  
- Wrote README.md with a balance of technical and inspirational tones to show why this project is important to me.  

**Notebooks:**  

- Added a notebooks folder to experiment
  - keep testing out of source code  
  - validate shape and flow with simulation before heavy UI and video handling  
  - use iPad when traveling to Panama for vacation.  
- Keep chaos separate and organize, but chaos is still part of the foundation of ChaotEX  

---

## ChaotEX Foundation

**Version 1 Goals:**  

- Upload and save a video  
- Load video to UI to segment and comment
- Generate simple text report with comments and ideas  

Notes:  

- experiment in notebook with simulated db
- manually enter timestamps to segment video
- manually add comments/ideas  
- report will just be basic data: source, segment, comments, ideas, metadata

**Data Models:**  

- raw_data (source)  
- segment (clip)  
- comment (training)  
- idea (content)  
- report (grouped-data)

**Knowledge Graph:**  
report -> created-with -> comments | ideas  
comments | ideas -> entered-by-user-per -> segment  
segments -> derived-from -> raw_data  

*suggested by ChatGPT5.1:*  
`RAW_DATA --has_segment--> SEGMENT`  
`SEGMENT -- has_note--> COMMENT/IDEA`  
`REPORT --includes--> COMMENT/IDEA`  
`NOTE -- attached_to--> SEGMENT`  
`REPORT --includes--> NOTES`  

**Future and Ideas:**  

- `REPORTS` will display `SEGMENT` metadata followed by `NOTES`  
- Consider using only `NOTES` for now, and expand into more later:  
  - needs_work  
  - did_good  
  - video_idea  
  - etc.
- ***BEFORE NOTEBOOK***, create a small written example of what all data looks like, this will create the data models.
