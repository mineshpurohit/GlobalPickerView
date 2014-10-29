GlobalPickerView
================

Global Picker View Library use for show Picker View in both iPhone and iPad with single call.

For using this Library in your xcode project.

Follow below steps:

1) Add GlobalPickerView File in your xcode project and make sure you check copy file if needed.

2) #import "PickerViewForiOS.h" add this line in view controller where you want to show Picker View.

3) Add below code for calling Show Picker View Method:

-> Add below script you want to Show Picker With Customer Array of Dictionary for Single Selection.

    // For get selected Index for Previous Selected Object. If first time it will retrun 0.
    NSInteger selectedIndex = [PickerViewForiOS getSelectedIndexFromArray:<Array-of-List> forSelectedId:<String-Value-That-Selected> inKey:<String-Key-Where-Value-Stored>];
    [PickerViewForiOS openScrollViewInView:<View-Where-You-Want-To-Show> delegate:<Delegate-Class> responder:<Sender-Object> valueInArray:<Array-of-List> selectedObjectId:selectedIndex];
    

-> Add below script you want to Show Picker With Customer Array of Dictionary for Multiple Selection.

    [PickerViewForiOS openScrollViewWithMultiPalSelInView:<View-Where-You-Want-To-Show> delegate:<Delegate-Class> responder:<Sender-Object> valueInArray:<Array-Of-List> andSelectedId:<Selected-Value-of-Id's> keyOfId:<String-Key-Where-Id-Stored> keyOfString:<String-Key-Where-Value-Stored>];
    

-> Add below script you want to Show Date & Time Picker.

    [PickerViewForiOS showDateTimePickerInView:<View-Where-You-Want-To-Show> delegate:<Delegate-Class> responder:<Sender-Object>];
    

-> Add below script you want to Show Date Picker.

    [PickerViewForiOS showOnlyDatePickerInView:<View-Where-You-Want-To-Show> delegate:<Delegate-Class> responder:<Sender-Object>];
    


After completing with add script for show picker. You need to implement Delegate Method of that Global Picker View as mention below:

    #pragma mark - Picker Action Delegate
    -(void) performAction:(id)object withSelectedValue:(NSString *) string
    {
      if ([string length] > 0)
      {
        /* Add you code there. string valuable will return value as below conditions:
           For Single Selection Picker: return's selected Index.
           For Multiple Selection Picker: return's selected ids with comma seperated.
           For Date&Time Picker: return's Date And Time in String format.
           For Only Date Picker: return's Only Date in String format.
        */ 
      }
    }
    #pragma mark -

