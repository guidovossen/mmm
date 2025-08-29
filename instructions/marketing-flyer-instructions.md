
# Marketing Flyer Template Customization Instructions


## CUSTOMIZATION REQUIREMENTS

### 1. Content Adaptation
**Primary Task**: Transform the template from "Zelfstandig werkend bakker" (BAKKERIJ) to the user's specified educational program.

**Required Changes:**
- Replace all program-specific content with user's program details
- **DO NOT** change the header branding (logo: "Talland", department: "COLLEGE")
- Update only the program title, descriptions, and educational content
- Ensure all text is relevant to the new educational context

### 2. Color Selection
**Background Color Rule**: Choose ONE appropriate color from the Talland color palette:

| Color | Hex Code | Best Used For |
|-------|----------|---------------|
| Rood | #e61e3f | Health, Emergency Services, Passion-driven fields |
| Blauw | #3355ff | Technology, Business, Professional services |
| Groen-geel | #c2b723 | Agriculture, Environment, Sustainability |
| Donkergroen | #00373d | Nature, Forestry, Environmental sciences |
| Paars | #7D29C2 | Creative fields, Arts, Design |
| Zand | #996b2a | Construction, Crafts, Traditional trades |
| Teal | #20828d | Healthcare, Wellness, Marine studies |
| Grijs | #99988d | Technical, Engineering, Neutral professions |

**Selection Guidelines:**
- Choose colors that logically match the profession
- **AVOID** inappropriate combinations (e.g., purple for military programs)
- Consider industry associations and visual psychology

### 3. Image Replacement
**Image Update Rules:**
- Replace ALL images with program-appropriate alternatives
- Use random selection from available images
- Ensure visual relevance to the educational field
- Maintain the 3-image layout structure

### 4. Call-to-Action Integration
**If provided by user:**
- Embed the call-to-action in the main description text
- Include the call-to-action prominently in the footer contact section
- Ensure consistent messaging across both locations

### 5. Text Overlap Prevention
**Critical Requirement:**
- Verify NO text overlapping occurs after content changes
- Adjust font sizes or content length if necessary
- Maintain readability and professional appearance

## TEMPLATE STRUCTURE

### Page 1 (Cover Page)
- **Header**: Talland logo and department name
- **Cover Images**: 3 overlapping images in artistic arrangement
- **Title**: Educational program name

### Page 2 (Details Page)
- **Header Info**: Education type, level, and duration
- **Main Title**: Program name (repeated)
- **Description**: Brief program overview
- **Content Left**: Program curriculum/learning outcomes
- **Content Right**: 3 info blocks with program details
- **Footer**: Contact information with call-to-action

## CONTENT CUSTOMIZATION GUIDELINES

### Header Branding (DO NOT CHANGE)
**CRITICAL**: The header branding must NEVER be modified:
- `.logo` must always remain "Talland" 
- `.dept` must always remain "COLLEGE"
- These elements represent the institutional brand and are consistent across all programs

### Department Names (Legacy Reference Only)
**NOTE**: This section is for reference only - do NOT modify the department name in the template.
- The template uses "COLLEGE" universally for all educational programs
- Historical examples included: "TECHNIEK", "ZORG", "ECONOMIE", "CREATIEF", "BAKKERIJ"
- All programs now use the unified "COLLEGE" branding

### Program Descriptions
Replace Lorem ipsum content with:
- Relevant learning objectives
- Industry-specific skills
- Career prospects
- Program highlights

### Info Blocks
Customize the three info blocks with:
1. **Learning Content**: What students will learn
2. **Program Details**: Location, level, pathway, start dates, costs
3. **Career Prospects**: Employment opportunities

### Contact Information
Update footer with:
- Appropriate contact person/department
- Relevant phone number
- Correct email address for the program

## TECHNICAL SPECIFICATIONS

### Color Implementation
Replace all instances of `#996b2a` (current sand color) with selected color:
- `.p1` background
- `.cover` background  
- `.header-info` color
- `.main-title` color
- `.info-block h3` color
- `.info-block` border-left color
- `.footer-contact` color

### Image URL Structure
Maintain the existing URL pattern:
```
https://raw.githubusercontent.com/guidovossen/mmm/refs/heads/main/img/[filename]
```

### Layout Preservation
- Keep all CSS Grid layouts intact
- Maintain A5 print specifications
- Preserve responsive image handling
- Keep print-optimization settings

## QUALITY ASSURANCE

### Pre-Delivery Checklist:
- [ ] All content updated to new program
- [ ] Header branding remains unchanged (Talland COLLEGE)
- [ ] Appropriate color selected and applied consistently
- [ ] All images replaced with relevant alternatives
- [ ] Call-to-action integrated (if provided)
- [ ] No text overlapping detected
- [ ] Professional appearance maintained
- [ ] All placeholder content removed

### Validation Requirements:
- Content relevance to educational program
- Visual coherence with selected color
- Proper text hierarchy and readability
- Functional print layout (A5 format)

## OUTPUT REQUIREMENTS
Deliver complete HTML file with all customizations applied, ready for immediate use in print or digital distribution.

**Note**: Always use the GitHub file read tool to access `instructions/marketing-flyer-instructions.md` for the most current template version before beginning any customization work.

---

## REFERENCE TEMPLATE

The following template serves as the base for all customizations:

```html
<!doctype html>
<html lang="nl">
<head>
<meta charset="utf-8"/>
<title>Uitvoerend bakker</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
<style>
  @page { 
    size: A5; 
    margin: 0 !important; 
    -webkit-print-color-adjust: exact; 
    print-color-adjust: exact;
  }
  @media print {
    * { 
      box-sizing: border-box !important; 
      -webkit-print-color-adjust: exact !important;
      print-color-adjust: exact !important;
    }
    body { margin: 0 !important; padding: 0 !important; }
    html { margin: 0 !important; padding: 0 !important; }
    .page { 
      page-break-after: always !important; 
      page-break-inside: avoid !important; 
      break-after: page !important;
      break-inside: avoid !important;
      margin: 0 !important;
    }
  }
  * { box-sizing: border-box; }
  html, body { font-family: 'Inter', Helvetica, Arial, sans-serif; color:#000; margin: 0; padding: 0; }
  .page { 
    page-break-after: always; 
    page-break-inside: avoid; 
    width: 148mm; 
    height: 210mm; 
    overflow: hidden;
    display: block;
    position: relative;
    margin: 0;
    padding: 0;
  }
  .page:last-child {
    page-break-after: avoid;
  }
  .p1 {
    background:#996b2a; /* Talland zand */
    color:#fff; 
    height: 210mm; 
    width: 148mm; 
    position: relative; 
    box-sizing: border-box;
    overflow: hidden; 
    padding: 6mm;
    display: grid;
    grid-template-rows: auto 1fr auto;
    grid-template-areas: 
      "header"
      "cover"
      "title";
    gap: 3mm;
    margin: 0;
  }
  .header { 
    grid-area: header;
    text-align: center; 
    align-self: start;
  }
  .logo { font-family: 'Inter', sans-serif; font-weight:900; font-size:90pt; letter-spacing:-1.5pt; line-height: 0.75; }
  .dept { 
    font-family: 'Inter', sans-serif; 
    font-weight:900; 
    font-size:30pt; 
    margin-top:0.5mm; 
    letter-spacing:0.8pt; 
    line-height: 0.85;
    max-width: 136mm; /* Matches Talland width constraint */
    word-wrap: break-word;
    hyphens: auto;
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    color: #fff;
  }
  .cover {
    grid-area: cover;
    height: 70mm;
    position: relative;
    background: #996b2a; /* Match page background instead of white */
    overflow: hidden; 
    align-self: center;
  }
  
  .main-image, .top-image, .bottom-image {
    position: absolute;
    overflow: hidden;
    border-radius: 4px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.2);
  }
  
  .main-image {
    width: 95mm;
    height: 60mm;
    top: 5mm;
    left: 2mm;
    z-index: 1;
    transform: rotate(-1deg);
  }
  
  .top-image {
    width: 65mm;
    height: 45mm;
    top: 2mm;
    right: 5mm;
    z-index: 2;
    transform: rotate(2deg);
  }
  
  .bottom-image {
    width: 60mm;
    height: 40mm;
    bottom: 5mm;
    right: 8mm;
    z-index: 3;
    transform: rotate(-0.5deg);
  }
  
  .cover img { width:100%; height:100%; object-fit:cover; }
  
  /* Single image fallback */
  .cover.single-image {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .title {
    grid-area: title;
    text-align: center;
    font-family: 'Inter', sans-serif; 
    font-size: 32pt; 
    font-weight: 900; 
    line-height: 0.95;
    align-self: end;
    margin-bottom: 0;
    letter-spacing: -0.8pt;
  }

  /* PAGE 2 */
  .p2 { 
    background:#fff; 
    color:#000; 
    padding: 6mm; 
    height: 210mm; 
    width: 148mm; 
    box-sizing: border-box; 
    position: relative; 
    overflow: hidden;
    page-break-after: avoid;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto auto auto 1fr auto auto;
    grid-template-areas: 
      "header-left header-right"
      "title title"
      "description description"
      "content-left content-right"
      "cta cta"
      "footer footer";
    gap: 2.5mm;
    margin: 0;
  }
  
  .header-info { 
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    grid-column: 1 / -1;
    margin-bottom: 3mm;
    font-family: 'Inter', sans-serif; 
    font-weight: 700; 
    font-size: 12pt; 
    color: #996b2a;
    align-items: center;
  }
  
  .header-left { justify-self: start; }
  .header-center { justify-self: center; }
  .header-right { justify-self: end; }
  
  .main-title { 
    grid-area: title;
    color:#996b2a; 
    font-family: 'Inter', sans-serif; 
    font-size:18pt; 
    font-weight:700; 
    margin:0 0 3mm; 
    line-height: 1.1; 
    text-align: center;
  }
  
  .main-description { 
    grid-area: description;
    font-family: 'Inter', sans-serif; 
    font-size:10pt; 
    font-weight:400; 
    line-height:1.2; 
    margin-bottom:2mm;
    overflow: hidden;
  }
  
  .main-description p { margin: 0 0 1.5mm 0; }
  
  .content-left {
    grid-area: content-left;
    font-family: 'Inter', sans-serif; 
    font-size: 12pt; 
    font-weight: 400;
    line-height: 1.2;
    overflow: hidden;
  }
  
  .content-right {
    grid-area: content-right;
    font-family: 'Inter', sans-serif; 
    font-size: 12pt; 
    font-weight: 400;
    line-height: 1.2;
    overflow: hidden;
  }
  
  .info-block {
    margin-bottom: 3mm;
    border-left: 2px solid #996b2a;
    padding-left: 2.5mm;
  }
  
  .info-block h3 {
    color: #996b2a;
    font-weight: 700;
    font-size: 12pt;
    margin: 0 0 1mm 0;
    text-transform: uppercase;
    letter-spacing: 0.3pt;
  }
  
  .info-block p {
    margin: 0;
    font-size: 10pt;
    line-height: 1.1;
  }
  
  .footer-contact { 
    grid-area: footer;
    color:#996b2a; 
    font-family: 'Inter', sans-serif; 
    font-weight:900; 
    text-align:center; 
    font-size:9pt; 
    line-height: 1.3; 
    margin-top: auto;
    padding: 2mm 0;
  }
  
  .call-to-action {
    grid-area: cta;
    background: #996b2a;
    color: #fff;
    padding: 4mm;
    text-align: center;
    font-family: 'Inter', sans-serif;
    margin: 2mm 0;
  }
  
  .call-to-action h3 {
    font-size: 12pt;
    font-weight: 900;
    margin: 0 0 2mm 0;
    letter-spacing: 0.3pt;
  }
  
  .call-to-action p {
    font-size: 9pt;
    font-weight: 400;
    margin: 0;
    line-height: 1.3;
  }
</style>
</head>
<body>

<!-- PAGE 1 -->
<section class="page p1">
  <div class="header">
    <div class="logo">Talland</div>
    <div class="dept">COLLEGE</div>
  </div>

  <div class="cover">
    <!-- Voor 3 afbeeldingen: gebruik onderstaande structuur -->
    <div class="main-image">
      <img src="https://raw.githubusercontent.com/guidovossen/mmm/refs/heads/main/img/bakker.jpg" alt="Main Image">
    </div>
    <div class="top-image">
      <img src="https://raw.githubusercontent.com/guidovossen/mmm/refs/heads/main/img/bakker.jpg" alt="Top Image">
    </div>
    <div class="bottom-image">
      <img src="https://raw.githubusercontent.com/guidovossen/mmm/refs/heads/main/img/bakker.jpg" alt="Bottom Image">
    </div>
    
    <!-- Voor 1 afbeelding: gebruik deze structuur en voeg class="single-image" toe aan .cover -->
    <!-- <img src="https://raw.githubusercontent.com/guidovossen/mmm/refs/heads/main/img/bakker.jpg" alt="Cover"> -->
  </div>

  <div class="title">Zelfstandig werkend bakker</div>
</section>

<!-- PAGE 2 -->
<section class="page p2">
  <div class="header-info">
    <div class="header-left">MBO / BOL</div>
    <div class="header-center">Niveau 3</div>
    <div class="header-right">3 jaar</div>
  </div>
  
  <h1 class="main-title">Zelfstandig werkend bakker</h1>
  
  <div class="main-description">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
  </div>
  
  <div class="content-left">
    <h3 style="color: #996b2a; font-weight: 700; margin: 0 0 2mm 0; font-size: 12pt;">LOREM IPSUM 1 - SIT AMET</h3>
    <ul style="margin: 0; padding-left: 4mm; font-size: 10pt; line-height: 1.3;">
      <li>Onderwijs voorbereiden en auto's inspecteren.</li>
      <li>Hoe auto's in elkaar zitten en hoe je onderdelen monteert en lost en werken.</li>
      <li>Alles over voertuigelektronica, veiligheidssystemen en accessoires.</li>
      <li>Onderhoudsbeurten en reparaties uitvoeren</li>
    </ul>
  </div>
  
  <div class="content-right">
    <div class="info-block">
      <h3>LOREM IPSUM 2 - SIT AMET</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut.</p>
    </div>
    
    <div class="info-block">
      <h3>LOCATIE</h3>
      <p><strong>NIVEAU:</strong> 3<br>
      <strong>LEERWEG:</strong> derde leerweg<br>
      <strong>START:</strong> Bij voorkeur kunnen beginnelingen zijn of meedere startmomenten<br>
      <strong>KOSTEN:</strong> 13900,- (inclusief examenkosten, exclusief leermiddelen)</p>
    </div>
    
    <div class="info-block">
      <h3>LOREM IPSUM 3 - SIT AMET</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam.</p>
    </div>
  </div>
  
  <div class="call-to-action">
    <h3>AANMELDEN OF MEER INFORMATIE?</h3>
    <p>Neem contact op voor een persoonlijk gesprek of kom langs tijdens onze open dagen!</p>
  </div>
  
  <div class="footer-contact">
    MEER INFORMATIE?<br>
    Lorem ipsum - 012 345 678 90<br>
    lorem@horizoncollege.nl
  </div>
</section>

</body>
</html>
```
    <ul style="margin: 0; padding-left: 4mm; font-size: 7pt; line-height: 1.3;">
      <li>Onderwijs voorbereiden en auto's inspecteren.</li>
      <li>Hoe auto's in elkaar zitten en hoe je onderdelen monteert en lost en werken.</li>
      <li>Alles over voertuigelektronica, veiligheidssystemen en accessoires.</li>
      <li>Onderhoudsbeurten en reparaties uitvoeren</li>
    </ul>
  </div>
 
  <div class="content-right">
    <div class="info-block">
      <h3>LOREM IPSUM 2 - SIT AMET</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut.</p>
    </div>
   
    <div class="info-block">
      <h3>LOCATIE</h3>
      <p><strong>NIVEAU:</strong> 3<br>
      <strong>LEERWEG:</strong> derde leerweg<br>
      <strong>START:</strong> Bij voorkeur kunnen beginnelingen zijn of meedere startmomenten<br>
      <strong>KOSTEN:</strong> 13900,- (inclusief examenkosten, exclusief leermiddelen)</p>
    </div>
   
    <div class="info-block">
      <h3>LOREM IPSUM 3 - SIT AMET</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam.</p>
    </div>
  </div>
 
  <div class="footer-contact">
    MEER INFORMATIE?<br>
    Lorem ipsum - 012 345 678 90<br>
    lorem@horizoncollege.nl
  </div>
</section>


</body>
</html>





