## 侧边滑动  a single swiping delete for ListView and GridView
>* 1.支持左滑删除 support left Swiping deleted
>* 2.支持右滑删除 support right Swiping deleted
>* 3.支持左滑打开关闭 support left Swiping open and close with Threshold
>* 4.支持右滑打开关闭 support right Swiping open and close with Threshold

                <Grid Grid.Row="5">
                    <Grid x:Name="CommandContainer" 
                              Margin="1" x:DeferLoadStrategy="Lazy">
                 
                        <ctl:WYBtnLable x:Name="LeftCommandPanel" 
                                    Background="SkyBlue" 
                                    VerticalAlignment="Stretch" 
                                    HorizontalAlignment="Left"
                                        HorizontalContentAlignment="Left"
                                        VerticalContentAlignment="Center"
                                         Padding="10"
                                        Content="right" 
                                        BorderBrush="Black" 
                                        Foreground="White"/>

                        <ctl:WYBtnLable  Grid.Column="1" 
                                         Background="Red" 
                                        HorizontalAlignment="Right"
                                        VerticalAlignment="Stretch" 
                                        HorizontalContentAlignment="Right"
                                         VerticalContentAlignment="Center"
                                         Padding="30"
                                        Content="删除" 
                                         BorderBrush="Black" 
                                        Foreground="White"/>
                    
                    </Grid>
                    <Grid x:Name="ContentGrid"
                              Background="Green"
                              ManipulationMode="TranslateX,System">
                        <ContentPresenter />
                        <Grid.RenderTransform>
                            <CompositeTransform x:Name="ContentTransform" TranslateX="-50"/>
                        </Grid.RenderTransform>
                    </Grid>
                </Grid>

--------

![cmd-markdown-logo](http://images2015.cnblogs.com/blog/443660/201703/443660-20170321175800846-2113702927.gif)

eg:

        <DataTemplate x:Key="SampleItemTemplate">
            <Border Background="{ThemeResource SystemControlHighlightListAccentHighBrush}">
                <ctl:WYSlidableItem cm:Message.Attach="[Event RightClick] = [Action Remove($dataContext)]" 
                                    LeftLabel="ss"
                                    LeftBackground="Red"
                                    LeftPadding="30"
                                    LeftForeground="White"
                                    RightLabel="delete"
                                    RightBackground="Red"  
                                    RightPadding="30"
                                    RightForeground="White">
                    <Image Source="{Binding}" Stretch="Fill" HorizontalAlignment="Stretch" VerticalAlignment="Stretch"/>
                    <!--<ctl:WYCacheView HttpUrl="{Binding}" Remove($dataContext) Background="Gray" StretchSource="UniformToFill"/>-->
                </ctl:WYSlidableItem>
            </Border>
        </DataTemplate>        
--------

        RightClick : for delete  
        public void Remove(string character)
        {
            HelloView.Remove(character);
        }
        LeftLabel="ss" 
        LeftBackground="Red"
        LeftPadding="30"
        LeftForeground="White"
        RightLabel="delete"
        RightBackground="Red"  
        RightPadding="30"
        RightForeground="White"
        above all property you can customized 
##      Get the control - I recommend using NuGet: https://www.nuget.org/packages/CCUWPToolkit/

