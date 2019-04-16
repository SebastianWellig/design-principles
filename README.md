# design-principles
## Uncategorised Considerations
### API based / Customizable / Extendable
- API is not just meant to be used for customization by users. They should
also provide the fundamental framework on which the software itself is
build.  
_e.g._ `Achilles_fnc_defineDialogControl`
- API functions as the one above should be as general as possible. More
specializations can be added by subclassing (in OOP) or providing other more
specialized API functions.

### Handling Huge Data
- Prevent repetition of iterating over the same huge data again and again by
caching.  
Prime example: ArmA 3 Zeus interface loading is expensive due to filtering
all available classes every time.
- Split huge data into groups. This allows loading a subset of data when
needed. Also allows updating caches for affected groups instead of the entire
data when needed.
