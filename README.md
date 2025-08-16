<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>آموزش جامع ریاضی نهم — کامل</title>
<style>
  :root{
    --navy:#1A237E;         /* سرمه‌ای */
    --navy-soft:#303F9F;    /* سرمه‌ای ملایم */
    --cream:#f7f3e9;        /* کرمی */
    --pistachio:#CFE8D8;    /* نخودی */
    --light-blue:#E6F7FF;   /* آبی روشن */
    --peach:#FFB3A7;        /* گل‌بهی (جایگزین خردلی) */
    --card:#fffaf0;
    --ink:#17203a;
  }
  *{box-sizing:border-box}
  html,body{margin:0;padding:0;background:var(--cream);color:var(--ink);font-family:Tahoma,Arial,Helvetica,sans-serif;line-height:1.45}
  header{background:var(--navy);color:#fff;padding:16px;text-align:center;position:sticky;top:0;z-index:20}
  header h1{margin:0;font-size:20px}
  .wrap{max-width:1100px;margin:auto;padding:14px}
  .note{background:var(--card);padding:12px;border-radius:10px;border:1px solid #efe7d8;margin-bottom:12px;font-size:14px}
  .grid{display:grid;grid-template-columns:1fr 320px;gap:16px}
  @media (max-width:980px){ .grid{grid-template-columns:1fr} }
  main{min-width:0}
  .chapter{background:#fff;border-radius:10px;padding:12px;margin-bottom:12px;border:1px solid #eee}
  .chapter h2{margin:0 0 8px;color:var(--navy);display:flex;justify-content:space-between;align-items:center}
  .pill{padding:6px 10px;border-radius:999px;font-size:13px}
  .pill.free{background:#43A047;color:white}
  .pill.locked{background:var(--peach);color:#5b2a1f}
  .lessons{display:grid;gap:10px}
  .lesson{padding:10px;border-radius:8px;background:linear-gradient(180deg,#fff,var(--light-blue));border-left:6px solid var(--peach)}
  .row{display:flex;gap:8px;flex-wrap:wrap;align-items:center}
  .btn{appearance:none;border:0;padding:8px 12px;border-radius:8px;cursor:pointer;font-weight:600}
  .btn.primary{background:var(--navy);color:#fff}
  .btn.link{background:transparent;color:var(--navy);text-decoration:underline;border:0;padding:4px;cursor:pointer}
  .btn.pay{background:var(--peach);color:#5b2a1f}
  .anim-box{background:var(--card);border:1px dashed var(--navy-soft);border-radius:10px;padding:10px;min-height:120px;margin-top:8px}
  .gif-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:10px}
  .media-thumb{width:100%;height:auto;border-radius:6px;border:1px solid #eee}
  .sidebar-card{background:var(--card);padding:12px;border-radius:10px;border:1px solid #efe7d8;margin-bottom:12px}
  footer{padding:16px;text-align:center;color:#fff;background:var(--navy);margin-top:16px;border-radius:6px}
  /* modal */
  .modal{position:fixed;inset:0;background:rgba(10,12,30,0.6);display:flex;align-items:center;justify-content:center;z-index:999;display:none}
  .modal.open{display:flex}
  .modal .box{width:min(920px,95%);background:#fff;padding:12px;border-radius:8px;max-height:90vh;overflow:auto}
  .modal .close{float:left;background:transparent;border:0;font-size:18px;cursor:pointer}
  .missing{padding:8px;border-radius:6px;background:#fff5f0;border:1px solid #ffd2c2;color:#8b3d2d}
  .lessonnote{background:#fff;padding:12px;border-radius:8px;border:1px solid #efe7d8;margin-top:8px;max-height:340px;overflow:auto}
  .note-title{color:var(--navy);font-weight:700;margin-bottom:8px}
</style>
</head>
<body>
<header>
  <h1>آموزش جامع ریاضی نهم — همهٔ مطالب یکجا</h1>
  <p style="margin:6px 0 0;font-size:13px">فصل اول کامل رایگان است. بقیه فصل‌ها با پرداخت جداگانه (تستی) قفل‌اند.</p>
</header>

<div class="wrap">
  <div class="note">
    <strong>راهنما — ساختار فایل‌ها و media/ :</strong>
    <ul style="margin:6px 0 0 18px;font-size:14px">
      <li>در کنار این فایل `index.html` پوشه‌ای بساز به نام <code>media</code>.</li>
      <li>نام‌گذاری فایل‌ها طبق الگو: <code>media/{ch}_{l}.mp4</code>, <code>media/{ch}_{l}.pdf</code>, <code>media/{ch}_{l}.gif</code>؛ مثال: فصل 1 درس 2 → <code>media/ch1_l2.mp4</code>.</li>
      <li>برای تست فعلاً نیازی به همهٔ فایل‌ها نیست — سیستم پیام جای خالی را نمایش می‌دهد.</li>
    </ul>
  </div>

  <div class="grid">
    <main>
      <!-- Chapter templates (eight chapters) -->
      <!-- CHAPTER 1 (FREE) -->
      <section class="chapter" id="ch1">
        <h2>فصل اول: مجموعه‌ها <span class="pill free">رایگان</span></h2>
        <div class="lessons">
          <!-- lesson 1 -->
          <article class="lesson">
            <div class="row"><strong>درس اول:</strong> معرفی مجموعه</div>
            <div class="row">
              <button class="btn link" onclick="showLocalVideo('ch1','l1')">پخش ویدیو</button>
              <button class="btn link" onclick="openPDF('ch1','l1')">باز کردن نمونه‌سوال (PDF)</button>
              <button class="btn link" onclick="showAnim('ch1','l1')">نمایش انیمیشن / GIF</button>
              <button class="btn primary" onclick="toggleLessonNote('ch1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch1" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — معرفی مجموعه</div>
              <p>در این درس با مفهوم مجموعه آشنا می‌شویم: تعریف مجموعه، اعضا، نمایش مجموعه، نمایش به کمک { }، نمایش به کمک نمودار وِن و مثال‌های ساده. هدف: توانایی تشخیص عضو بودن و نوشتن مجموعه‌ها به چند روش.</p>
              <ol>
                <li>تعریف مجموعه و نمادها</li>
                <li>نحوهٔ نوشتن عناصر</li>
                <li>مثال‌ها و تمرین‌های ساده</li>
              </ol>
            </div>
          </article>

          <!-- lesson 2 -->
          <article class="lesson">
            <div class="row"><strong>درس دوم:</strong> مجموعه‌های برابر و نمایش مجموعه‌ها</div>
            <div class="row">
              <button class="btn link" onclick="showLocalVideo('ch1','l2')">پخش ویدیو</button>
              <button class="btn link" onclick="openPDF('ch1','l2')">نمونه‌سوال</button>
              <button class="btn link" onclick="showAnim('ch1','l2')">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch1_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch1_l2" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — مجموعه‌های برابر و نمایش مجموعه‌ها</div>
              <p>در این درس معیارهای برابری مجموعه‌ها، نمایش مجموعه‌ها با عناصر و با شرایط، و کاربردها بررسی می‌شود. مثال‌های تمرینی همراه با نکات رایج اشتباه حل شده‌اند.</p>
            </div>
          </article>

          <!-- lesson 3 (venn) -->
          <article class="lesson" id="ch1-l3">
            <div class="row"><strong>درس سوم:</strong> اجتماع، اشتراک و تفاضل مجموعه‌ها (انیمیشن تعاملی)</div>
            <div class="row">
              <button class="btn link" onclick="showLocalVideo('ch1','l3')">پخش ویدیو</button>
              <button class="btn link" onclick="openPDF('ch1','l3')">نمونه‌سوال</button>
              <button class="btn link" onclick="showAnim('ch1','l3')">انیمیشن / GIF</button>
              <button class="btn primary" onclick="toggleLessonNote('ch1_l3')">درسنامه کامل</button>
            </div>
            <div class="anim-box">
              <div id="vennArea" style="position:relative;height:200px;background:#fff;border-radius:8px;border:1px solid #efe7d8;overflow:hidden">
                <div id="A" class="circle" style="position:absolute;border-radius:50%;width:130px;height:130px;background:var(--navy);opacity:.72;top:30px;left:24px;cursor:grab"></div>
                <div id="B" class="circle" style="position:absolute;border-radius:50%;width:130px;height:130px;background:var(--light-blue);opacity:.72;top:40px;left:100px;cursor:grab"></div>
                <div id="vennHint" style="position:absolute;bottom:8px;left:0;right:0;text-align:center;color:#445;font-size:13px">A ∪ B — A ∩ B — A \\ B</div>
              </div>
            </div>
            <div id="lessonnote-ch1_l3" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — اجتماع، اشتراک و تفاضل</div>
              <p>اجتماع (∪)، اشتراک (∩) و تفاضل (\\) را تعریف می‌کنیم، قوانین بنیادی و مثال‌های متنوع می‌آوریم. تمرین‌ها شامل رسم نمودارهای وِن و تعیین اعضای اجتماع/اشتراک است.</p>
            </div>
          </article>

          <!-- lesson 4 -->
          <article class="lesson">
            <div class="row"><strong>درس چهارم:</strong> مجموعه‌ها و احتمال</div>
            <div class="row">
              <button class="btn link" onclick="showLocalVideo('ch1','l4')">پخش ویدیو</button>
              <button class="btn link" onclick="openPDF('ch1','l4')">نمونه‌سوال</button>
              <button class="btn link" onclick="showAnim('ch1','l4')">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch1_l4')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch1_l4" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — مجموعه‌ها و احتمال</div>
              <p>ارتباط مجموعه‌ها با احتمال‌سنجی ساده: فضای نمونه، رویدادها، و احتمال رویداد. مثال‌های ابتدایی با سکه، تاس و نمونه مسائل کلاسی.</p>
            </div>
          </article>
        </div>
      </section>

      <!-- The remaining chapters (2..8) follow the same pattern (lessonnote + links) -->
      <!-- For brevity, content is similar in structure. They start locked and open after buyChapter() -->
      <!-- CHAPTER 2 -->
      <section class="chapter" id="ch2">
        <h2>فصل دوم: اعداد حقیقی <span id="ch2-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch2-lessons">
          <article class="lesson">
            <div class="row"><strong>درس اول:</strong> عددهای گویا</div>
            <div class="row">
              <button class="btn link" data-ch="ch2" data-l="l1" onclick="requireAccess(this)">پخش ویدیو</button>
              <button class="btn link" data-ch="ch2" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch2" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch2_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch2_l1" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — عددهای گویا</div>
              <p>مفهوم اعداد گویا، نمایش به صورت کسری، ویژگی‌ها و مثال‌ها.</p>
            </div>
          </article>

          <article class="lesson">
            <div class="row"><strong>درس دوم:</strong> عددهای حقیقی</div>
            <div class="row">
              <button class="btn link" data-ch="ch2" data-l="l2" onclick="requireAccess(this)">پخش ویدیو</button>
              <button class="btn link" data-ch="ch2" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch2" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch2_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch2_l2" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — عددهای حقیقی</div>
              <p>مجموعهٔ اعداد حقیقی، تفاوت با اعداد گویا، و نمایش روی محور اعداد.</p>
            </div>
          </article>

          <article class="lesson">
            <div class="row"><strong>درس سوم:</strong> قدر مطلق و محاسبه تقریبی</div>
            <div class="row">
              <button class="btn link" data-ch="ch2" data-l="l3" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch2" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch2" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch2_l3')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch2_l3" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — قدر مطلق</div>
              <p>تعریف، خواص، و کاربرد قدر مطلق؛ تقریب و خطای محاسباتی ساده.</p>
            </div>
          </article>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch2')">خرید فصل دوم — پرداخت تست</button></div>
      </section>

      <!-- CHAPTER 3 -->
      <section class="chapter" id="ch3">
        <h2>فصل سوم: استدلال و اثبات در هندسه <span id="ch3-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch3-lessons">
          <article class="lesson"><div class="row"><strong>درس اول:</strong> استدلال</div>
            <div class="row">
              <button class="btn link" data-ch="ch3" data-l="l1" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch3" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch3" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch3_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch3_l1" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — استدلال</div>
              <p>مراحل استدلال هندسی، استنتاج و استدلال قیاسی و نمونهٔ اثبات کوتاه.</p>
            </div>
          </article>
          <!-- more lessons ... (same pattern) -->
          <article class="lesson"><div class="row"><strong>درس دوم:</strong> آشنایی با اثبات در هندسه</div>
            <div class="row">
              <button class="btn link" data-ch="ch3" data-l="l2" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch3" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch3" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch3_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch3_l2" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — آشنایی با اثبات</div>
              <p>انواع اثبات (مستقیم، خلف و ...)، مثال‌های ساده و نحوهٔ نوشتن اثبات کوتاه.</p>
            </div>
          </article>

          <article class="lesson"><div class="row"><strong>درس سوم:</strong> هم‌نوشتی مثلث‌ها</div>
            <div class="row">
              <button class="btn link" data-ch="ch3" data-l="l3" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch3" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch3" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch3_l3')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch3_l3" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — هم‌نوشتی مثلث‌ها</div>
              <p>شرایط هم‌نوشتی، پس‌درجات، و مثال‌های حل‌شده.</p>
            </div>
          </article>

          <article class="lesson"><div class="row"><strong>درس چهارم:</strong> حل مسئله در هندسه</div>
            <div class="row">
              <button class="btn link" data-ch="ch3" data-l="l4" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch3" data-l="l4" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch3" data-l="l4" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch3_l4')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch3_l4" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — حل مسئله</div>
              <p>روش‌های حل مسئله، نکات محوری و مثال‌های مرحله‌ای.</p>
            </div>
          </article>

          <article class="lesson"><div class="row"><strong>درس پنجم:</strong> شکل‌های متشابه</div>
            <div class="row">
              <button class="btn link" data-ch="ch3" data-l="l5" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch3" data-l="l5" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch3" data-l="l5" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch3_l5')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch3_l5" class="lessonnote" style="display:none;">
              <div class="note-title">درسنامه — شکل‌های متشابه</div>
              <p>تعریف تشابه، نسبت‌ها، کاربرد در حل مسائل و مثال‌ها.</p>
            </div>
          </article>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch3')">خرید فصل سوم — پرداخت تست</button></div>
      </section>

      <!-- CHAPTER 4 -->
      <section class="chapter" id="ch4">
        <h2>فصل چهارم: توان و ریشه <span id="ch4-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch4-lessons">
          <article class="lesson"><div class="row"><strong>درس اول:</strong> توان صحیح</div>
            <div class="row">
              <button class="btn link" data-ch="ch4" data-l="l1" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch4" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch4" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch4_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch4_l1" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — توان صحیح</div><p>قوانین توان‌ها، ضرب توان‌ها، جمع و ...</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس دوم:</strong> نماد علمی</div>
            <div class="row">
              <button class="btn link" data-ch="ch4" data-l="l2" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch4" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch4" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch4_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch4_l2" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — نماد علمی</div><p>نمایش عددها در نماد علمی، کاربردها و تمرین‌ها.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس سوم:</strong> ریشه‌گیری</div>
            <div class="row">
              <button class="btn link" data-ch="ch4" data-l="l3" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch4" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch4" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch4_l3')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch4_l3" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — ریشه‌گیری</div><p>قوانین رادیکال و مثال‌ها.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس چهارم:</strong> جمع و تفریق رادیکال‌ها</div>
            <div class="row">
              <button class="btn link" data-ch="ch4" data-l="l4" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch4" data-l="l4" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch4" data-l="l4" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch4_l4')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch4_l4" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — جمع و تفریق رادیکال‌ها</div><p>روش‌ها و مثال‌های تمرینی.</p></div>
          </article>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch4')">خرید فصل چهارم — پرداخت تست</button></div>
      </section>

      <!-- CHAPTER 5 -->
      <section class="chapter" id="ch5">
        <h2>فصل پنجم: عبارت‌های جبری <span id="ch5-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch5-lessons">
          <article class="lesson"><div class="row"><strong>درس اول:</strong> عبارت‌های جبری و مفهوم اتحاد</div>
            <div class="row">
              <button class="btn link" data-ch="ch5" data-l="l1" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch5" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch5" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch5_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch5_l1" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — اتحادها</div><p>مربع دو جمله‌ای و مثال‌های کاربردی.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس دوم:</strong> چند اتحاد دیگر، تجزیه و کاربردها</div>
            <div class="row">
              <button class="btn link" data-ch="ch5" data-l="l2" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch5" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch5" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch5_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch5_l2" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — تجزیه</div><p>روش‌های تجزیه و کاربرد در حل مسئله.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس سوم:</strong> نابرابری و نامعادله‌ها</div>
            <div class="row">
              <button class="btn link" data-ch="ch5" data-l="l3" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch5" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch5" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch5_l3')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch5_l3" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — نابرابری</div><p>تعاریف، روش‌ها و تمرینات.</p></div>
          </article>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch5')">خرید فصل پنجم — پرداخت تست</button></div>
      </section>

      <!-- CHAPTER 6 -->
      <section class="chapter" id="ch6">
        <h2>فصل ششم: خط و معادلات خطی <span id="ch6-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch6-lessons">
          <article class="lesson"><div class="row"><strong>درس اول:</strong> معادلهٔ خط</div>
            <div class="row">
              <button class="btn link" data-ch="ch6" data-l="l1" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch6" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch6" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch6_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch6_l1" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — معادلهٔ خط</div><p>معادله خط به صورت y=mx+c، شیب و مثال‌ها.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس دوم:</strong> شیب و عرض از مبدأ</div>
            <div class="row">
              <button class="btn link" data-ch="ch6" data-l="l2" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch6" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch6" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch6_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch6_l2" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — شیب و عرض</div><p>تعریف شیب، محاسبه و کاربردها.</p></div>
          </article>
          <article class="lesson" id="ch6-steps"><div class="row"><strong>درس سوم:</strong> دستگاه معادله‌های خطی</div>
            <div class="row">
              <button class="btn link" onclick="runSteps()">نمایش مرحله‌ای</button>
              <button class="btn link" data-ch="ch6" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch6" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch6_l3')">درسنامه کامل</button>
            </div>
            <div class="anim-box"><div class="steps" id="steps"><div class="step">۲x + ۳ = ۷</div><div class="step">۲x = ۴</div><div class="step">x = ۲</div></div></div>
            <div id="lessonnote-ch6_l3" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — دستگاه معادله‌ها</div><p>روش‌های حل دستگاه‌ها: حذف، جایگزینی و نمونه‌ها.</p></div>
          </article>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch6')">خرید فصل ششم — پرداخت تست</button></div>
      </section>

      <!-- CHAPTER 7 -->
      <section class="chapter" id="ch7">
        <h2>فصل هفتم: عبارت‌های گویا <span id="ch7-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch7-lessons">
          <article class="lesson"><div class="row"><strong>درس اول:</strong> معرفی و ساده کردن عبارت‌های گویا</div>
            <div class="row">
              <button class="btn link" data-ch="ch7" data-l="l1" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch7" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch7" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch7_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch7_l1" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — عبارت‌های گویا</div><p>تعریف، ساده‌سازی و نکات مهم.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس دوم:</strong> محاسبات عبارت‌های گویا</div>
            <div class="row">
              <button class="btn link" data-ch="ch7" data-l="l2" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch7" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch7" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch7_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch7_l2" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — محاسبات</div><p>قوانین محاسبات و مثال‌ها.</p></div>
          </article>
          <article class="lesson"><div class="row"><strong>درس سوم:</strong> تقسیم چند جمله‌ای‌ها</div>
            <div class="row">
              <button class="btn link" data-ch="ch7" data-l="l3" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch7" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch7" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch7_l3')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch7_l3" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — تقسیم چند جمله‌ای</div><p>روش تقسیم، نکات و تمرین‌ها.</p></div>
          </article>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch7')">خرید فصل هفتم — پرداخت تست</button></div>
      </section>

      <!-- CHAPTER 8 -->
      <section class="chapter" id="ch8">
        <h2>فصل هشتم: حجم و مساحت <span id="ch8-pill" class="pill locked">قفل شده</span></h2>
        <div class="lessons" id="ch8-lessons">
          <article class="lesson"><div class="row"><strong>درس اول:</strong> حجم و مساحت کره</div>
            <div class="row">
              <button class="btn link" data-ch="ch8" data-l="l1" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch8" data-l="l1" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch8" data-l="l1" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch8_l1')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch8_l1" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — کره</div><p>فرمول‌ها، مثال‌های محاسباتی و نکات کاربردی.</p></div>
          </article>

          <article class="lesson"><div class="row"><strong>درس دوم:</strong> حجم هرم و مخروط</div>
            <div class="row">
              <button class="btn link" data-ch="ch8" data-l="l2" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch8" data-l="l2" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch8" data-l="l2" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch8_l2')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch8_l2" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — هرم و مخروط</div><p>فرمول‌ها و مثال‌ها برای هرم و مخروط.</p></div>
          </article>

          <article class="lesson"><div class="row"><strong>درس سوم:</strong> سطح و حجم</div>
            <div class="row">
              <button class="btn link" data-ch="ch8" data-l="l3" onclick="requireAccess(this)">ویدیو</button>
              <button class="btn link" data-ch="ch8" data-l="l3" onclick="requireAccess(this)">نمونه‌سوال</button>
              <button class="btn link" data-ch="ch8" data-l="l3" onclick="requireAccess(this)">انیمیشن</button>
              <button class="btn primary" onclick="toggleLessonNote('ch8_l3')">درسنامه کامل</button>
            </div>
            <div id="lessonnote-ch8_l3" class="lessonnote" style="display:none;"><div class="note-title">درسنامه — سطح و حجم</div><p>جمع‌بندی فرمول‌ها و تمرینات نهایی.</p></div>
          </article>

          <div class="anim-box" style="margin-top:8px">
            <h4 style="margin:4px 0;color:var(--navy)">نمونه GIFهای آموزشی (قابل جایگزینی)</h4>
            <div class="gif-grid">
              <img class="media-thumb" src="media/ch8_l1.gif" alt="کره (GIF)" onerror="this.style.display='none'">
              <img class="media-thumb" src="media/ch8_l2.gif" alt="مخروط (GIF)" onerror="this.style.display='none'">
              <img class="media-thumb" src="media/ch8_l3.gif" alt="هرم (GIF)" onerror="this.style.display='none'">
            </div>
          </div>
        </div>
        <div style="margin-top:10px"><button class="btn pay" onclick="buyChapter('ch8')">خرید فصل هشتم — پرداخت تست</button></div>
      </section>

    </main>

    <aside>
      <div class="sidebar-card">
        <h3 style="margin:0 0 8px;color:var(--navy)">پیشرفت و دسترسی</h3>
        <div id="accessList" class="small">فقط فصل اول رایگان است.</div>
      </div>

      <div class="sidebar-card">
        <h4 style="margin:0 0 8px;color:var(--navy)">راهنما سریع</h4>
        <div class="small">
          <ul style="margin:0 0 0 18px">
            <li>پوشهٔ <code>media</code> را کنار این فایل بساز و فایل‌ها را طبق الگو قرار بده.</li>
            <li>برای پرداخت واقعی (زرین‌پال) من آماده‌سازی بک‌اند و تغییرات لازم را برایت می‌نویسم.</li>
            <li>برای آنلاین شدن: تمام فایل‌ها را در repo بریز و GitHub Pages فعال کن.</li>
          </ul>
        </div>
      </div>
    </aside>
  </div>

  <footer>© 2025 آموزش جامع ریاضی نهم</footer>
</div>

<!-- Modal for media preview -->
<div id="modal" class="modal" role="dialog" aria-modal="true" aria-hidden="true">
  <div class="box">
    <button class="close" onclick="closeModal()">✕ بستن</button>
    <div id="modalContent" style="margin-top:8px"></div>
  </div>
</div>

<script>
/* ---------------- Utilities for local media paths ---------------- */
function mediaPath(ch, lesson, ext){
  return 'media/' + ch + '_' + lesson + '.' + ext;
}

/* ---------------- Show local video in modal ---------------- */
function showLocalVideo(ch, lesson){
  const path = mediaPath(ch, lesson, 'mp4');
  const html = `<video controls style="width:100%;height:auto" onerror="handleMediaError(this)">
    <source src="${path}" type="video/mp4">مرورگر شما از پخش این ویدیو پشتیبانی نمی‌کند.</video>`;
  showModal(html);
}

/* ---------------- Open PDF in new tab ---------------- */
function openPDF(ch, lesson){
  const path = mediaPath(ch, lesson, 'pdf');
  window.open(path, '_blank');
}

/* ---------------- Show animation/gif in modal ---------------- */
function showAnim(ch, lesson){
  const img = mediaPath(ch, lesson, 'gif');
  const html = `<img src="${img}" alt="animation" style="width:100%;height:auto" onerror="this.onerror=null;this.style.display='none';document.getElementById('modalContent').innerHTML='<div class=missing>انیمیشن یافت نشد — فایل ${img} را در پوشه media قرار دهید.</div>';">`;
  showModal(html);
}

/* ---------------- Modal control ---------------- */
function showModal(innerHtml){
  const modal = document.getElementById('modal');
  document.getElementById('modalContent').innerHTML = innerHtml;
  modal.classList.add('open');
  modal.setAttribute('aria-hidden','false');
}
function closeModal(){
  const modal = document.getElementById('modal');
  modal.classList.remove('open');
  modal.setAttribute('aria-hidden','true');
  document.getElementById('modalContent').innerHTML = '';
}

/* ----------------- Lessonnote toggle ----------------- */
function toggleLessonNote(id){
  // id is like 'ch1' or 'ch1_l2' etc.
  const el = document.getElementById('lessonnote-' + id);
  if(!el) return alert('درسنامه یافت نشد.');
  // if chapter locked, require access
  const ch = id.split('_')[0]; // 'ch2' or 'ch1'
  if(document.getElementById(ch + '-pill') && document.getElementById(ch + '-pill').classList.contains('locked')){
    // require purchase
    if(!confirm('این فصل قفل است. پرداخت تستی را انجام می‌دهید؟')) return;
    buyChapter(ch);
    // after unlock, show (buyChapter stores and updates UI)
    setTimeout(()=>{ el.style.display = 'block'; }, 700);
    return;
  }
  el.style.display = (el.style.display === 'none' || el.style.display === '') ? 'block' : 'none';
}

/* ---------------- requireAccess handler for locked lessons ---------------- */
function requireAccess(btn){
  const ch = btn.getAttribute('data-ch'), l = btn.getAttribute('data-l');
  if(localStorage.getItem('purchased_' + ch) === '1'){ showLocalVideo(ch,l); }
  else{
    if(confirm('این فصل قفل است. می‌خواهید پرداخت تستی را انجام دهید؟')){ buyChapter(ch); }
  }
}

/* ---------------- Payment simulation & unlocking chapters ---------------- */
/*
  - buyChapter(id): شبیه‌سازی پرداخت؛ پس از موفقیت، localStorage ست می‌شود و UI بروزرسانی می‌شود.
  - برای پرداخت واقعی: این تابع را به آدرس backend متصل کن که با زرین‌پال کار می‌کند.
*/
const chapters = ['ch2','ch3','ch4','ch5','ch6','ch7','ch8'];
function buyChapter(chId){
  if(confirm('پرداخت تستی برای ' + chId + ' انجام شود؟ (شبیه‌سازی)')){
    setTimeout(()=>{
      localStorage.setItem('purchased_' + chId, '1');
      unlockChapterUI(chId);
      alert('پرداخت موفق (تستی). فصل باز شد.');
    },600);
  }
}

function unlockChapterUI(chId){
  const pill = document.getElementById(chId + '-pill');
  if(pill){ pill.className = 'pill free'; pill.textContent = 'دسترسی فعال'; }
  updateAccessList();
}

function checkUnlocked(){
  chapters.forEach(ch=>{
    if(localStorage.getItem('purchased_' + ch) === '1'){ unlockChapterUI(ch); }
  });
}

function updateAccessList(){
  const list = [];
  chapters.forEach(ch=>{
    if(localStorage.getItem('purchased_' + ch) === '1'){
      const map = {'ch2':'فصل دوم','ch3':'فصل سوم','ch4':'فصل چهارم','ch5':'فصل پنجم','ch6':'فصل ششم','ch7':'فصل هفتم','ch8':'فصل هشتم'}[ch];
      if(map) list.push(map);
    }
  });
  const el = document.getElementById('accessList');
  el.textContent = list.length ? 'فصول باز: ' + list.join(' ، ') : 'فقط فصل اول رایگان است.';
}

/* ---------------- Venn drag interaction ---------------- */
(function(){
  const area = document.getElementById('vennArea');
  if(!area) return;
  const A = document.getElementById('A'), B = document.getElementById('B');
  let dragged=null, dx=0, dy=0;
  function start(e){
    dragged = e.target;
    const rect = dragged.getBoundingClientRect();
    dx = (e.clientX || (e.touches && e.touches[0].clientX)) - rect.left;
    dy = (e.clientY || (e.touches && e.touches[0].clientY)) - rect.top;
    dragged.style.cursor='grabbing';
  }
  function move(e){
    if(!dragged) return;
    const clientX = e.clientX || (e.touches && e.touches[0].clientX);
    const clientY = e.clientY || (e.touches && e.touches[0].clientY);
    const rect = area.getBoundingClientRect();
    let x = clientX - rect.left - dx;
    let y = clientY - rect.top - dy;
    x = Math.max(-10, Math.min(rect.width - dragged.offsetWidth + 10, x));
    y = Math.max(-10, Math.min(rect.height - dragged.offsetHeight + 10, y));
    dragged.style.left = x + 'px'; dragged.style.top = y + 'px';
    updateBg();
  }
  function end(){ if(dragged) dragged.style.cursor='grab'; dragged=null; }
  [A,B].forEach(el=>{
    el.addEventListener('mousedown', start);
    el.addEventListener('touchstart', start, {passive:false});
  });
  document.addEventListener('mousemove', move);
  document.addEventListener('mouseup', end);
  document.addEventListener('touchmove', move, {passive:false});
  document.addEventListener('touchend', end);
  function updateBg(){
    const ar = A.getBoundingClientRect(), br = B.getBoundingClientRect();
    const ox = Math.max(0, Math.min(ar.right, br.right) - Math.max(ar.left, br.left));
    const oy = Math.max(0, Math.min(ar.bottom, br.bottom) - Math.max(ar.top, br.top));
    area.style.background = (ox*oy) > 0 ? '#e8f4ff' : '#fff';
  }
})();

/* ---------------- Steps animation for equations ---------------- */
function runSteps(){
  const items = document.querySelectorAll('#steps .step');
  items.forEach(el=>el.classList.remove('on'));
  items.forEach((el,i)=>setTimeout(()=>el.classList.add('on'), i*600));
}

/* ---------------- media error handler for <video> ---------------- */
function handleMediaError(el){
  const parent = document.getElementById('modalContent');
  parent.innerHTML = `<div class="missing">فایل ویدیو پیدا نشد — لطفاً فایل مربوط را در پوشهٔ <code>media</code> قرار دهید.</div>`;
}

/* ---------------- Init ---------------- */
document.addEventListener('DOMContentLoaded', function(){
  checkUnlocked();
  updateAccessList();
});
</script>
</body>
</html>
