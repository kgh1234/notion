# notion

1. Preparing to connect the Notion database with Python code
```database_id = "input your database id"
notion_key = "input your notion key"
notion_db = NotionDatabase(database_id, notion_key)
```

2. property information of the Notion database
```
notion_db.print_property_dict()
```
![image](https://github.com/user-attachments/assets/a8b9a7b3-2526-418c-8b7d-192a4635f6fa) ![image](https://github.com/user-attachments/assets/4ae3bfa8-cc6a-4ba3-8bce-caa198ac4489)

3. Date and time in ISO 8601 format
```
DATE = notion_db.transform_date("20230101000000")
# 2023-01-01T00:00:00.000+09:00
```

4.Automated data upload 
```
page_values = {
    "Model": "model_name",
    "Dataset": "Dataset",
    "Input Size": "Input_Size",
    "Batch Size": "Batch_Size",
    "Learning Rate": 0.5,
    "Loss Func": "Loss_Function",
    "Class Weight": "(0:1, 1:1)",
    "Threshold": 0.5,
    "Precision": 0.5,
    "Recall": 0.5,
    "F1 Score": 0.5,
    "Accuracy": 0.5,
    "상태": "Done",
    "실행 일시": DATE
}

notion_db.upload_page_values(page_values)
```

5. Code execution
   
Automating the process of adding or retrieving data in a Notion database
   
url:https://github.com/LHyunn/NotionDatabaseAPI
