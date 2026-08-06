যোগিনীবাড়ী — লোকেশন সেকশন ফিক্স
================================

কী কী ঠিক করা হয়েছে:
1. ম্যাপ এখন দুর্গানগর ইউনিয়ন পরিষদের দিকে না গিয়ে 
   যোগিনীবাড়ী বায়তুন নূর জামে মসজিদ (7HFC+3P6) এর কাছে দেখাবে।
2. সেকশন অনেক কম জায়গা নেবে (কমপ্যাক্ট)।
3. খুব বেশি হাইলাইট নেই।

কীভাবে আপলোড করবেন:
---------------------
1. GitHub এ যান: https://github.com/mylifetimeofficial100-jpg/amaderjoginibari
2. index.html ফাইল এডিট করুন।
3. <style> ট্যাগের ভিতরে পুরনো location CSS (/* ---------- LOCATION / MAP ---------- */ থেকে পরের section পর্যন্ত) মুছে 
   joginibari-location-css.css এর কোড বসিয়ে দিন।
4. <section class="location-section" id="location"> ... </section> পুরো অংশ মুছে 
   joginibari-location-fix.html এর কোড বসিয়ে দিন।
5. Commit & Push করুন। Vercel নিজে থেকে আপডেট হয়ে যাবে।

ফাইল দুটো:
- joginibari-location-fix.html  → HTML অংশ
- joginibari-location-css.css     → CSS অংশ
