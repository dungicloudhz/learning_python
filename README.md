# Lộ Trình Học Python Từ Cơ Bản Tới Nâng Cao

Mình sẽ lên cho bạn **lộ trình học Python từ cơ bản tới nâng cao** theo từng giai đoạn, có thứ tự rõ ràng, kèm mục tiêu và nội dung cho từng bước.  
Bạn có thể áp dụng lộ trình này dù học để làm **web, data, AI, automation hay backend**.

---

## **Giai đoạn 1 – Python Cơ bản (0 → 1 tháng)**

**Mục tiêu:** Nắm cú pháp, kiểu dữ liệu, cấu trúc điều khiển.

#### 1. **Cài đặt và môi trường làm việc**

   - Cài Python & pip
   - IDE: PyCharm, VSCode hoặc Jupyter Notebook
   - Chạy file `.py` và dùng Python REPL

#### 2. **Cú pháp & biến**
   - Biến, hằng số, quy tắc đặt tên
     - Hằng số: Python không có **const**, nhưng quy ước viết hoa.
       ```python
         age = 25 # biến
         NAME = "Alice" # hằng số (quy ước)
       ```
     - Quy tắc đặt tên
       - Chữ thường, **\_** phân cách (**snake_case**)
       - Không bắt đầu bằng hằng số
       - Không dùng từ khóa Python (**if**, **for**...)
   - Input/Output (`print()`, `input()`)
     ```python
        name = intput("Nhập tên của bạn: ")
        print("Xin chào", name)
     ```
#### 3. **Kiểu dữ liệu cơ bản**
   - `int`, `float`, `str`, `bool`
   - Ép kiểu (`int()`, `str()`…)
     ```python
     x = int("10") # chuỗi -> số nguyên
     y = float("3.14") # chuỗi -> số thực
     s = str(100) # số -> chuỗi
     ```
#### 4. **Toán tử**
   - Số học
   ```python
      a,b = 5, 2
      print(a + b)  # 7
      print(a - b)  # 3
      print(a * b)  # 10
      print(a / b)  # 2.5
      print(a // b) # 2 (chia lấy số nguyên)
      print(a % b) # 1 (chia lấy số dư)
      print(a ** b) #  25 (Lũy thừa)
   ```
   - So sánh, logic (`and`, `or`, `not`)
   ```python
      print(a > b)   # True
      print(a == b)  # False
      print(a != b)  # True
      print(a > 0 and b > 0)  # True
      print(a > 0 or b < 0)   # True
      print(not (a > b)) # False
   ```
   - Toán tử gán và toán tử đặc biệt (`+=`, `//`, `%`)
   ```python
      x = 10
      x += 5 # 15
      x //= 3 # 5
      x %= 2 # 1
   ```
#### 5. **Cấu trúc điều khiển**
   - `if`, `elif`, `else`
   ```python
      n = 7
      if n > 10:
         print("Lớn hơn 10")
      elif n == 10:
         print("Bằng 10")
      else:
         print("Nhỏ hơn 10")
   ```
   - Vòng lặp `for`, `while`
   ```python
      # for
      for i in range(5):
         print(i) # 0,1,2,3,4
      # while
      count = 0
      while count < 3:
            print("Lặp", count)
            count += 1
   ```
   - `break`, `continue`, `pass`
   ```python
      for i in range(5):
      if i == 2:
         continue  # bỏ qua 2
      if i == 4:
         break     # dừng vòng lặp
      print(i)
   ```

#### 6. **Collections**
   - `list`, `tuple`, `set`, `dict`
   - Các method thường dùng (`append`, `remove`, `keys`, `values`…)
   ##### 6.1 List (mutable, có thứ tự, cho phép trùng lặp)
   
   | Method | Mô tả |
   |--------|-------|
   |`append(x)`|Thêm phần tử `x` vào cuối list|
   |`extend(iterable)`|Thêm nhiều phần tử từ một iterable (list, touple, set,...)|
   |`insert(i, x)`|Chèn `x` vào vị trí `i`|
   |`remove(x)`|Xóa phần tử đầu tiên có giá trị `x`|
   |`pop([i])`|Xóa và trả về phần tử tại vị trí `i` (mặc định cuối list)|
   |`clear()`|Xóa toàn bộ phần tử|
   |`index(x, start, end)`|Trả về vị trí đầu tiên tìm thấy `x`|
   |`count(x)`|Đếm số lần xuất hiện của `x`|
   |`sort(reverse=False, key=None)`|Sắp xếp list|
   |`reverse()`|Đảo ngược list|
   |`copy()`|Sao chép nông (shallow copy)|

      ```python
         fruits = ["apple", "banana"]
         fruits.append("orange") # thêm
         fruits.remove("orange") # xóa
         print(fruits[0]) # apple
      ```
   ##### 6.2 Tuple (immutable, có thứ tự, cho phép trùng lặp)

   | Method | Mô tả |
   |--------|-------|
   |`count(x)`|Đếm số lần xuất hiện của `x`|
   |`index(x, start, end)`|Trả về vị trí đầu tiên tìm thấy `x`|
   > Không có method thêm, xóa , sửa. Nếu muốn thay đổi phải tạo tuple mới 
   ```python
      point = (1, 2)
      print(point[0])
   ```

   ##### 6.3 Set (Mutable, không thứ tự, không trùng lặp)

   | Method | Mô tả |
   |--------|-------|
   |`add(x)`|Thêm phần tử `x`|
   |`update(iterable)`|Thêm nhiều phần tử|
   |`remove(x)`|Xóa `x`, báo lỗi nếu không tồn tại|
   |`discard(x)`|Xóa `x` nếu tồn tại, không báo lỗi|
   |`pop()`|Xóa và trả về phần tử ngẫu nhiên|
   |`clear()`|Xóa tất cả phần tử|
   |`union(orther_set)`| Hợp nhất 2 set |
   |`intersection(orther_set)`|Lấy điểm giao giữa 2 set|
   |`difference(orther_set)`|Hiệu|
   |`symmetric_difference(orther_set)`|Hiệu đối xứng|
   |`issubset(orther)`|Kiểm tra tập con|
   |`issuperset(orther)`|Kiểm tra tập cha|
   |`isdisjoint(orther)`|Kiểm tra không có phần tử chung|
   |`copy()`|Sao chép|

   ```python
      nums = {1, 2, 2, 3}
      print(nums) # {1, 2, 3}
      nums.add(4)
      nums.discard(2)
   ```
##### 6.4 Dict (Mutable, không thứ tự*, key duy nhất)
> \* Từ python 3.7 trở lên, dict giữ thứ tự chèn.

| Method | Mô tả |
|--------|-------|
|`get(key, default)`|Lấy giá trị của key (trả về `default` nếu không tồn tại)|
|`keys()`|Lấy danh sách key|
|`values()`|Lấy danh sách value|
|`items()`|Lấy danh sách (key, value)|
|`update(orther_dict)`|Thêm/ cập nhật key-value|
|`pop(key, default)`|Xóa key và trả về value|
|`popitem()`|Xóa và trả về một cặp (key, value) ngẫu nhiên|
|`setdefault(key, default)`|Lấy value của key, nếu tồn tại thì thêm key với `default`|
|`clear()`|Xóa toàn bộ phần tử|
|`copy()`|Sao chép|

```python
   person = {"name": "Alice", "age": 25}
   print(person["name"])
   person["age"] = 26
   print(person.keys())
   print(person.values())
```
##### 6.5 Tóm tắt nhanh

| Kiểu | Có thứ tự | Cho phép trùng lặp | Mutable | Thêm/Xóa/Sửa được |
|------|-----------|-------------------|---------|-------------------|
| list | ✅ | ✅ | ✅ | ✅ |
| tuple | ✅ | ✅ | ❌ | ❌ |
| set | ❌ | ❌ | ✅ | ✅ |
| dict | ❌ *(Python 3.7+ giữ thứ tự chèn)* | ❌ (key) | ✅ | ✅ |
#### 7. **Hàm (function)**
   ##### 7.1 Định nghĩa và gọi hàm (`def`)
   - Hàm giúp nhóm các đoạn code có chức năng giống nhau vào một khối để tái sử dụng
   - Cú pháp:
   ```python
      def xin_chao():
         print("Xin chào Python!")
      # Gọi hàm
      xin_chao()
   ```
   ##### 7.2 Tham số (Parameters) và Đối số (Arguments)

   | Loại tham số | Mô tả |Ví dụ|
   |--------------|-------|-----|
   |**Positional arguments**|Truyền theo thứ tự định nghĩa|`tong(5,3)`|
   |**Key word arguments**|Truyền theo tên tham số|`tong(a=5,b=3)`|
   |**Default arguments**|Giá trị mặc định nếu không truyền|`def chao(ten="bạn"):`|
   |**Variable-length `(*args)`**|Nhận nhiều giá trị không giới hạn (tuple)|`def tong(*args):`|
   |**Variable-length keyword `(**kwwargs)`**|Nhận nhiều cặp key-value (dict)|`def in_thong_tin(**kwargs)`|

   ```python
      def tong(a, b):
         return a + b
      print(tong(5, 3))          # Positional
      print(tong(b=3, a=5))      # Keyword

      def chao(ten="bạn"):
         print(f"Xin chào {ten}!")

      chao("Dung")   # Xin chào Dung!
      chao()         # Xin chào bạn!
   ```

   ##### 7.2 `return` trong hàm
   - `return` dùng để trả về kết quả từ hàm cho nơi gọi.
   - Nếu không có `return`, hàm sẽ trả về `None` mặc định.
   ```python
      def binh_phuong(x):
         return x * x
      ket_qua = binh_phuong(5)
      print(ket_qua)  # 25
   ```
   ##### 7.2 Tổng hợp ví dụ

   ```python
      def thong_tin_hoc_vien(ten, tuoi=18, *mon_hoc, **thong_tin_khac):
         print(f"Tên: {ten}")
         print(f"Tuổi: {tuoi}")
         if mon_hoc:
            print("Môn học:", mon_hoc)
         if thong_tin_khac:
            print("Thông tin khác:", thong_tin_khac)
      thong_tin_hoc_vien("Dung", 25, "Python", "Java", que="Hà Nội", so_thich="Lập trình")

      # Kết quả
      # Tên: Dung
      # Tuổi: 25
      # Môn học: ('Python', 'Java')
      # Thông tin khác: {'que': 'Hà Nội', 'so_thich': 'Lập trình'}
   ```

---

## **Giai đoạn 2 – Python Nâng cao nền tảng (1 → 2 tháng)**

**Mục tiêu:** Viết code gọn, quản lý tốt dữ liệu và module.

### 1. **String nâng cao**
   - F-string, `format()`, `join()`, slicing
##### 1.1 F-string (Python 3.6+)
   - Cách viết nhanh khi chèn biến vòa chuỗi:
   ```python
      name = "Alice"
      age = 25
      print(f"Tôi là {name}, {age} tuổi")
      print(f"Năm sau tôi {age + 1} tuổi")
   ```
##### 1.2 `format()`
   ```python
      print("Tôi là {}, {} tuổi".format(name, age))
      print("Tôi là {0}, {1} tuổi".format(name, age))
      print("Tôi là {ten}, {tuoi} tuổi".format(ten=name, tuoi=age))
   ```
##### 1.3 `join()`   
   ```python
      words = ["Python", "is", "fun"]
      sentence = " ".join(words)
      print(sentence)  # Python is fun
   ```
##### 1.4 Slicing
   - `sequence[start:stop:step]`
   ```python
      s = "Python"
      print(s[0:3])   # Pyt
      print(s[-3:])   # hon
      print(s[::-1])  # nohtyP (đảo ngược)
   ```   

### 2. **List comprehension & Generator**

##### 2.1 Cách viết ngắn gọn
   - Viết ngắn gọn thay vì dùng vòng lặp
   - **List comprehension** là cách viết ngắn gọn để tạo list mới từ một iterable (list, tuple, set, range, ...).
   - Ưu điểm:
      - Cú pháp ngắn gọn hơn vòng lặp `for`.
      - Thường nhanh hơn vòng lặp thủ công khi tạo list.
   ```python
      # [biểu_thức for biến in iterable if điều_kiện]
      nums = [x for x in range(10) if x % 2 == 0]
      print(nums)  # [0, 2, 4, 6, 8]
   ```

##### 2.2 Generator (`yield`)
   - __Generator__ tạo dữ liệu theo yêu cầu (không tốn nhiều RAM)
   - **Generator** là hàm đặc biệt trong Python, dùng để sinh ra giá trị từng bước (lazy evaluation).
   - Thay vì `return`, generator dùng **`yield`** để trả về từng giá trị một.
   - Ưu điểm:
      - Tiết kiệm bộ nhớ (không lưu toàn bộ dữ liệu cùng lúc).
      - Có thể sinh dữ liệu vô hạn.
      - Thích hợp để xử lý dữ liệu lớn.
   ```python
      def countdown(n):
         while n > 0:
            yield n
            n -= 1
      for num in countdown(5):
         print(num)
   ```

##### 2.3 Generator expressions
   - **Generator expression** là cú pháp rút gọn để tạo **generator** mà không cần định nghĩa hàm với `yield`.
   - Giống **list comprehension**, nhưng:
      - **List comprehension** → Tạo list, lưu toàn bộ dữ liệu trong bộ nhớ.
      - **Generator expression** → Tạo generator, sinh giá trị từng bước (tiết kiệm bộ nhớ).
   ```python
      ## (expr for var in iterable if điều_kiện)
      gen = (x * x for x in range(5))
      for val in gen:
         print(val)
   ```

### 3. **Làm việc với file**
#### Tổng quan nhanh
   - Dùng hàm __`open(path, mode, encoding=...)`__ để mở file.   
   - Luôn ưu tiên dùng **context manager** (`with open(...) as f:`) để tự động đóng file.
   - Các mode phổ biến:
      - `'r'`: đọc (text)
      - `'w'`: ghi (viết đè)
      - `'a'`: ghi (thêm vào cuối)
      - `'x'`: tạo và ghi, lỗi nếu tồn tại
      - Thêm `'b'` để thao tác binary (`'rb'`, `'wb'`) và `'t'` để text (mặc định).
   - `encoding='utf-8'` thường được dùng cho text hiện đại; chú ý BOM/endcoding khác.
##### 3.1 Đọc file text
   ```python
      # đọc toàn bộ file thành 1 chuỗi
      with open("example.txt", "r", encoding="utf-8") as f:
         text = f.read()      

      # Đọc theo dòng / theo iterator (khuyên dùng cho file lớn)
      with open("example.txt", "r", encoding="utf-8") as f:
         for line in f:              # hiệu quả, không load toàn bộ file vào RAM
            print(line.rstrip("\n"))
   ```
   - Một số method hay dùng
      - **`f.read(size)`** -- Đọc tối đa **size** ký tự/byte.
      -  **`f.readline()`** -- Đọc 1 dòng (bao gồm **\n** ở cuối, nếu có).
      -  **`f.readlines()`** -- Trả về list các dòng (tránh dùng với file lớn). 
      -  **`for line in f:`** -- Đọc dòng theo iterator (phổ biến & memory-safe) 
   - Đọc file lớn theo block (chunks)   
   ```python
      def read_in_chunks(file_path, chunk_size=1024*1024):
         with open(file_path, "r", encoding="utf-8") as f:
            while True:
                  chunk = f.read(chunk_size)
                  if not chunk:
                     break
                  yield chunk

      for part in read_in_chunks("big.txt"):
         process(part)
   ```
##### 3.2 Ghi file text
   - Ghi đơn giản
   ```python
      with open("out.txt", "w", encoding="utf-8") as f:
      f.write("Hello\n")
      f.writelines(["line1\n", "line2\n"])
   ```
   - Thêm vào cuối file `(append)`
   ```python
      with open("out.txt", "a", encoding="utf-8") as f:
         f.write("Thêm dòng mới\n")
   ```
   - **Lưu ý**
      - Nếu dùng `csv.writer` để ghi file CSV trên Windows, **mở file với** `newline=''` (Xem phần CSV)
      - Nếu cần chắc chắn dữ liệu đã ghi xuống đĩa: `f.flush()` + `os.fsync(f.fileno())` (thường dùng cho critial data)
##### 3.3 Làm việc với file binary (ảnh, pdf...)
   - Đọc/ Ghi binary
   ```python
      # Copy file binary
      with open("source.jpg", "rb") as src, open("dest.jpg", "wb") as dst:
         while True:
            chunk = src.read(1024*64)
            if not chunk:
                  break
            dst.write(chunk)
   ```
##### 3.4 CSV (module `csv`)
   - Đọc CSV (list rows)
   ``` python
      import csv

      with open("data.csv", "r", encoding="utf-8", newline="") as f:
         reader = csv.reader(f, delimiter=",", quotechar='"')
         for row in reader:
            # row là list: ['col1', 'col2', ...]
            print(row)
   ```
   - Ghi CSV (list rows)
   ``` python
      import csv

      rows = [
         ["name", "age"],
         ["Alice", "30"],
         ["Bob", "25"]
      ]
      with open("out.csv", "w", encoding="utf-8", newline="") as f:
         writer = csv.writer(f, delimiter=",", quotechar='"', quoting=csv.QUOTE_MINIMAL)
         writer.writerows(rows)
   ```
   - **Chú ý**: Luôn dùng `newLine=""` khi mở file để tránh ra dòng trống (blank lines)  trên Windows.
##### 3.5 DictReader / DictWriter (dễ dùng khi có header)
   ```python
      import csv

      # Đọc
      with open("people.csv", "r", encoding="utf-8", newline="") as f:
         reader = csv.DictReader(f)
         for row in reader:
            # row là dict: {'name': 'Alice', 'age': '30'}
            print(row["name"], row["age"])
      # Ghi
      fieldnames = ["name", "age"]
      with open("out.csv", "w", encoding="utf-8", newline="") as f:
         writer = csv.DictWriter(f, fieldnames=fieldnames)
         writer.writeheader()
         writer.writerow({"name": "Charlie", "age": 22})
   ```
   - Tùy chọn quan trọng:
      - **delimiter**: ký tự phân cách
      - **quotechar**: ký tự dùng dể quote
      - **quoting**: `csv.QUOTE_MINIMAL`, `QUOTE_ALL`, `QUOTE_NONNUMERIC`, `QUOTE_NONE`
      - **escapechar**: ký tự escape khi cần
##### 3.6 JSON (module `json`)
   - Ghi object Python vào file JSON
   ```python
      import json

      data = {"name": "Dung", "age": 30, "skills": ["python", "sql"]}

      with open("data.json", "w", encoding="utf-8") as f:
         json.dump(data, f, ensure_ascii=False, indent=2)
   ```
   > `ensure_ascii=False` để giữ ký tự Unicode (ví dụ tiếng Việt) thay vì escape \u....
   > `indent=2` để format đẹp (human-readable).
   - Đọc JSON từ file
   ```python
   import json

   with open("data.json", "r", encoding="utf-8") as f:
      data = json.load(f)  # trả về dict/list tương ứng
   ```
   - Khi object không thể serialize trực tiếp (ví dụ `datetime`)
   ```python
      import json
      from datetime import datetime

      def default(o):
         if isinstance(o, datetime):
            return o.isoformat()
         raise TypeError

      obj = {"time": datetime.now()}

      with open("t.json", "w", encoding="utf-8") as f:
         json.dump(obj, f, default=default)
   ```

##### 3.7 Path và thao tác với đường dẫn
   - Sử dụng `os.path`
   ```python
   import os

   # Lấy đường dẫn thư mục hiện tại
   current_dir = os.getcwd()
   print("Thư mục hiện tại:", current_dir)
   # Nối đường dẫn (dễ hơn là tự ghép bằng '/')
   file_path = os.path.join(current_dir, "data.txt")
   print("Đường dẫn file:", file_path)
   # Kiểm tra file/folder có tồn tại không
   print("Tồn tại?", os.path.exists(file_path))
   # Lấy tên file và thư mục
   print("Tên file:", os.path.basename(file_path))
   print("Thư mục chứa file:", os.path.dirname(file_path))
   ```
   > **Ưu điểm**: tương thích với nhiều phiên bản Python cũ.
   - Sử dụng `pathlib` (Cách hiện đại hơn)
   ```python
   from pathlib import Path

   # Lấy thư mục hiện tại
   current_dir = Path.cwd()
   print("Thư mục hiện tại:", current_dir)
   # Tạo đường dẫn file
   file_path = current_dir / "data.txt"
   print("Đường dẫn file:", file_path)
   # Kiểm tra tồn tại
   print("Tồn tại?", file_path.exists())
   # Lấy tên file và thư mục
   print("Tên file:", file_path.name)
   print("Thư mục chứa file:", file_path.parent)
   ```
   > **Ưu điểm**: cú pháp gọn, dễ đọc, hoạt động trên mọi hệ điều hành.

### 4. **Module & Package**
#### 4.1 Import Module
   - Python có nhiều **module** (thư viện) tích hợp sẵn
   Ví dụ: `math`, `datetime`, `os`, `random`, ...
   ```python
      import math

      print(math.sqrt(16))  # 4.0
      print(math.pi)        # 3.141592653589793
   ```
   - Bạn cũng có thể **import 1 phần** của module:
   ```python
      from math import sqrt, pi
      print(sqrt(25))  # 5.0
      print(pi)        # 3.141592653589793
   ```
#### 4.1 Import Module
   > Tự tạo module
   - Giả sử bạn tạo file `my_path.py`:
   ```python
      def add(a, b):
         return a + b
      def sub(a, b):
         return a - b
   ```
   - Sau đó tạo file `main.py`:
   ```python
      import my_math

      print(my_math.add(5, 3))  # 8
      print(my_math.sub(10, 4)) # 6
   ```
   ✅ Mỗi file `.py` là 1 **module**.
   > Cài và dùng thư viện ngoài (`pip install`)
   - Ví dụ: cài thư viện **request**
      ```bash
         pip install requests
      ```
   - Dùng:
      ```python
         import requests

         response = requests.get("https://api.github.com")
         print(response.status_code)
         print(response.json())
      ```
### 5. **Ngoại lệ (Exception)**

#### 5.1 `try`, `except`, `finally`
   ```python
      try:
         num = int(input("Nhập số: "))
         print(10/ num)
      except ValueError:
         print("Vui lòng nhập số tài nguyên!")
      except ZeroDivisionError:
         print("Không thể chia cho 0!")
      finally:
         print("Luôn chạy dù có lỗi hay không")
   ```
#### 5.2 Tự định nghĩa exception
   ```python
      class MyError(Exception):
         pass
   
      def check_age(age):
         if age < 18: raise MyError("Tuổi phải lớn hơn 18")
         return "OKE"
      
      try:
         print(check_age(5))
      except MyError as e:
         print("Lỗi: ", e)
   ```

### 6. **OOP trong Python**
#### 6.1 `class`, `__init`
   - **Class** là khuôn mẫu (blueprint) để tạo **object** (instance).
   - **\_\_init__** là **hàm khởi tạo** được gọi ngay khi tạo instance, dùng để gán thuộc tính ban đầu.
   ```python
      class Person:
         def __init__(self, name, age):
            self.name = name
            self.age = age
         
         def say_hello(self):
            print(f"Xin chào, tôi là {self.name}")

      p = Person("DUNG", 23)
      p.say_hello()
   ```
   > Chú ý:
   > - **self** tham chiếu chính tời instance (tên **self** là quy ước, không bắt buộc nhưng nên dùng).
   > - **\_\_init__** không phải trả về instance(không cần **return**).
#### 6.2 Thuộc tính (attributes) & phương thức (methods)
##### 6.2.1 Instance attribute vs Class attribute
   - **Instance attribute**: thuộc tính riêng cho mỗi instance (**`self.x`**)
   - **Class attribute**: thuộc tính chia sẻ giữa toàn bộ class (khai báo ở ngoài **\_\_init__**)
   ```python
      class Cat:
         species = "Felis catus" # class attribute
         def __init__(self, name):
            self.name = name # instance attribute
      
      c1 = Cat("Miu")
      c2 = Cat("Mèo")
      print(Cat.species)  # Felis catus
      print(c1.species)   # Felis catus
   ```
##### 6.2.2 Các loại phương thức
   - **Instance method**: nhận `self`.
   - **Class method**: dùng `@classmethod` và nhận `cls` (tham chiếu tới class)
   - **Static method**: dùng `@staticmethod`, không nhận `self`/`cls`.
   ```python
      class Demo:
         counter = 0

         def __init__(self):
            Demo.counter += 1

         @classmethod
         def how_many(cls):
            return cls.counter
         @staticmethod
         def hello():
            return "Hello"

      d = Demo()
      print(Demo.how_many()) # 1
      print(Demo.hello()) # Hello
   ```
##### 6.2.3 Property - đóng gói getter/setter
   > Dùng `@property` để biến method thành thuộc tính có thể đọc/ghi an toàn.
   ```python
      class Rectangle:
         def __init__(self, w, h):
            self._w = w
            self._h = h

         @property
         def area(self):
            return self._w * self._h
         
         @property
         def width(self):
            return self._w

         @width.setter
         def width(self, value)
            if value <= 0:
               raise ValueError("Width must be > 0")
            self._w = value
      
      r = Rectangle(3, 4)
      print(r.area)    # 12
      r.width = 5
      print(r.area)    # 20
   ```
##### 6.2.4 Quy ước "private" / name mangling
   - `_attr` -- Quy ước protected (không bắt buộc), vẫn truy cập được.
   - `__attr` -- name mangling (`_ClassName_attr`) để hạn chế truy cập trực tiếp
   ```python
      class A:
         def __init__(self):
            self._x = 1
            self.__y = 2 # sẽ biến thành _A__y
   ```
##### 6.2.5 Kế thừa
   - Kế thừa cho phép class con dùng/ghi đè hành vi class cha.
   - Dùng `supper()` để gọi hàm class cha.
   ```python
      class Animal:
         def __init__(self, name):
            self.name = name
         def speak(self):
            raise NotImplementedError

      class Dog(Animal):
         def __init(self, name, breed):
            supper().__init__(name)
            self.breed = breed

         def speak(self):
            return "Woof!"
      dog = Dog("Buddy", "Beagle")
      print(dog.name, dog.breed, dog.speak()) # Buddy Beagle Woof!
   ```
##### 6.2.5 Multiple inheritance & MRO
   > Python cho phép kế thừa nhiều lớp, nhưng cần hiểu **MRO (method resolution order)** để tránh tranh chấp.
   ```python
      class A: ...
      class B(A): ...
      class C(A): ...
      class D(B, C): ...
      # D.__mro__ or D.mro() cho biết thứ tự tìm phương thức
   ```
##### 6.2.6 Đa hình
   - **Đa hình**: các object khác nhau có thể gọi cùng một method nhưng triển khai khác nhau.
   - Python khuyến khích **duck typing**: "nếu nó đi như vịt và kê như vịt thì coi là vịt" -- không cần kế thừa.
   > Ví dụ (overriding):
   ```python
      class Cat(Animal):
         def speak(self):
            return "Meow"

      animals = [Dog("A", "X"), Cat("B")]
      for a in animals:
         print(a.speak())  # Woof!, Meow
   ```
   > Ví dụ (duck typing):
   ```python
      class Airplane:
         def fly(self):
            print("plane flies")

      class Bird:
         def fly(self):
            print("bird flies")

      def let_it_fly(obj):
         obj.fly()  # chỉ cần obj có method fly()

      let_it_fly(Airplane()); let_it_fly(Bird())
   ```
###### 6.2.6.1 Absstract Base Class (tùy chọn)
   > Dùng `abc` để yêu cầu class con triển khai method nhất định.
   ```python
      from abc import ABC, abstractmethod

      class Shape(ABC):
         @abstractmethod
         def area(self):
            pass

      class Circle(Shape):
         def __init__(self, r):
            self.r = r
         def area(self):
            return 3.14 * self.r * self.r
   ```
##### 6.3 Magic methods 
   > (`__str__`, `__repr__`, `__len__`…)
   - Magic methods (hay dunder methods -- double underscore) là những hàm đặc biệt trong Python, **tên bắt đầu và kết thức bằng 2 dấu gạch dưới `__`**.
   - Chúng giúp định nghĩa **hành vi đặc biệt** cho đối tượng, ví dụ:
      - Cách khởi tạo (`__init__`)
      - Cách int ra (`__str__`)
      - Cách so sánh (`__eq__`)
      - Cách cộng/ trừ (`__add__`, `__sub__`)
      - Và nhiều cái khác
   > Ví dụ các magic method phổ biến
   ```python
      class Persion:
         def __init_(self, name, age):
            # Hàm khởi tạo (constructor) 
            self.name = name
            self.age = age

         def __str__(self):
            # In ra chuỗi dễ đọc (dành cho người dùng)

         def __repr__(self):
            # In ra chuỗi dành cho lập trình viên (debug)
            return f"Person('{self.name}', '{self.age})"

         def __len__(self):
            # Trả về độ dài (ví dụ: tuổi)

         def __eq__(self, orther):
            # So sánh == giữa 2 Person dựa vào name và age
            return self.name == orther.name and self.age == orther.age

      # Tạo mới đối tượng
      p1 = Person("Alice", 30)
      p2 = Person("Alice", 30)
      p3 = Person("Bob", 25)
      # __str__ và __repr__
      print(p1)        # Person(name=Alice, age=30)  -> dùng __str__
      print(repr(p1))  # Person('Alice', 30)         -> dùng __repr__
      # __len__
      print(len(p1))   # 30

      # __eq__
      print(p1 == p2)  # True
      print(p1 == p3)  # False
   ```
   > Một số magic methods thông dụng

   | Magic method  | Ý nghĩa                          | Ví dụ                 |
   | ------------- | -------------------------------- | --------------------- |
   | `__init__`    | Khởi tạo đối tượng               | `p = Person("A", 20)` |
   | `__str__`     | Chuỗi hiển thị cho người dùng    | `print(obj)`          |
   | `__repr__`    | Chuỗi cho lập trình viên (debug) | `repr(obj)`           |
   | `__len__`     | Độ dài đối tượng                 | `len(obj)`            |
   | `__eq__`      | So sánh bằng `==`                | `obj1 == obj2`        |
   | `__add__`     | Toán tử cộng `+`                 | `obj1 + obj2`         |
   | `__getitem__` | Lấy phần tử bằng `[]`            | `obj[key]`            |
   | `__setitem__` | Gán phần tử bằng `[]`            | `obj[key] = value`    |
---

## **Giai đoạn 3 – Python Chuyên sâu (2 → 4 tháng)**

**Mục tiêu:** Nắm vững công cụ, thuật toán, áp dụng vào dự án.

### 1. **Lập trình hàm (Functional Programming)**
#### 1.1 Functional Programming là gì?
   - **Functional Programming (FP)** là phong cách lập trỉnh mà **hàm** là trung tâm.
   - Tránh thay đổi dữ liệu gốc, ưu tiên dùng **hàm thuần (pure functions)**
   - Sử dụng **hàm bậc cao (higher-order functions)** -- hàm nhận hàm khác làm tham số hoặc trả về hàm.
   > Ví dụ ý tưởng
   ```python
      # Imperative style (cách lập trình bình thường)
      numbers = [1, 2, 3, 4]
      squares = []
      for n in numbers:
         squares.append(n ** 2)

      # Functional style
      numbers = [1, 2, 3, 4]
      squares = list(map(lambda x: x**2, numbers))
   ```
#### 1.2 Lambda function
   - **Hàm vô danh** (không cần `def`), thường dùng khi hàm ngắn gọn.
   ```python
      add = lambda a, b: a + b
      print(add(3, 4)) #7
   ```
#### 1.3 `map()`, `filter()`, `reduce()`
##### 1.3.1 `map(func, iterable)`
   - Áp dụng một hàm lên từng phần tử
   ```python
      nums = [1, 2, 3, 4]
      squares = list(map(lambda x: x**2, nums))
      print(squares)  # [1, 4, 9, 16]
   ```
##### 1.3.2 `filter(func, iterable)`
   - Lọc phần tử theo điều kiện (hàm trả về True/False)
   ```python
      nums = [1, 2, 3, 4, 5]
      evens = list(filter(lambda x: x % 2 == 0, nums))
      print(evens)  # [2, 4]
   ```
##### 1.3.2 `reduce(func, iterable)` **Cần import**
   - Gộp dần các phần tử thành một giá trị duy nhất
   ```python
      from functools import reduce
      nums = [1, 2, 3, 4]
      product = reduce(lambda a, b: a* b, nums)
      print(product) # 24
   ```
#### 1.4 List Comprehension (Functional Style)
   - Viết gọn thay vì vòng lặp
   ```python
      nums = [1, 2, 3, 4]
      squares = [x**2 for x in nums]
      print(squares)  # [1, 4, 9, 16]
      # Kết hợp điều kiện
      evens = [x for x in nums if x % 2 == 0]
      print(evens)  # [2, 4]
   ```
#### 1.5 Generator Expression
   - Tương tự list comprehension nhưng tạo **generator** (tiết kiệm bộ nhớ).
   ```python
      gen = (x**2 for x in range(5))
      for val in gen:
         print(val)
   ```
#### 1.6 Hàm bậc cao (Higher-order functions)
   - Hàm có thể nhận hoặc trả về hàm khác:
   ```python
      def make_multiplier(factor):
         def multiplier(x):
            return x * factor
         return multiplier
      
      double = maker_multiplier(2)
      print(double(5)) # 10
   ```
#### 1.7 Pure function & bất biến
   - Hàm thuần **không thay đổi dữ liệu gốc**.
   ```python
      # Không pure function
      nums = [1, 2, 3]
      def add_one(lst):
         for in in range(len(lst)):
            lst[i] += 1
      add_one(nums)      
      print(nums) # [2, 3, 4] (bị thay đổi)

      # Pure function
      nums = [1, 2, 3]
      def add_one(lst):
         return [x + 1 for x in lst]
      print(add_one(nums))  # [2, 3, 4]
      print(nums)           # [1, 2, 3] (nguyên bản)
   ```


### 2. **Decorators & Context Manager**
#### 2.1 Decorators(`@decorator`)
   - **Dùng để bọc hàm** → thêm chức năng mà không sửa code gốc.
   - Cú pháp: `@tên_decorator` đặt tên hàm.
   ```python
      def log(func):
         def wrapper(*args, **kwargs):
            print(f"Gọi hàm {func.__name__}")
            return func(*args, **kwargs)
         return wrapper
      
      @log
      def say_hello():
         print("Hello!")

      say_hello()
      # Gọi hàm say_hello
      # Hello!
   ```
#### 2.2 Context Manager (`with` statement)   
   - **Quản lý tài nguyên** (file, kết nối...) → tự đóng/ giải phóng khi xong việc.
   - Cú pháp:
   ```python
      with open("data.txt", "w") as f:
         f.write("Xin chào")
      # File tự đóng sai khi ra khỏi khối with

      #Tự tạo context manager
      class MyCM:
         def __enter__(self):
            print("Bắt đầu")    
            return self
         def __exit__(self, exc_type, exc, tb):
            print("Kết thúc")

      with MyCM():
         print("Trong khối with")
   ```

3. **Xử lý dữ liệu nâng cao**

   - `itertools`, `collections` (`Counter`, `defaultdict`)
   - Regular Expressions (`re`)

4. **Thuật toán & cấu trúc dữ liệu**

   - Sort, search
   - Stack, Queue, Linked List (dùng Python list/deque)

5. **Unit Test**

   - `unittest`, `pytest`

6. **Giao tiếp API**
   - `requests` module
   - GET/POST JSON

---

## **Giai đoạn 4 – Ứng dụng thực tế (4 → 8 tháng)**

**Mục tiêu:** Xây dựng dự án thật với Python.

1. **Web Development**

   - Flask / FastAPI / Django
   - REST API, CRUD

2. **Data Analysis**

   - `pandas`, `numpy`, `matplotlib`
   - Làm sạch, phân tích và visualize dữ liệu

3. **Automation**

   - `selenium`, `beautifulsoup`
   - Tự động tải, gửi email, crawl dữ liệu

4. **Machine Learning**
   - `scikit-learn`, `tensorflow`, `pytorch` (nếu đi hướng AI)
   - Bài toán phân loại, dự đoán

---

## **Giai đoạn 5 – Chuyên gia & Best Practices**

**Mục tiêu:** Code tối ưu, dễ bảo trì.

- Design Patterns với Python
- Clean Code & PEP8
- Viết package publish lên PyPI
- Async Programming (`asyncio`)
- Multithreading & Multiprocessing

---

## **Tips học hiệu quả**

- Mỗi giai đoạn nên làm **dự án nhỏ** (game console, web app, crawler…)
- Đọc tài liệu chính thức: [https://docs.python.org/3/](https://docs.python.org/3/)
- Code mỗi ngày ít nhất 30–60 phút
- Học kèm Git & GitHub để quản lý dự án
