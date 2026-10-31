# Universal Education IELTS V16 — Frontend Foundation 0.2

આ પેકેજ V15 Master Frontendને cumulative આધાર તરીકે રાખીને V16 Practice Centreનું development foundation છે.

## Files
- `index.html` — login entry page
- `app.js` — V15 cumulative application logic + V16 practice integration
- `style.css` — existing responsive IELTS UI + V16 styles
- `config.js` — NEW V16 Supabase Project URL અને Publishable Key અહીં ઉમેરવાના

## જરૂરી Configuration
1. `config.js` ખોલો.
2. `PASTE_V16_SUPABASE_PROJECT_URL_HERE` ને નવા V16 Supabase Project URLથી બદલો.
3. `PASTE_V16_SUPABASE_PUBLISHABLE_KEY_HERE` ને નવા V16 Publishable Keyથી બદલો.
4. `service_role` અથવા secret key ક્યારેય frontend/GitHubમાં ન મૂકશો.
5. V15 Supabase URL/Key વાપરશો નહીં.

## Security changes in this checkpoint
- Student Practice Set load કરતી વખતે `answer_key` select થતું નથી.
- Browser-side answer grading અને direct client update of final score/status દૂર કર્યાં છે.
- Practice submission હવે `submit-practice-attempt` Edge Functionને મોકલે છે.
- તે Edge Function હજી build/compile/live-test/deploy થયેલી નથી; તેથી submit feature હાલ કામ નહીં કરે. આ સુરક્ષિત રીતે fail-closed રહેશે.

## Not production-ready
આ Development Foundation છે, final V16 frontend નથી. નીચેના integration કામ બાકી છે:
- Secure `submit-practice-attempt` Edge Function અને matching autosave/resume API.
- Username/Student ID loginને identifier-login Edge Function સાથે integrate કરવું; હાલ inherited V15 login code હજી legacy synthetic-email flow વાપરે છે.
- Full IELTS question-type visual editor and renderer.
- Speaking audio recording/upload/review workflow.
- Full writing patterns, notifications, analytics, goals/calendar and role-permission validation.
- Student/Faculty/Sub Admin/Main Admin live role testing.

**આ ZIPને હમણાં Public GitHub Repositoryમાં upload અથવા deploy ન કરશો.** પહેલાં config, backend integration અને security tests પૂર્ણ થવા જોઈએ.
