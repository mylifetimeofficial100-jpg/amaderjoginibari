================================================
  আমাদের যোগিনী বাড়ী — নতুন অ্যাডমিন প্যানেল
  প্রফেশনাল + ইমেজ অটো-কম্প্রেশন + সব ফাইল সাপোর্ট
================================================

১. admin.html ফাইলটি ডাউনলোড করুন।

২. আপনার GitHub রিপোজিটরিতে (amaderjoginibari) 
   পুরনো admin.html এর জায়গায় এই নতুন ফাইলটি আপলোড করুন 
   (অথবা admin.html নামে সেভ করে Vercel-এ ডিপ্লয় করুন)।

৩. Firebase Console → Storage → Rules এ এই রুলস দিন:

rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /posts/{allPaths=**} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}

৪. Firestore Rules (যদি না থাকে):

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /posts/{document=**} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}

৫. মূল সাইটে পোস্ট দেখানোর জন্য:
   firebase-notice-section-updated.html ফাইলের কোড 
   index.html এর খবরাখবর সেকশনে বসিয়ে দিন 
   (পুরনো firebase-notice-section.html এর জায়গায়)।

৬. অ্যাডমিন প্যানেল লিংক:
   https://amaderjoginibari.vercel.app/admin.html
   (ডিপ্লয়ের পর)

================================================
ফিচারসমূহ:
- ছবি অটো কম্প্রেস (১০MB → ২০০-৬০০KB, কোয়ালিটি ক্লিয়ার)
- ভিডিও / অডিও / PDF / যেকোনো ফাইল আপলোড
- ইউটিউব ও এক্সটার্নাল লিংক
- ড্র্যাগ অ্যান্ড ড্রপ
- প্রিভিউ + প্রোগ্রেস বার
- পুরনো পোস্ট ডিলিট
- মোবাইল ফ্রেন্ডলি প্রফেশনাল UI
================================================
