#### For the invalid dog names, there is a better way to clean it that was suggested in the review of this code:

"Most incorrectly recorded names are lower case rather than correctly recorded names which are capitalized. Therefore, we can use str.islower() to find these incorrect dog names and then clean this issue."
- to find the count of all invalid names: \
 twitter_arch_clean[twitter_arch_clean.name.str.islowe()].name.value_counts() 
- we knew them, then we locate them and replace them with NaN: \
 twitter_arch_clean.loc[twitter_arch_clean.name.str.islower() == True , 'name'] = np.nan
