# آلارم موشن🌟

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>
<img src="https://github.com/jokernets/motion_cv2/blob/main/Alarm%20motion(1).gif" width=600px>
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>


<p align="center">
  <img src="https://img.shields.io/github/last-commit/jokernets/snake-game">
  <img src="https://img.shields.io/github/contributors/jokernets/snake-game">
  <img src="https://img.shields.io/github/issues/jokernets/snake-game">
  <img src="https://img.shields.io/github/stars/jokernets/snake-game">
</p>





## ` ترجمه 🔗`

  
- [English](https://github.com/jokernets/snake-game/blob/main/Translatin/FA.md)






جدول و فهرست مطالب ✅✔
=================

<!--ts-->
   * [نصب و راه اندازی](#%D9%86%D8%B5%D8%A8-%D9%88-%D8%B1%D8%A7%D9%87-%D8%A7%D9%86%D8%AF%D8%A7%D8%B2%DB%8C)
   * [آنالیز کدها📈](#%D8%A2%D9%86%D8%A7%D9%84%DB%8C%D8%B2-%DA%A9%D8%AF-%D9%87%D8%A7-)
     * [پارت 1✔](#%D9%BE%D8%A7%D8%B1%D8%AA-1)
     * [پارت 2✔](#%D9%BE%D8%A7%D8%B1%D8%AA-2)
     * [پارت 3✔](#%D9%BE%D8%A7%D8%B1%D8%AA-3)
     * [پارت 4✔](#%D9%BE%D8%A7%D8%B1%D8%AA-4)

   * [نمایش ویترین💯](
#%D9%86%D9%85%D9%88%D9%86%D9%87-%D9%87%D8%A7%DB%8C-%D8%A8%DB%8C%D8%B4%D8%AA%D8%B1-%D8%A7%D8%B2-%D9%88%DB%8C%D8%AA%D8%B1%DB%8C%D9%86)
 
     * [ویدیو از پروژه📺](
#%D9%88%DB%8C%D8%AF%DB%8C%D9%88-%D8%A7%D8%B2-%D9%BE%D8%B1%D9%88%DA%98%D9%87-)
    
   * [`ارتباط با من 🌐👻`](#%D8%A7%D8%B1%D8%AA%D8%A8%D8%A7%D8%B7-%D8%A8%D8%A7-%D9%85%D9%86-)
<!--te-->



# آلارم موشن 😍

## پروژه هشدار حرکت با استفاده از کتابخانه OpenCV یک پروژه جذاب و کاربردی است که امکان تشخیص حرکت را می دهد. این پروژه به شما امکان می دهد با تشخیص حرکت در تصاویر یا ویدیوها، اعلان ها یا اقدامات را فعال کنید. از جمله کاربردهای آن می توان به نظارت درب، اعلام حریق و یا اطلاع رسانی در مواقع اضطراری اشاره کرد. این پروژه می تواند به شما در بهبود امنیت و کارایی سیستم های خود کمک کند

### `پیشنهاد میکنم تا آخر توضیحات با من همراه باشید ❤`!

#### `استار یادت نره `😉🌟




# نصب و راه اندازی

## کتابخانه را با pip نصب کنید:

```python
pip install `opencv-python`
pip install imutils
pip install threaded

```
نصب موجود را به روز کنید: `pip3 install (کتابخانه شما) -- ارتقاء`
(تا حد امکان به روز رسانی کنید زیرا این کتابخانه در حال توسعه فعال است)


# آنالیز کد ها :



## `پارت 1`:
- "import threading" - ماژول threading را وارد می کند، که به شما امکان می دهد چندین رشته را به طور همزمان اجرا کنید.-
- "import winsound" - ماژول winsound را وارد می کند که به شما امکان می دهد صدا را در سیستم های ویندوز پخش کنید.
- "import cv2" - کتابخانه OpenCV را وارد می کند که برای کارهای بینایی کامپیوتر استفاده می شود.
- "import imutils" - کتابخانه imutils را وارد می کند، که توابع راحتی را برای کار با OpenCV فراهم می کند.
- `cap = cv2.VideoCapture(0, cv2.CAP_DSHOW)` - یک دستگاه فیلمبرداری (وب کم) با شاخص دستگاه 0 را با استفاده از DirectShow API در ویندوز باز می کند.
- `cap.set(cv2.CAP_PROP_FRAME_WIDTH, 640)` - عرض فریم های ویدئویی گرفته شده را روی 640 پیکسل تنظیم می کند.
- `cap.set(cv2.CAP_PROP_FRAME_HEIGHT, 480)` - ارتفاع فریم های ویدیویی گرفته شده را روی 480 پیکسل تنظیم می کند.
- `_, start_frame = cap.read()` - فریمی را از دستگاه ضبط ویدیو می خواند و آن را به متغیر 'start_frame' اختصاص می دهد.
- `start_frame = imutils.resize(start_frame, width=500)` - اندازه تصویر 'start_frame' را با استفاده از کتابخانه imutils به عرض 500 پیکسل تغییر می دهد.
- "start_frame = cv2.cvtColor(start_frame, cv2.COLOR_BGR2GRAY)" - تصویر رنگی "start_frame" را به مقیاس خاکستری تبدیل می کند.
- `strat_frame = cv2.GaussianBlur(start_frame, (21, 21), 0)` - یک فیلتر گاوسی تاری با اندازه هسته (21, -) اعمال می کند.
- به تصویر «start_frame» در مقیاس خاکستری.

```python
import threading
import  winsound
import cv2
import imutils

cap = cv2.VideoCapture(0,cv2.CAP_DSHOW)
cap.set(cv2.CAP_PROP_FRAME_WIDTH,640)
cap.set(cv2.CAP_PROP_FRAME_HEIGHT,480)

_,start_frame = cap.read()
start_frame = imutils.resize(start_frame,width=500)
start_frame = cv2.cvtColor(start_frame,cv2.COLOR_BGR2GRAY)
strat_frame = cv2.GaussianBlur(start_frame,(21,21),0)
```
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>

# Adding Define in project

## `پارت 2`:

- `alarm = False`: متغیر "alarm" را به صورت "False" راه اندازی می کند.
- `alarm_mode = False`: متغیر "alarm_mode" را به صورت "False" راه اندازی می کند.
- `alarm_counter = 0`: متغیر "alarm_counter" را به صورت "0" راه اندازی می کند.
- `def beep_alarm():`: تابعی به نام "beep_alarm" را تعریف می کند.
- `global alarm`: اعلام می کند که متغیر `alarm` در داخل تابع به متغیر جهانی با همین نام اشاره دارد.
- `for _ in range(5):`: حلقه ای را شروع می کند که 5 بار با استفاده از یک زیرخط `_` به عنوان متغیر حلقه اجرا می شود (از آنجایی که در داخل حلقه استفاده نمی شود).
- "اگر نه حالت_زنگ: شکست": بررسی می کند که "حالت_زنگ" "نادرست" است یا خیر، اگر درست باشد از حلقه خارج می شود.
- `winsound.Beep(2500,100)`: تابع "Beep" را از ماژول "winsound" با فرکانس "2500" و مدت زمان "100" برای تولید صدای بوق فراخوانی می کند.
- `alarm = False`: متغیر "alarm" را روی "False" تنظیم می کند.
```python

alarm = False 
alarm_mode = False
alarm_counter = 0 

def beep_alarm():
    global alarm 
    for _ in range(5):
        if not alarm_mode:
            break 
        #print("ALARM")
        winsound.Beep(2500,100)
    alarm = False 
```
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>

## `پارت 3`:
- حلقه "while True:" به طور مداوم اجرا می شود و فریم های دوربین را می گیرد ("cap.read()").

- اندازه فریم گرفته شده به عرض 500 پیکسل با استفاده از "imutils.resize()" تغییر می کند.

- اگر "حالت_زنگ" فعال باشد:
     آ. قاب به مقیاس خاکستری تبدیل شده است (`cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)`).
     ب تاری گاوسی روی قاب خاکستری اعمال می شود.
     ج. تفاوت بین قاب کنونی و «فریم_شروع» محاسبه می‌شود.
     د یک آستانه برای برجسته کردن تغییرات به تفاوت اعمال می شود.
     ه. اگر مجموع مقادیر آستانه از آستانه معینی (در این مورد 1000» تجاوز کند، زنگ هشدار ایجاد می شود.

- اگر شمارنده زنگ از یک آستانه (`20`) فراتر رفت و زنگ هشدار قبلاً فعال نشده باشد، یک رشته جدید برای شروع زنگ ایجاد می شود.

-برنامه به ورودی های کلیدی گوش می دهد. با فشار دادن 't' حالت زنگ هشدار تغییر می کند و با فشار دادن 'q' از برنامه خارج می شوید.

- تابع 'beep_alarm()' (که در کد ارائه شده نشان داده نشده است) احتمالاً مسئول تولید صدای زنگ هشدار است.

```python

while True:
    _,frame = cap.read()
    frame = imutils.resize(frame,width=500)

    if alarm_mode : 
        frame_bw = cv2.cvtColor(frame,cv2.COLOR_BGR2GRAY)
        frame_bw = cv2.GaussianBlur(frame_bw,(5,5),0)
        diffrence = cv2.absdiff(frame_bw,start_frame)
        threshold = cv2.threshold(diffrence,25,255,cv2.THRESH_BINARY)[1]
        start_frame = frame_bw 
        
        if threshold.sum()> 1000 :
            print(threshold.sum())
            alarm_counter += 1 
            
        else : 
            if alarm_counter > 0 : 
                alarm_counter -= 1 
        cv2.imshow("Cam",threshold)
    else: 
        cv2.imshow("Cam",frame)
            
    if alarm_counter > 20 :
        if not alarm : 
            alarm = True 
            threading.Thread(target=beep_alarm).start()  
    key_pressed = cv2.waitKey(30)
    if key_pressed == ord("t"):
        alarm_mode = not alarm_mode 
        alarm_counter = 0
    if key_pressed == ord("q"):
        alarm_mode = False 
        break    
```

## `پارت 4`:
در اینجا یک تفکیک کد خط به خط است:

- `cap.release()`: این خط شیء ضبط ویدیوی 'cap' را آزاد می کند، که برای فیلم برداری از یک دوربین یا فایل ویدیویی استفاده می شود. رها کردن شی capture برای آزاد کردن منابع سیستم مهم است.
- `cv2.destroyAllWindows()`: این خط تمام پنجره های OpenCV را که در حال حاضر باز هستند می بندد. این برای تمیز کردن پنجره‌هایی که ممکن است در حین پردازش تصویر یا ویدیو باز شده باشند مفید است.

```python
cap.release()
cv2.destroyAllWindows()
```

<img src="https://github.com/jokernets/motion_cv2/blob/main/Cam%202024-04-18%2022_17_44.png" width="300" height="300">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>





## نمونه های بیشتر از ویترین🎄👑

### ویدیو از پروژه 📺





# `ارتباط با من `🌐👻

<a herf="https://www.buymeacoffee.com/jokernets"><img src="https://cdn.buymeacoffee.com/buttons/v2/arial-yellow.png" alt="Buy Me A Coffee" width="180px">
<a href="mailto:joker.until33@gmail.com"><img align="center" width="60px" src="https://github.com/edent/SuperTinyIcons/raw/master/images/svg/gmail.svg" style="max-width: 100%;"></a><a href="https://www.linkedin.com/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/in/imfallah/" height="40" width="60" /></a>
