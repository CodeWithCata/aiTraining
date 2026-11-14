# HANDOFF — AI Business Challenge UPB (pentru următorul AI)

> Citește acest document integral înainte să răspunzi. Starea este cea de **sâmbătă, 14 noiembrie 2026, ~14:40 (Europe/Bucharest)**. Concursul e pe **20 noiembrie 2026**, deci mai sunt 6 zile.
> Limba de lucru: **română**. Utilizatorul scrie scurt și direct; răspunde la fel: concret, fără introduceri lungi.

---

## 1. Cine e utilizatorul și ce vrea

- Echipă de **3 persoane** la **AI-Powered Business Challenge** (Start Your StartUP 2026, UPB).
- **Utilizatorul = Persoana 1, Technical Lead.** Știe să programeze. Tratează-l ca pe un inginer experimentat: detalii tehnice, compromisuri, fără simplificări. Nu vrea curs despre „ce e AI-ul".
- **Colegii (P2 Product & UX/UI, P3 Business/Research/QA)** au puțină sau deloc experiență de programare. Pentru ei: limbaj simplu, un exemplu concret, o sarcină mică odată, fără jargon neexplicat.
- Obiectivul acum: **pregătirea echipei într-o săptămână**, apoi construirea livrabilelor în 3 ore în ziua concursului.
- Utilizatorul folosește aplicația mobilă Claude, deci răspunsurile scurte și ușor de citit pe telefon sunt preferate.

## 2. Faptele concursului (din regulamentul oficial și pagina UPB)

Surse citite direct:
- Pagina: https://events.upb.ro/ai-business-challenge
- Regulament (PDF): https://events.upb.ro/ai-business-challenge/Regulament_AI_Powered_Business_Challenge_2026.pdf
- Contact organizatori: razvan.dobrescu@upb.ro, nicoleta.orb@upb.ro

**Format**
- Probă fizică la POLITEHNICA București, **3 ore**. Tema, datele, cerințele și ora-limită se comunică la start, simultan tuturor.
- Echipe de 1–3. Nu e necesară experiență de programare.
- AI permis pentru tot (analiză, cod, texte, imagini, prezentări, no-code/low-code). Aplicația nu trebuie să conțină obligatoriu o funcție AI. Numărul de unelte sau un abonament plătit nu aduc puncte.
- Mentori disponibili în cele 3 ore (business, finanțe, tehnologie, comunicare). Ei dau feedback, **nu fac livrabilele**.
- Preselecția: comisie + AI pe aceeași grilă, cu verificare umană. Primele **10 echipe cu minimum 60 de puncte** merg în finală.
- Finala: **3 min pitch + demo, 2 min întrebări**, 5 jurați din business.

**Cele 6 livrabile (toate cerute)**
1. Aplicație web publicată (link, cel puțin o funcție principală testabilă, parcurs simplu; date de test)
2. Strategie pe o pagină (problemă, public, soluție, atragere clienți, 3 pași de implementare)
3. Model financiar (tabel editabil cu formule, ipoteze, costuri, venituri, rezultat; un singur scenariu de bază)
4. Material de promovare (postare sau afiș: mesaj, vizual, îndemn la acțiune)
5. Jurnal AI (max 1 pagină: unelte, 3 prompturi, 1 exemplu de rezultat AI verificat și corectat; declarare resurse/șabloane externe)
6. Pitch și demo (max 5 slide-uri + link + instrucțiuni de testare)

Video, scenarii suplimentare și oferta pentru parteneri sunt opționale și **nu aduc puncte**.

**Grila de preselecție (regulament):** Aplicație și UX 35, Strategie și model financiar 25, Utilizarea critică a AI 15, Material de promovare 15, Pitch predat 10.
**Grila finalei:** Aplicație și demonstrație 30, Strategie și model financiar 30, Utilizarea și înțelegerea AI 20, Prezentare și răspunsuri 20.

**Reguli de integritate:** fără funcții sau rezultate inexistente prezentate ca reale, fără plagiat, livrabilele le fac doar membrii înscriși, resursele externe se declară în jurnalul AI, date fictive pentru testare, nu se introduc date personale reale sau confidențiale în AI. Se evaluează doar versiunea predată la termen.

## 3. Neconcordanțe și lucruri NEVERIFICATE (nu le trata ca sigure)

- **Ora de start:** pagina spune 10:00, regulamentul spune 11:00. De confirmat cu organizatorii.
- **Grile diferite:** pagina web are o grilă cu „Plan de implementare 15" și „Demonstrarea funcției principale 5"; regulamentul are alta. Subsolul paginii spune că formatul/grila sunt „propuneri". **Regulamentul are prioritate.**
- **Înscrierea s-a închis pe 10 noiembrie.** Utilizatorul nu a confirmat explicit că echipa e înscrisă și că a depus PDF-ul de o pagină despre experiența cu AI. Merită întrebat.
- **Premiile** (locurile I–III) nu sunt specificate public; regulamentul spune că se anunță înaintea înscrierilor.
- Formatele de predare, limitele de dimensiune și spațiul de predare se comunică **înaintea probei**; nu sunt cunoscute acum.
- Pagina menționează un „atelier de pregătire", fără dată.

## 4. Ce s-a făcut în conversația asta

1. Am citit contextul echipei (`CLAUDE_TEAM_CONTEXT_AI_BUSINESS_CHALLENGE.md`), am confirmat rolurile și am dat un prim plan + 3 exerciții.
2. La cererea utilizatorului am citit pagina și regulamentul. **Concluzia care a schimbat planul:** nu se predă doar o aplicație, ci 6 livrabile; strategia și finanțele valorează cât aplicația.
3. Am creat **`Roadmap_AI_Business_Challenge_UPB.pdf`** (6 pagini, în română) pentru colegi: concursul pe scurt, livrabile, punctaj, 5 reguli, roadmap pe 6 zile (14–19 nov), șablon de prompt, glosar, checklist UX, planul de 180 min, checklist-uri, resurse, videoclipuri, aplicații. Livrat utilizatorului.
4. Am creat **`index.html`** (un singur fișier autonom, minimalist, cu meniu): același conținut, plus numărătoare inversă, cronometru de simulare 180 min, roadmap cu bifare zile, constructor de prompturi cu copiere, glosar cu căutare, checklist-uri salvate în browser (localStorage), filtru de videoclipuri pe zile, temă luminoasă/întunecată. Livrat utilizatorului.
5. Utilizatorul a cerut acum acest document de predare.

## 5. Planul de pregătire în vigoare (6 zile)

| Zi | Dată | Focus | Cine conduce |
|---|---|---|---|
| 1 | Sâm 14 nov | Prompt engineering aplicat (ROL/CONTEXT/SARCINĂ/CONSTRÂNGERI/FORMAT/CRITERII) | toți |
| 2 | Dum 15 nov | Strategie pe o pagină + model financiar cu formule | P3 (P2 ajută, P1 verifică formulele) |
| 3 | Lun 16 nov | Front-end practic: HTML/CSS/JS, state, events, debugging, publicare | P1 |
| 4 | Mar 17 nov | Produs, UX/UI, afiș, pitch de 5 slide-uri | P2 |
| 5 | Mie 18 nov | **Simulare completă de 3 ore** cu toate 6 livrabilele | toți |
| 6 | Joi 19 nov | Pitch de 3 min cronometrat, ajustări, logistică; nimic nou | toți |

**Planul de 180 min (ziua concursului), adaptat la cele 6 livrabile:**
0–30 tema, problema, MVP, ce tăiem · 30–110 construire în paralel (P1 aplicația, P3 strategie + model, P2 afiș + slide-uri) · 110–150 testare + jurnal AI + integrare · 150–170 pitch + instrucțiuni de testare · 170–180 predare, verificare link, backup.

## 6. Starea fișierelor și ce NU este verificat

- `Roadmap_AI_Business_Challenge_UPB.pdf`: randat și inspectat vizual pagină cu pagină (diacritice, tabele, casete corecte). Livrat.
- `index.html`: **sintaxa JavaScript a fost verificată (`node --check`), dar pagina NU a fost rulată într-un browser.** O verificare cu Chrome headless (interacțiuni, erori de consolă, capturi mobil/desktop) a fost începută și **întreruptă de utilizator**; scriptul `check_page.py` (în directorul scratchpad al sesiunii) nu a rulat. Dacă utilizatorul raportează probleme, repară cu modificări mici, nu rescrie.
- **Videoclipuri YouTube:**
  - verificat direct: „world's shortest UI/UX design course" (canal Juxtopposed), `watch?v=wIuVvCuiJhU`
  - link direct neconfirmat (ID din pagini-agregator; YouTube a limitat cererile): „Prompt Engineering Guide – From Beginner to Advanced" (`uDIW34h8cmM`), „How to Vibe Code – Making a real web app step by step" (`7kQi2HQMz4s`, ~47 min, Sara Dietschy)
  - restul sunt **căutări YouTube** (funcționează sigur, rezultatele variază). Nu inventa ID-uri de video.
- **Aplicațiile recomandate** (Claude, ChatGPT, Gemini, Lovable, Replit, Bolt, Netlify Drop, Vercel, GitHub Pages, Canva, Figma, Google Workspace) sunt din cunoștințe generale, nu verificate acum: planurile gratuite și limitele trebuie verificate de echipă.
- Linkurile non-UPB din „Resurse" (MDN, web.dev, NN/g, Lean Canvas, ghidul de prompt engineering) sunt site-uri de referință cunoscute, neverificate în sesiune.
- Mediul de lucru avea rețeaua dezactivată pentru instalări de pachete; ce s-a generat a folosit doar ce era deja instalat.

## 7. Ce NU s-a decis încă

- **Tema concursului** (necunoscută până la start) și deci stack-ul final. Nu presupune o temă.
- Ce unealtă de construit aplicația și ce hosting vor folosi (P1 trebuie să aleagă una și să o exerseze în simulare).
- Numele colegilor și atribuirea finală a rolurilor (acum „Persoana 1/2/3", orientative).
- Tema inventată și datele de test pentru simularea din ziua 5.

## 8. Următorii pași propuși (întreabă utilizatorul pe care îl vrea)

1. **Șabloane pentru livrabile:** strategie pe o pagină, structură de model financiar cu formule, jurnal AI, checklist de predare.
2. **Tema inventată + date de test** pentru simularea de 3 ore (ziua 5), cu criterii ca la concurs.
3. **Exerciții detaliate** pe zile (prompturi și fișiere gata de folosit), începând cu ziua 1.
4. Testarea și eventuala reparare a `index.html` după feedback.
5. Pregătirea pitch-ului de 3 minute + răspunsuri la întrebările probabile ale juriului.

## 9. Cum să lucrezi cu această echipă (din brief-ul lor)

- Fii direct, practic, critic, orientat spre rezultat. Dacă ceva e prea mare pentru 3 ore, spune și propune o versiune mai mică.
- **Nu inventa** API-uri, rezultate de test, statistici, utilizatori, funcționalități sau reguli. Separă clar: ce se știe, ce se presupune, ce trebuie verificat. Dacă o decizie depinde de regulament, verifică sursa oficială.
- Gândește în **MVP**: un flux principal funcțional cap-coadă, interfață clară, date demo credibile și marcate ca demo. Taie implicit: autentificare complexă, plăți, chat în timp real, panouri admin, integrări fragile.
- Lucrează **incremental**; la modificări spune ce fișiere sunt afectate, limitează schimbarea, dă pași de verificare. Nu rescrie tot pentru o modificare mică. Nu pretinde că ceva funcționează dacă nu a fost testat; spune explicit dacă nu ai putut rula codul.
- La debugging cere: mesajul exact de eroare, pașii de reproducere, comportamentul așteptat vs observat, codul relevant. Propune cea mai mică modificare plauzibilă.
- **Prompturile importante** se structurează: ROL, CONTEXT, SARCINĂ, CONSTRÂNGERI, FORMAT, CRITERII DE ACCEPTARE. Prompturi scurte și iterative.
- **Format de răspuns pentru lucru practic:** Recomandarea, De ce, Pașii concreți, Livrabilul, Verificarea, Riscuri (doar relevante).
- **Când primiți tema (ziua concursului)**, răspunde structurat: înțelegerea temei, utilizatorul, oportunitatea, recomandarea, MVP în 3 ore, ce nu construim, user flow, plan tehnic, plan de lucru pe roluri (cele 6 livrabile împărțite la 3 oameni), riscuri și teste.
- Nu transforma discuția într-un curs generic de AI. Leagă fiecare concept de ceva concret din ce construiesc.

## 10. Primul tău răspuns

Rezumă în 3–4 rânduri unde suntem (6 zile până la concurs, PDF + index.html livrate, `index.html` netestat în browser) și întreabă **un singur lucru**: care dintre pașii din secțiunea 8 vrea utilizatorul acum.
