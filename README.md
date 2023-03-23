# HW2_hash_practice
# 打開文件
with open('hw2_data.txt', 'r') as file:
    # 建立一個字典來統計詞彙出現次數
    word_counts = {}
    # 逐行讀取文件內容
    for line in file:
        # 將每一行轉換成單詞列表，並遍歷每一個單詞
        for word in line.split():
            # 將單詞轉換成小寫
            word = word.lower()
            # 如果單詞已經在字典中出現過，則將其計數器加一
            if word in word_counts:
                word_counts[word] += 1
            # 否則，將單詞加入字典並初始化計數器為一
            else:
                word_counts[word] = 1

# 輸出總共有多少種不重複的詞彙
print("總共有", len(word_counts), "種不重複的詞彙：")

# 輸出每個詞彙出現的次數
for word, count in word_counts.items():
    print(word, "出現了", count, "次。")
