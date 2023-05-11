def check_signs(arr):
  if len(arr)<2:
    return False
    sign=arr[0]>=0
    for i in range(1, len(arr)):
      if (arr[i]>=0)==sign:
        return False
        sign= not sign
      return True

arrays=[]
for i in range(5):
  arr =list(map(float, input(f"Введите элементы массива {i+1} через пробел: ").split()))
  arrays.append(arr)

found=False
for i in range(5):
  if check_signs(arrays[i]):
    print(f"ьассив под номером {i+1} является знакочередующимся")
    found=True


if not found:
  print("нету знакочередущих массивов")
