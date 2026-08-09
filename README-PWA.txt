===============================================
  আমাদের যোগিনী বাড়ী - PWA (অ্যাপ) সেটআপ গাইড
===============================================

কী কী ফাইল আছে:
1. manifest.json
2. sw.js
3. এই README ফাইল

===============================================
ধাপ ১: এই দুটি ফাইল আপলোড করো
===============================================
- manifest.json
- sw.js

এই দুটো ফাইল তোমার GitHub রিপোজিটরির মূল ফোল্ডারে (index.html যেখানে আছে সেখানে) আপলোড করো।

===============================================
ধাপ ২: index.html এ কোড যোগ করো
===============================================

A) <head> এর ভিতরে (অন্যান্য meta ট্যাগের কাছে) এই লাইনগুলো যোগ করো:

<link rel="manifest" href="/manifest.json">
<meta name="theme-color" content="#1f4a32">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="যোগিনীবাড়ী">

B) </body> ট্যাগের ঠিক আগে এই স্ক্রিপ্ট যোগ করো:

<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', function() {
      navigator.serviceWorker.register('/sw.js')
        .then(function(reg) {
          console.log('Service Worker registered');
        })
        .catch(function(err) {
          console.log('SW registration failed:', err);
        });
    });
  }
</script>

===============================================
ধাপ ৩: Vercel ডিপ্লয়
===============================================
GitHub-এ সেভ করলে Vercel নিজে থেকে ডিপ্লয় করে দেবে।
১-২ মিনিট অপেক্ষা করো।

===============================================
ধাপ ৪: টেস্ট করো
===============================================
অ্যান্ড্রয়েড Chrome-এ সাইট খোলো → মেনু (⋮) → "Add to Home screen" বা "Install app"

===============================================
নোট
===============================================
- favicon.png ফাইল তোমার সাইটে আগে থেকেই আছে, তাই আইকন কাজ করবে।
- সম্পূর্ণ ফ্রি।
- কোনো পেইড সার্ভিস লাগবে না।
