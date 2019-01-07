# CodeGenerator
A web based code generator based on the template you supply. It can be used for any purpose, coding or otherwise.  Repetitive tasks sometimes get boring and result in typos, hence it needs some level of automation to overcome it. **That's exactly what this does!**


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

2. Choose the template or type your template in the Template textbox. eg. for BindableProperty, the following will be the template:
```C#
public static readonly BindableProperty $1Property = BindableProperty.Create ("$1", typeof($2), typeof($3), $4);

public $2 $1 {
  get => ($2)GetValue ($1Property);
  set => SetValue ($1Property, value);
}
```

3. Click on the **Generate Code** to generate the code. If you have 100 lines of property data, it will generate 100 properties based on the template, which would have taken a considerable amount of time, if done manually.

4. That's it.
