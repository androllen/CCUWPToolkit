# WYBtnColors

A simple button with colors control which is commonly used in Android apps.

Currently this control is available for UWP for desktop only. I do not plan to add a UWP for mobile version, but feel free to create one. This project is compatible with Visual Studio Community 2015.

# How to use

1. Get the control - I recommend using NuGet: https://www.nuget.org/packages/CCUWPToolkit/
2. Import the namespace in your XAML: `xmlns:ctl="using:CCUWPToolkit.Controls"`
3. Include the control in the content area of your page: `<ctl:WYBtnColors />`
4. Customise the control and its content:
	- `Label`:  Set the master text
	- `LabelNum`: Set the second text
	- `ColorsSource`: Set the background of the WYBtnColors area
	- `IsEnableAdaptiveLable`: Set the flow of the WYBtnColors
	- `IsEnableStackLable`: Set the StackPanel of the WYBtnColors
  - `GeneratedBaseHorizontalStretch`: Set the Main Horizontal Stretch of the WYBtnColors
  - `GeneratedBaseVerticalStretch`: Set the Base Vertical Stretch of the WYBtnColors
  - `GeneratedContentHorizontalStretch`: Set the Content Horizontal Stretch of the WYBtnColors
  - `GeneratedContentVerticalStretch`: Set the Content Vertical Stretch of the WYBtnColors  
  - `GeneratedImageHorizontalStretch`: Set the Image Horizontal Stretch of the WYBtnColors
  - `GeneratedImageVerticalStretch`: Set the Image Vertical Stretch of the WYBtnColors  
5. Provide contents:
	- Put the stuff to present in the WYBtnColors inside the Property `IsEnableStackLable`: `<ctl:WYBtnColors IsEnableStackLable="True" Height="40" VerticalAlignment="Top" Label="1111" LabelNum="222" ColorsSource="Green">`
	- Put the pages content in the content area of the control
	
You may take a look at the sample project which is included in the repository.

# Preview
![](http://images2015.cnblogs.com/blog/443660/201703/443660-20170321192408393-1775305892.gif)

# Contribute
Feel free to contribute to this project: add issues or create pull request.

# Changelog
## 1.0.4:
* Initial implementation
