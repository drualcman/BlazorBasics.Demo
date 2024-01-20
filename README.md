# How to use Digital Door Blazor Basics

All examples are using Bulma CSS Framework

## BlazorBasics.Captcha

Example to show send button after validate a math question.

``` RAZOR
<CaptchaComponent class="button">
    <AfterValidate>
        <button class="button is-primary" type="submit">Send</button>
    </AfterValidate>
</CaptchaComponent>
```

## BlazorBasics.InputFileExtended

Example to allow copay and paste and drag and drop the files.

``` RAZOR
<InputFileComponent OnChange="GetFile" Parameters="InputParameters" />

@code{
    BlazorBasics.InputFileExtended.ValueObjects.InputFileParameters InputParameters = new BlazorBasics.InputFileExtended.ValueObjects.InputFileParameters()
        {
            AllowPasteFiles = true,
            DragAndDropOptions = new BlazorBasics.InputFileExtended.ValueObjects.DragAndDropOptions
            {
                CanDropFiles = true
            }
        };

    void GetFile(FilesUploadEventArgs file)
    {
        // your code to manage teh file
    }
}
```

## BlazorBasics.RichTextEditor

Example to add a rich text with a save button in the tool bar

``` RAZOR
 <RichTextEditorComponent OnSave="SaveComment" />
 @code{
    void SaveComment(string content)
    {
        // your code to manage the content
    }
 }
```