---
published: true
layout: bookpage
weight: 78
section: Workflow
title: افزودن گلیف به یک قلم عربی
---

## مقدمه

گاهی ممکن است یک قلم یک یا چند گلیف که برای کار شما اساسی است را نداشته باشد. در قلم‌های عربی این مسئله‌ای خاص است چرا که شکل یک گلیف نه‌تنها به محل آن در واژه بلکه به ویژگی‌های خود حرف نیز بستگی دارد. برای مثال در واژهٔ بی‌معنی *بَبَب*، حرف *ب* بسته به جایگاهش در واژه در سه شکل مختلف شامل شکل آغازین، میانی و پایانی آمده است در حالی که در واژهٔ *دَدَد*  حرف *د* مستقل از جایگاهش در واژه، تنها یک شکل دارد.

قلم‌های با پروانه‌های باز (مثل [GPL](http://gnu.org/copyleft/gpl.html) یا [OFL](http://scripts.sil.org/OFL-FAQ_web)) به کاربر اجازهٔ ویرایش می‌دهند. در صورتی که بخواهید یک قلم با پروانه‌ای باز را ویرایش و بازنشر کنید لازم است که اشاره‌های مربوط به حق رونوشت خالق اصلی و اطلاعات مربوط به پروانهٔ قلم را نگه دارید.  هرچند می‌توانید یادداشتی دربارهٔ حق رونوشت خودتان نیز به آن بیفزایید.

<img src="images/beh_dal.png" />

این فصل یک راهنمای گام‌به‌گام افزودن یک گلیف به یک قلم عربی است. قلم استفاده شده در این راهنما *گراف* ([Graph](http://openfontlibrary.org/en/font/graph)) است و قرار است حرف *پ* (U+067E) که در زبان عربی وجود ندارد اما در زبان‌های دیگری از جمله فارسی وجود دارد به آن اضافه شود. (می‌توانید فهرستی از همهٔ گلیف‌های خط عربی [Unicode charts](http://www.unicode.org/charts) را ببینید.)

<img src="images/peh.png" />

## رونوشتی از قلم تهیه کنید

قلم را از سایتش بارگیری کنید و اگر یک فایل فشرده است آن را بازگشایی کنید. نرم‌افزار فونت‌فورج را باز کرده و قلم را بارگذاری کنید. آن را دوباره با فرمت *sfd* و با اسمی جدید مثل **GraphNew.sfd** ذخیره کنید.

## تغییر نام قلم

### چرا نام قلم باید عوض شود؟

اگر نام قلم عوض نشود، قلم تغییر یافته جدا از قلم اصلی نصب نمی‌شود یعنی برای نصب قلم جدید لازم است که اول قلم قبلی را از روی سیستم حذف کنید. همچنین در صورتی که می‌خواهید قلم جدید را بازنشر کنید داشتن یک اسم جدید منطقی است. همچنین در صورتی که خالق اصلی قلم اسمش را در مکانیسم Reserved Font Name (RFN) رزرو کرده باشد، فقط خودش امکان استفاده از آن نام را خواهد داشت.

### تغییر داده‌های نام

از گزینگان بالای نرم‌افزار  **Element > Font Info** را انتخاب کنید. در پنجرهٔ باز شده در زبانهٔ *PS Names* مقادیر  *Fontname*, *Family Name*, و *Name For Humans*  را تغییر دهید. در این مثال آن‌ها را به اسم **GraphNew** تغییر می‌دهیم.

<img src="images/font_rename.png" />

در صورت تمایل می‌توانید در بخش *Copyright* اسم خودتان را به‌عنوان کسی که گلیف‌هایی به قلم اضافه کرده درج کنید. مثلاً با عبارت زیر: 'Additional glyphs added by...'.

در همان پنجره در زبانهٔ *TTF Names* مقادیر *Family* و *Fullname* باید مطابق با اسم جدید دیده شوند. مقادیر *Preferred Family* و *Compatible Full* را نیز به اسم قلم جدید تغییر دهید.

اکنون پس از این تغییر اسم‌ها قلم شما به‌عنوان یک قلم جدید شناسایی می‌شود و در کنار قلم اصلی قابل‌نصب خواهد بود.

در همین زبانه هم می‌توانید به اسم خودتان به‌عنوان اضافه کنندهٔ گلیف‌های جدید اشاره کنید. با چیزی مثل جملهٔ Additional glyphs added by در بخش Designer.

دکمهٔ  **OK** را برای ذخیرهٔ تغییرات فشار دهید. یک پیام مبنی بر ساخت یک شناسهٔ یکتای جدید دریافت خواهید کرد. روی دکمهٔ  **Change** کلیک کنید.

## افزودن گلیف برای شکل مستقل *پ*

در چارت قلم به بخش عربی بروید. برای این کار می‌توانید گزینهٔ **View &mdash; Go to** را انتخاب کنید و پس از انتخاب **Arabic** از منوی کشویی، روی **OK** بزنید.

با کلیک کردن روی یک سلول در چارت قلم کد یونیکد آن به همراه اسمش در پنل بالا به رنگ آبی نمایش داده می‌شود. به سلول با کد ۱۶۶۲ یعنی حرف پ بروید. خواهید دید که در بالا عبارت 1662 (0x67e) U+067E "uni067E" ARABIC LETTER PEH* دیده می‌شود. روی سلول به‌جای یک شکل گلیف یک ضربدر خاکستری دیده می‌شود که یعنی این سلول فاقد گلیف است.

<img src="images/peh_blank.png" />

قرار است با کپی کردن *ب* و تغییر نقطهٔ آن از نقطهٔ تکی به نقطهٔ سه‌تایی حرف *پ* را بسازیم.

روی سلول *ب* (با کد ۱۵۷۶) کلیک کنید. سپس راست‌کلیک کرده و گزینهٔ **copy** را انتخاب کنید. سپس روی سلول *پ* راست‌کلید کرده و گزینهٔ **Paste** را انتخاب کنید. اکنون گلیف *ب* باید در سلول *پ* کپی شده باشد. قدم بعدی تغییر نقطه است.

<img src="images/peh_with_beh.png" />

یک گلیف با سه تا نقطه پیدا کنید. برای مثال *شین* (با کد ۱۵۸۸ یا U+0634). بر روی سلول دابل‌کلیک کنید تا پنل طراحی باز شود. کلید <kbd>V</kbd> را فشار دهید تا ابزار اشاره‌گر انتخاب شود. با فشردن کلید <kbd>Z</kbd> هم می‌توانید پنل را بزرگ کنید تا نمای بهتری داشته باشید.

همهٔ گره‌های سه تا نقطه را با کلید کردن و کشیدن ماوس انتخاب کنید. می‌توانید با کمک کلید <kbd>Shift</kbd> نقطه‌های بیشتر یا کمتری را انتخاب کنید. پس از انتخاب با فشردن کلید ترکیبی <kbd>Alt</kbd> + <kbd>C</kbd> شکل را کپی کنید.
<img src="images/sheen_dots.png" />

حال دوباره به چارت قلم برگردید و روی گلیف *پ* دو بار کلیک کنید که پنل طراحی‌اش باز شود و در کنار پنل طراحی *شین* قرار گیرد.

با هایلایت کردن نقطهٔ زیر گلیف و فشردن کلید <kbd>Delete</kbd> آن نقطه را پاک کنید و سپس با فشردن کلید ترکیبی <kbd>Alt</kbd> + <kbd>V</kbd> سه تا نقطه‌ای که کپی کرده بودید را در آنجا جایگذاری کنید. این نقطه‌ها احتمالاً در جای درستی نخواهند بود چون در حرف *شین* نقطه‌ها بالای حرف قرار دارند. حال باید این را بچرخانیم و وارونه کنیم تا مناسب سه تا نقطهٔ زیر گلیف باشند.

<img src="images/peh_dots1.png" />

وارونه کردن نقطه‌ها: ابزار چرخاندن (دو تا مثلث با یک خط‌چین قرمز بینشان) را از جعبهٔ ابزار انتخاب کنید. (همچنین می‌توانید با راست‌کلیک در وسط نقطه‌ها و انتخاب **Flip the selection** این کار را انجام دهید.) روی یکی از گره‌های نقطه‌ها کلیک کنید و ماوس را اندکی به سمت چپ یا راست بکشید.
<img src="images/peh_dots2.png" />

حرکت دادن نقطه‌های وارونه شده: کلید <kbd>V</kbd> را بفشارید تا ابزار نشانگر دوباره انتخاب شود. روی یکی از گره‌های مربوط به نقطه‌ها کلیک کنید و آن‌ها را به سمت پایین بدنهٔ گلیف بکشید. جوری که مرکز آن بالای نشانگر *ArabicBelow* قرار گیرد.

<img src="images/peh_dots3.png" />

پنل طراحی گلیف را ببندید. اکنون باید بتوانید گلیف جدید *پ* را در چارت قلم ببینید. قلم را ذخیره کنید. (**File > Save**)

<img src="images/peh_new.png" />


## Add the glyphs for the connected forms of *peh*

However, this is only the isolated (standalone) form of the glyph. If you try to use your adapted font, you will find that initial, medial and final forms are not available. These have to be created separately.

>The[se] forms are built as unencoded glyphs (glyphs whose encoding is -1 in FontForge conventions). Th[ey] have no predefined slots." (Khaled Hosny)

Select **Encoding > Add Encoding Slots** and enter the number of the glyphs you want &mdash; in this case, 3. FontForge will add the same number of slots at the very end of the font, and you will be moved there in the font chart. The last three cells (positions 65537, 65538, 65539) have a question mark as a reference glyph, and it is in those cells that you will add the unencoded glyphs by repeating the process above.

<img src="images/peh_slots.png" />

<p class="note">Note that if by mistake you start typing when the font chart still has focus, you get moved to the European section at the top. To get back to the bottom, select <strong>View > Go to</strong>, click the dropdown box and select <strong>Not a Unicode Character</strong>,  and then click <strong>OK</strong>.</p>
### Create the final form

Roll the font chart up a bit until you come to a set of Arabic glyphs at position 65152 (U+FE80) onwards. At U+FE90 (position 65168) you will see a *behfinal* glyph &mdash; click on it and press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy it. Roll down to the third last cell in the chart (position 65537), click on it, and press <kbd>Ctrl</kbd> + <kbd>V</kbd> to paste in the *behfinal* glyph.

<img src="images/beh_forms.png" />

Right-click on the cell and select **Glyph Info**. The naming convention is to use the number of the isolated glyph + a suffix for the form, so change *Glyph Name* to **uni067E.fina**,  and click **OK**. The question mark in the reference cell will change to *peh*.

<img src="images/peh_final.png" />

Get the three dots: double-click on *sheen* (U+FEB5) to load it into the glyph design panel, select the three dots and press <kbd>Ctrl</kbd> + <kbd>C</kbd>.

Double-click on the new *pehfinal* to load it into the glyph design panel, click and drag to highlight the nodes of the dot and press <kbd>Delete</kbd>.

<kbd>Ctrl</kbd> + <kbd>V</kbd> to insert the three dots from *sheen*, flip them, and move them into position below the glyph body. Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save the revised font chart.

### Create the initial and medial forms

Copy the initial form U+FE91 (position 65169) to the penultimate cell (position 65538), delete the single dot and paste in the three dots.

Right-click the cell, select **Glyph Info**, change *Glyph Name* to **uni067E.init**, and click **OK**.

Copy the medial form U+FE92 (position 65170) to the last cell (position 65539), delete the single dot and paste in the three dots.

Right-click the cell, select **Glyph Info**, change *Glyph Name* to **uni067E.medi**, and click **OK**.

<img src="images/peh_forms.png" />

Select **File > Save** to save the revised font chart.


## Add the lookups

The isolated form has to be mapped (linked) to its initial, medial and final forms.

Select **Element > Font Info > Lookups**.

Click on the **+** beside the entry *'init' Initial Forms in Arabic lookup 2*. This will open a submenu of the same name. Click on this submenu.

The *Edit Data* button on the right will now become available &mdash; click it.

<img src="images/peh_lookups1.png" />

In the *Lookup Subtable* panel that pops up, ensure that the *Unicode* button is checked. Roll the list of characters down until you come to the end.

In the box beside *Default Using Suffix*, enter the relevant suffix (in this case, **init**), and then click **Default Using Suffix**.

A new mapping will be added to the list of characters, from uni067E (the isolated form of *peh*) to uni067E.init (the initial form).
Click **OK**.

<img src="images/peh_lookups2.png" />

Do the same for the submenus under the entries *'medi' Medial Forms in Arabic lookup 2* and *'fina' Terminal Forms in Arabic lookup 2*, choosing *medi* and *fina* as the relevant suffix.

Click **OK** again to close the panel, and save the font chart (<kbd>Ctrl</kbd> + <kbd>S</kbd>).

Note that *Default Using Suffix* only seems to work on glyphs in the Unicode 06 (*Arabic*) block &mdash; glyphs in Unicode 07 (*Arabic Supplement*), e.g. *ain* with two dots may have to be added manually by clicking the line marked *New* and typing in the names.

### Generate the adapted font

Select **File > Generate Fonts**.

In the dropdown showing *PS Type 1 (Binary)*, select **TrueType**, and check that the filename reads *GraphNew.ttf*.

Navigate to where you want to save the font, and then click **Generate**. Click **Yes** and **Generate** to the two information messages that come up.

You can then use your normal font installation procedure to install the adapted font. The new glyph *peh* can then be used alongside the existing glyphs in the same nonsense examples as at the beginning of this chapter:

<img src="images/beh_dal_peh.png" />

<p class="note">Note that if you are using a font in LibreOffice and make changes to that font, you need to restart LibreOffice to have it see any changes &mdash; otherwise it will use the previous version of the font, and not the one with the new changes.</p>
Thanks to [Khaled Hosny](http://khaledhosny.org) for his advice on using FontForge to edit Arabic glyphs.

## Further reading

* [This thread on improved Arabic auto-hinting](http://lists.nongnu.org/archive/html/freetype-devel/2015-08/msg00016.html) has a tip about how to draw the overlapping parts of Arabic glyphs.
