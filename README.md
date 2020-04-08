# How to work with Expander using C# in Xamarin.Forms (SfExpander)

You can create the [SfExpander](https://help.syncfusion.com/xamarin/expander/getting-started?) using the C# in Xamarin.Forms.

You can also refer the following article.

https://www.syncfusion.com/kb/11367/how-to-work-with-expander-using-c-in-xamarin-forms-sfexpander 

**C#**

Creating the SfExpander in the constructor of the MainPage.

``` c#
public partial class MainPage : ContentPage
{
    SfExpander expander, expander2;
    ScrollView scrollView;
    StackLayout stack;
    public MainPage()
    {
        InitializeComponent();
        scrollView = new ScrollView();
        stack = new StackLayout();
        //Expander One
        expander = new SfExpander();
        //Expander Header
        var headergrid = new Grid()
        {
            HeightRequest =60
        };
        var headerLabel = new Label()
        {
            TextColor = Color.White,
            BackgroundColor = Color.Teal,
            HorizontalTextAlignment =TextAlignment.Center ,
            Text = "Veg Pizza",
            VerticalTextAlignment = TextAlignment.Center
        };
        headergrid.Children.Add(headerLabel);
        expander.Header = headergrid;
        //Expander Content
        var contentgrid = new Grid()
        {
            HeightRequest =60
        };
        var contentLabel = new Label()
        {
            TextColor = Color.Black,
            BackgroundColor = Color.White,
            Text = "Veg pizza is prepared with the items that meet vegetarian standards by not including any meat or animal tissue products.",
            VerticalTextAlignment = TextAlignment.Center,
            HeightRequest = 50
        };
        contentgrid.Children.Add(contentLabel);
        expander.Content = contentgrid;
        //Expander Two
        expander2 = new SfExpander();
        //Expander Header
        var headergrid2 = new Grid()
        {
            HeightRequest =60
        };
        var headerLabel2 = new Label()
        { TextColor = Color.White,
            BackgroundColor = Color.Teal,
            Text = "Non- Veg Pizza",
            HorizontalTextAlignment = TextAlignment.Center,
            VerticalTextAlignment = TextAlignment.Center
        };
        headergrid2.Children.Add(headerLabel2);
        expander2.Header = headergrid2;
        //Expander Content
        var contentgrid2 = new Grid();
        var contentLabel2 = new Label() 
        {
            TextColor = Color.Black,
            BackgroundColor = Color.White,
            Text = "Non-veg pizza is prepared by including the meat and animal tissue products.",
            VerticalTextAlignment = TextAlignment.Center,
            HeightRequest = 50
        };
        contentgrid2.Children.Add(contentLabel2);
        expander2.Content = contentgrid2;
        stack.Children.Add(expander);
        stack.Children.Add(expander2);
        scrollView.Content = stack;
        this.Content = scrollView;
    }
}
```
