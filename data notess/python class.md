20 Python one-liners I use constantly in my analysis.  
  
𝗗𝗔𝗧𝗔 𝗤𝗨𝗔𝗟𝗜𝗧𝗬  
  
df.duplicated() — find duplicate rows  
df.isna().sum() — count missing values per column  
df.describe() — get a full statistics summary instantly  
  
𝗖𝗟𝗘𝗔𝗡𝗜𝗡𝗚  
  
df.drop_duplicates(keep='last') — remove duplicates, keep the latest  
df.fillna() — handle missing values  
df.replace({dict}) — replace multiple values at once  
df.str.contains() — filter text columns without regex headaches  
df.clip() — cap outliers without removing them from your dataset  
  
𝗔𝗡𝗔𝗟𝗬𝗦𝗜𝗦  
  
df.value_counts(normalize=True) — calculate percentages instantly  
pd.crosstab() — create a pivot summary in one line  
df.groupby().nlargest() — get the top N results per group  
  
𝗧𝗥𝗔𝗡𝗦𝗙𝗢𝗥𝗠𝗔𝗧𝗜𝗢𝗡  
  
pd.cut() — create bins from continuous numbers  
df.merge() — join two dataframes  
df.pivot_table() — create flexible pivots  
df.assign() — add new columns without overwriting your original dataframe  
df.explode() — unnest list columns into individual rows  
df.pipe() — chain multiple operations cleanly in sequence  
  
𝗦𝗘𝗟𝗘𝗖𝗧𝗜𝗢𝗡 & 𝗦𝗢𝗥𝗧𝗜𝗡𝗚  
  
df.query() — filter with readable syntax instead of brackets  
df.nlargest(n, 'col') — get the top N rows by column value  
df.sort_values() — sort by one or multiple columns


![[Pasted image 20260525055706.png]]