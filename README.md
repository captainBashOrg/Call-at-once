print("Вызов разом")

def apply_all_func(int_list, *functions):
    results = {}   # пустой словарь результата
    for func in functions:
        results [ func.__name__ ] = func (int_list)
    return results

def reverse ( int_list ):   # Чуть больше, чем в ТЗ
    return sorted (int_list, reverse=True)


int_list = [6, 20, 15, 9]

print(apply_all_func([6, 20, 15, 9], max, min))
print(apply_all_func([6, 20, 15, 9], len, sum, sorted))
print(apply_all_func([6, 20, 15, 9], reverse))
