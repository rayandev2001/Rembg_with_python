# Remove Background in Python

این کد به صورت مختصر وظیفه حذف پس‌زمینه تصویر و ذخیره‌سازی تصویر خروجی را دارد. حالا به بخش‌های مختلف کد می‌پردازیم

## Installation

```bash
pip install rembg
```

## Usage

```python
import foobar

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```

## Contributing

1. ایمپورت کتابخانه‌ها:
   - `from rembg import remove`: این خط کتابخانه `rembg` را که برای حذف پس‌زمینه تصویر استفاده می‌شود، وارد می‌کند.
   - `from PIL import Image`: این خط کتابخانه `PIL` (Python Imaging Library) را وارد می‌کند که برای کار با تصاویر به کار می‌رود. هرچند در این کد مستقیماً استفاده نشده است.

2. تعریف مسیرهای ورودی و خروجی:
   - `input_path = "rayan.jpg"`: مسیر فایل ورودی (تصویر اصلی) را مشخص می‌کند.
   - `output_path = "output.jpg"`: مسیر فایل خروجی (تصویر با پس‌زمینه حذف شده) را مشخص می‌کند.

3. باز کردن فایل‌های ورودی و خروجی:
   - `with open(input_path , "rb") as i:`: فایل ورودی را در حالت خواندن باینری باز می‌کند.
   - `with open(output_path , "wb") as o:`: فایل خروجی را در حالت نوشتن باینری باز می‌کند.

4. خواندن، پردازش و نوشتن تصویر:
   - `input = i.read()`: محتوای فایل ورودی را به صورت باینری می‌خواند و در متغیر `input` ذخیره می‌کند.
   - `output = remove(input)`: تابع `remove` از کتابخانه `rembg` روی تصویر ورودی اعمال شده و پس‌زمینه تصویر حذف می‌شود. نتیجه در متغیر `output` ذخیره می‌شود.
   - `o.write(output)`: تصویر خروجی (با پس‌زمینه حذف شده) را در فایل خروجی می‌نویسد.
