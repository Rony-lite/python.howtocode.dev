# \# -- coding: utf-8 --

`# -*- coding: utf-8 -*-` এই কমেন্ট লাইনটাকে অনেক পাইথন স্ক্রিপ্টের শুরুতেই দেখা যায়। একটু একটু বোঝা যায় যে এখানে এনকোডিং ডিফাইন করে দেয়া হয়েছে। কিন্তু কিসের এবং কেন? কার জন্যই বা দরকার এটা? প্রথমেই জানতে হবে কম্পিউটারের সাথে টেক্সট নিয়ে কাজ করতে হলে তাকে টেক্সট গুলো চেনাতে হয়, আর আমরা সবাই জানি কম্পিউটার 1, 0 ছাড়া আর কাউকেই চেনে না। তো এনকোডিং এর সহজ মানে হচ্ছে একটা ম্যাপিং টেবিল যেখানে বলা আছে A এর মানে 01000001 \(এটা ASCII এনকোডিং/টেবিল\)। কিন্তু এই টেবিলে দুনিয়ার সব ভাষার সব ক্যারেক্টার এর সাপেক্ষে এরকম কম্পিউটার উপযোগী কোড নাই। এদিকে আমাদের প্রোগ্রাম লিখতে বা টেক্সট ফাইল লিখতে সেই ক্যারেক্টার গুলো লাগতেই পারে। তাই এরকম আরও একটা বিশাল লম্বা টেবিল আছে, utf-8 এনকোডিং/টেবিল। এই টেবিলে বাংলা "ক" সাপেক্ষেও একটা বাইনারি পাওয়ার ব্যবস্থা আছে। তো আমাদের পাইথন প্রোগ্রামে যদি এরকম ASCII এর বাইরের ক্যারেক্টার থাকে তাকে চেনাতে হলে ফাইলের শুরুতে বলে দিতে হবে যে - ভাই পাইথন তুমি আমার এই সোর্স ফাইলকে দয়া করে utf-8 টেবিল/এনকোডিং মোতাবেক পার্স করিয়ো নাহলে বুঝবা না আমি ফাইলে কি লিখছি :\)

নিচের প্রোগ্রামটা যদি একটা `Test.py` ফাইলে লিখে পাইথন ২ দিয়ে রান করাই,

```python
name = "নুহিল"
print(name)
```

তাহলে আউটপুট আসবে,

```python
File "Test.py", line 3
SyntaxError: Non-ASCII character '\xe0' in file Test.py on line 3
```

তাই ওই `Test.py` কে আপডেট করে নিচের মত করতে হবে,

```python
# -*- coding: utf-8 -*-
name = "নুহিল"
print(name)
```

এবার ঠিকঠাক রান করবে। আর হ্যা, ঠিক `# -*- coding: utf-8 -*-` এভাবেই যে সোর্স ফাইলের এনকোডিং ডিফাইন করতে হবে তাও কিন্তু না। `# Please encoding: utf-8` \(সত্যি\) এরকম লিখলেও পাইথন বুঝে যাবে :\) শেষ কথা, এই ঝক্কি ঝামেলা কিন্তু Python 3 তে করতে হবে না কারন পাইথন ৩ ডিফল্ট এনকোডিং হিসেবে utf-8 কেই ধরে নেয় :D

