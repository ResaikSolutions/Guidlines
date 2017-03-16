# Code review references iOS (Resaik Solutions)
---
During writing new code and for code review follow the policy.

| Rule name | Rule description | How to fix |
| - | - | - |
|**RSWrongCodeStyle**| *Follow code style.* | *Install and use* [XcodeClangFormat](https://github.com/mapbox/XcodeClangFormat#building). |
|**RSCommentedCode**| *Don't leave commented code.* | *Delete commented code or leave a comment why this code should not be deleted.* |
|**RSDebugLog**| *Logging intended for debug.* | *Delete logging for debug.* |
| **RSWrongFloatFormat** | *Float format is 0.0f. Not 0, not 0.0, not .0, not .0f. The '.' and 'f' symbols are mandatory.* | *Write float value in "0.0f" format.* |
|**RSWrongCopyrights**| *Wrong copyrights.* | ***Created by** must contain a real full name. **Copyrights** must be **Resaik Solutions**. Also be sure if copyrights set correctly in project file.* |
| **RSUnnecessaryNilCheck** | *Don't check for nil before calling a method. For example:* `if (self.array != nil && self.array.count > 0)` | `if (self.array.count)` |
| **RSEmptyBlock** | *Prefer using **nil** instead empty block when it's possible.*| `[self presentViewController:vc animated:YES completion:nil];`|
| **RSTrivialMethodOverwrite** | *Don't leave methods that only call those **super**.* | *Delete this method at all.* |
|**RSMagicValue** | *Variable's name like: **a**, **b**, **x**, **y**, **c2** etc.* | *All values should be named in code.* |
|**RSPreferNSTypesVSCType**| *Prefer using NSInterger, NSUInteger, CGFloat vs int, float, double etc.* | *Replace int, float, double with corresponded NS type.* |
|**RSWrongCallProperty**| *Don't call **property** getter/setter as a method. For example*: ` [self setFrame:frame];` | `self.frame = frame;` |
|**RSCollectionTypeRequire**| *Mandatory using type of any collections.* `@property (nonatomic, strong) NSArray *list;` | `@property (nonatomic, strong) NSArray<NSString *> *list;` |
|**RSOldObjectiveCStyle**| *Old Objective-C code style used.* | *Apply new Objective-C 2.0 style. Such as: `@(2.0f);`, `array[0];`, `dictionary[@"key"]` etc.* |
