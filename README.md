from datetime import datetime

# Assuming df5 is your DataFrame and 'Month' is the column containing values like 'Jan'24'
df5['Month'] = df5['Month'].apply(lambda x: datetime.strptime(x, "%b'%y").strftime('%b%y'))
