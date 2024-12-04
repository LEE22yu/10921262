# 10921262
# 顯示任務清單
def show_tasks():
    print("\n=== 任務清單 ===")
    print("未完成的任務：")
    if not pending_tasks:
        print("\n  目前沒有任何任務！\n")
    else:
        for idx, task in enumerate(pending_tasks, start=1):
            print(f"  {idx}. {task['title']} ({task['description'][:40]})") # 描述部份最多顯示 40 個字元
    
    print("\n已完成的任務：")
    if not completed_tasks:
        print("\n  目前沒有任何任務！\n")
    else:
        for idx, task in enumerate(completed_tasks, start=1):
            print(f"  {idx}. {task['title']} ({task['description'][:40]})") # 描述部份最多顯示 40 個字元
    print()
