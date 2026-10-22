# Haridwar

Please build a production-ready, interactive, mobile-first responsive web application dashboard in a single HTML file (with embedded CSS and JavaScript) for a trip expense & room allotment tracker in Gujarati. Use Claude Artifacts to render the fully working preview.

### Technical & System Requirements:
1. Mobile-first design: Optimized for 360px–480px screens, sleek modern card/widget layout (inspired by Apple/Modern iOS dashboards with subtle borders, blur effects, clean padding, and soft drop-shadows).
2. Gujarati typography: Clean sans-serif rendering with Gujarati font fallbacks (-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Noto Sans Gujarati", sans-serif).
3. Cache-busting meta headers in <head>:
   <meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
   <meta http-equiv="Pragma" content="no-cache">
   <meta http-equiv="Expires" content="0">
4. Smart Refresh Action: An interactive "🔄 રિફ્રેશ" button in the header that resets cached values and force-reloads using a timestamp query parameter (`window.location.href = window.location.origin + window.location.pathname + '?t=' + new Date().getTime()`).
5. Accordions & Modals: Smooth toggle animations using JavaScript (no external libraries or heavy CDNs).

### Header & Executive KPI Cards:
- App Title: હરિદ્વાર-ઋષિકેશ પ્રવાસ
- Subtitle: પ્રવાસ ખર્ચ અને રૂમ વિગત ૨૬ થીમ
- Refresh CTA: "🔄 રિફ્રેશ" button in top-right of header.
- Top Grid Metrics (2 Cards):
  1. કુલ દાખલ ખર્ચ: ₹7,86,527
  2. કુલ બાકી ચુકવણી: ₹1,43,580 (highlighted in soft red/amber)

### Critical Pending Dues Section (Red/Danger Accent Container):
- Section Title: ⏳ ચૂકવવાની બાકી રકમ (કુલ: ₹1,43,580)
- 4 Compact Metric Cards (Grid):
  1. 🚆 ટ્રેન ટિકિટ બાકી: ₹81,780
  2. 🪂 મા ગંગા બંજી: ₹37,800
  3. 🚙 ૫ જીપ + ગાઇડ: ₹20,000
  4. 🥁 ઢોલ બુકિંગ: ₹4,000

### Itemized Expense & Allotment List:

1. 🏨 **રૂમ + હોલ (૮ રાત)**:
   - Primary Amount: ₹2,92,800 (દૈનિક ₹36,600 × 8 રાત | 15 રૂમ / 38 બેડ)
   - Status: આયોજિત
   - Modal Trigger: A distinct "📄 રૂમ લિસ્ટ PDF / પત્રક" button opening a clean printable popup modal with full floor-wise allotment and a "🖨️ આ પત્રક પ્રિન્ટ / PDF સેવ કરો" button calling `window.print()`.
   - Collapsible Detail: Clicking card expands floor-wise allotment displaying ONLY person names and room types (NO individual prices):
     * G/F (ગ્રાઉન્ડ ફ્લોર):
       - રૂમ ૧ (2-Bed): Ramabhai
       - રૂમ ૨ (2-Bed): Ashokbhai
       - ફેમિલી હોલ (4-Bed Non-AC): General / Open
     * 1/F (પહેલો માળ):
       - રૂમ ૧ (2-Bed Non-AC): Amitbhai
       - રૂમ ૨ (2-Bed Non-AC): Bharatkaka
       - રૂમ ૩ (2-Bed Non-AC): Rameshkaka
       - રૂમ ૪ (2-Bed AC): Arvindbhai
       - ફેમિલી રૂમ (6-Bed AC ગંગા ફેસિંગ): Kids (બાળકો)
     * 2/F (બીજો માળ):
       - રૂમ ૧ (2-Bed AC): Niketbhai
       - રૂમ ૨ (2-Bed AC): Dipaben
       - રૂમ ૩ (2-Bed AC): Jigneshbhai
       - રૂમ ૪ (2-Bed AC): Rohit
       - ફેમિલી રૂમ (4-Bed AC ગંગા ફેસિંગ): Ritesh
     * 3/F (ત્રીજો માળ):
       - રૂમ ૧ (2-Bed AC): Dinesh
       - રૂમ ૨ (2-Bed AC): Ajay
     * Hotel Rules Box: લિફ્ટ નથી (No Lift), હોટેલ સવલતો (સાબુ, ટુવાલ, હેન્ડવોશ, રૂમ સર્વિસ) ઉપલબ્ધ નથી, બેડશીટ દર ૩ દિવસે બદલાશે.

2. 🥁 **ઢોલ બુકિંગ**:
   - Primary Amount: ₹4,500 (એડવાન્સ ₹500 ચૂકવેલ)
   - One-tap Action: Green pill button with `tel:9997057352` displaying "📞 કૉલ કરો: 9997057352"
   - Pending Due: ⚠️ ₹4,000 બાકી

3. 🚆 **ટ્રેન ટિકિટ્સ (કુલ ખર્ચ)**:
   - Primary Amount: ₹2,81,780 (જવા + આવવાની બધી ટિકિટ અને ચાર્જ)
   - Badge/Status: ✓ એડવાન્સ: ₹2,00,000 | ⚠️ બાકી: ₹81,780
   - Interactive Expand: Clicking shows train breakdown:
     * જવા માટે (07/11/2026 - ટ્રેન ૧૯૦૧૯) & આવવા માટે (16/11/2026 - ટ્રેન ૨૨૬૬૦)
     * કુલ ટિકિટ ભાડું (Fare Total): ₹1,47,780
     * કુલ સર્વિસ ચાર્જ (S.CL Total): ₹1,34,000
     * ટ્રેન કુલ રકમ: ₹2,81,780
     * ચૂકવેલ એડવાન્સ: -₹2,00,000
     * ચૂકવવાની બાકી રકમ: ₹81,780

4. ✈️ **ફ્લાઇટ / પર્સનલ ટિકિટ**:
   - Primary Amount: ₹1,28,472 (₹54,792 + ₹73,680)
   - Status Pill: ચકાસવાનું બાકી

5. 🪂 **મા ગંગા બંજી જમ્પિંગ**:
   - Primary Amount: ₹42,000 (6 વ્યક્તિ • 9 નવેમ્બર, બપોરે 12)
   - Advance: ₹4,200 ચૂકવેલ | Due: ₹37,800 બાકી

6. 🚙 **જિમ કોર્બેટ જીપ + ગાઇડ (૫ જીપ)**:
   - Primary Amount: ₹20,000 (૫ જીપ × ₹4,000 | જીપ ₹3,000 + ગાઇડ ₹1,000)
   - Due Status: ⚠️ ₹20,000 સંપૂર્ણ બાકી (સ્થળ પર ચુકવણી)

7. 🐅 **જિમ કોર્બેટ સફારી ટિકિટ**:
   - Primary Amount: ₹16,975 (5 વ્યક્તિ × ₹3,395)
   - Status Pill: ✓ સંપૂર્ણ ચૂકવેલ

### Deliverable:
Provide the full, un-truncated, self-contained HTML code in a single artifact code block named `index.html`. Ensure JavaScript toggle and modal logic is fully functional.
