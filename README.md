# CodeGenerator
A web based code generator based on the template you supply


### How to use?
1. Enter your data line-by-line separated with commas in Input textbox. eg. for BindableProperty, the following will be the code:
- FontSize, double, ControlName, 12
- Radius, float, ControlName, 6f

The above 2 lines will generate the following output:
```C#
public static readonly BindableProperty FontSizeProperty = BindableProperty.Create ("FontSize", typeof(double), typeof(ControlName), 12);

public double FontSize {
  get => (double)GetValue (FontSizeProperty);
  set => SetValue (FontSizeProperty, value);
}

public static readonly BindableProperty RadiusProperty = BindableProperty.Create ("Radius", typeof(float), typeof(ControlName), 6f);

public float Radius {
  get => (float)GetValue (RadiusProperty);
  set => SetValue (RadiusProperty, value);
}
```

2. Choose the template or type your template in the Template textbox
3. Click on the **Generate Code** to generate the code.
4. That's it.
