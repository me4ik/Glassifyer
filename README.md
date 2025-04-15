# Glassifyer
Small .NET class for creating glassmorphism/acrylic style windows in WPF.

## Example:


![image](https://github.com/user-attachments/assets/b54f05df-ecc6-40a4-aca8-e1693a894a5a)

## Usage
1. Add the glassifyer static class to your project
2. Set your window options like this:
```
public YourWindowNameHere()
{
    InitializeComponent();

    this.AllowsTransparency = true;
    this.WindowStyle = WindowStyle.None;
    this.Background = Brushes.Transparent;
}
```
3. Add blur to your window:
```
private void YourWindow_LoadedListener(object sender, RoutedEventArgs e)
{
    Glassifyer.EnableBlur(this);
}
```
4. Enjoy!

## Remarks
If you have a window with 100% transparency, your click will go through it. To fix it, add a grid or any other element with 1% or more transparency to the window and it will work.
