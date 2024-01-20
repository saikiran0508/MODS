from datetime import datetime

# Assuming df5 is your DataFrame and 'Month' is the column containing values like 'Jan'24'
df5['Month'] = df5['Month'].apply(lambda x: datetime.strptime(x, "%b'%y").strftime('%b%y'))
# Assuming 'YourColumn' is the column with float values
df5['YourColumn'] = pd.to_numeric(df5['YourColumn'], errors='coerce').astype('Int64')



import pandas as pd

# Replace 'YourDataFrame' with the actual name of your DataFrame
# Replace 'Column1', 'Column2', etc., with the actual column names you want to convert

columns_to_convert = ['Column1', 'Column2', 'Column3']

for column in columns_to_convert:
    df['YourDataFrame'][column] = df['YourDataFrame'][column].astype('Int64')
