# বুলিয়ান লজিক

if স্টেটমেন্টের জন্য জটিল কন্ডিশন তৈরির ক্ষেত্রে বুলিয়ান লজিক ব্যবহৃত হয়ে থাকে। অর্থাৎ একটি if স্টেটমেন্ট যদি একাধিক কন্ডিশনের উপর নির্ভর করে সেখানে আমরা বুলিয়ান লজিক ব্যবহার করতে পারি। আগেও বলা হয়েছে, পাইথনে and, or এবং not এই তিন ধরণের বুলিয়ান অপারেটর আছে।

**and**  
এই অপারেটর দুটো আর্গুমেন্ট নিয়ে যাচাই করে এবং সত্য হয় যখন দুটো আর্গুমেন্টই সত্য হয়।

```python
>>> 1 == 1 and 2 == 2
True
```

এখানে `1 == 1` সত্য এবং `2 == 2` সত্য। তাই `and` অপারেটর এর আউটপুট `True`. একটি কথা মনে করিয়ে দেয়া দরকার, অন্যান্য প্রোগ্রামিং ল্যাঙ্গুয়েজে এ ধরণের AND, OR বা NOT অপারেটরকে সাধারণত `&&`, `||`, `!` দিয়ে প্রকাশ করা হয় যেখানে পাইথনে শব্দ আকারে লেখা হয়।

**or**  
উপরে উল্লেখিত `and` অপারেটর এর মতই `or` এরও দুটো আর্গুমেন্ট থাকে কিন্তু এটি সত্য হয় যদি উক্ত দুটো আর্গুমেন্টের যেকোনো একটি সত্য হয়। অর্থাৎ নিচের স্টেটমেন্টে,

```python
>>> 1 == 1 or 2 == 3
True
```

এখানে `or` এর বাম পাশের লজিকটি সত্য কিন্তু ডান পাশেরটি সত্য নয়। তারপরেও `or` এর আউটপুট `True`.

**not**  
অন্য দুটি অপারেটর এর মত `not` দুটো আর্গুমেন্ট নিয়ে কাজ করে না। বরং এর জন্য একটি আর্গুমেন্টই যথেষ্ট। এটি দিয়ে চেক করা হয় কোন লজিক **না** হয় কিনা। নিচের উদাহরণ দেখলে পরিষ্কার বোঝা যাবে,

```python
>>> not 1 == 1
False
>>> not 1 > 7
True
```

প্রথম স্টেটমেন্ট এর `1 == 1` এটা আমরা সবাই জানি। এর সামনে `not` জুড়ে দিয়ে দেখার চেষ্টা করছি যে `1 == 1` নয়। কিন্তু এটা আসলে ঠিক না, ১ আর ১ তো সমানই। আর তাই `not 1 == 1` এর আউটপুট আসছে `False`. সেরকম দ্বিতীয় লাইনে দেখছি/পড়ছি `নয় ১ > ৭` এবং এটা সঠিক। আসলেই ১ কিন্তু ৭ এর চেয়ে বড় নয়। তাই `not 1 > 7` স্টেটমেন্টটি সত্য রিটার্ন করছে।

**উদাহরণ**

```python
a = 1
b = 1

c = 5
d = 10

if a == b and d > c:
    print("a and b are equal and d is greater than c")
```

আউটপুট,

```python
a and b are equal and d is greater than c
```

> সংকলন - [নুহিল মেহেদী](https://nuhil.net)

