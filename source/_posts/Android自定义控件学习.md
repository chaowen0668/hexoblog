title: Android自定义控件学习
date: 2015-09-24 14:36:18
tags: android
categories: android

---
# 控件架构 #
控件分为ViewGroup控件与View控件。ViewGroup控件作为父控件可以包含多个View控件，并管理包含的View控件。通过ViewGroup,整个界面上的控件形成了一个树形结构，这也就是我们常说的控件树，上层控件负责下层子控件的测量与绘制，并传递交互事件。

# 自定义View #
## 自定义view的分类 ##
1. 继承View重写onDraw方法

    这种方法主要用于实现一些不规则的效果,采用这种方式需要自己支持wrap_content,并且padding也要处理。

2. 继承ViewGroup派生特殊的Layout
   
    实现自定义布局。重新定义一种新的布局。需要处理View    

3. 继承特定的View(比如Textview)

    用于扩展已有的View的功能。不需要自己支持wrap_content和padding。
4. 继承特定的ViewGroup(比如LinearLayout)

   
## 自定义View的注意 ##
1. 让View支持wrap_content
2. 如果有必要，让你的view支持padding
3. 尽量不要在View中使用Handler。
4. View中如果有线程或者动画，需要及时停止。
5. View中带有滑动嵌套情形时,需要处理好滑动冲突。

## 自定义view示例 ##
### 继承View重写onDraw方法 ###
```
public class CircleView extends View{

   private int mColor = Color.RED;
    private Paint mPaint = new Paint(Paint.ANTI_ALIAS_FLAG);
    public CircleView(Context context) {
        super(context);
        init();
    }

    public CircleView(Context context, AttributeSet attrs) {
        super(context, attrs);
        init();
    }

    public CircleView(Context context, AttributeSet attrs, int defStyleAttr) {
        super(context, attrs, defStyleAttr);
        init();
    }



    private void init(){
        mPaint.setColor(mColor);
    }

    @Override
    protected void onDraw(Canvas canvas) {
        super.onDraw(canvas);
        final int paddingLeft = getPaddingLeft();
        final int paddingRight = getPaddingRight();
        final int paddingTop = getPaddingTop();
        final int paddingBottom = getPaddingBottom();
        int width = getWidth()-paddingLeft - paddingBottom;
        int height = getHeight() - paddingTop - paddingBottom;
        int radius = Math.min(width,height) /2;
        canvas.drawCircle(paddingLeft+width/2,paddingTop+height/2,radius,mPaint);
    }

    @Override
    protected void onMeasure(int widthMeasureSpec, int heightMeasureSpec) {
        super.onMeasure(widthMeasureSpec, heightMeasureSpec);
        int widthSpecMode = MeasureSpec.getMode(widthMeasureSpec);
        int widthSpecSize = MeasureSpec.getSize(widthMeasureSpec);
        int heightSpecMode = MeasureSpec.getMode(heightMeasureSpec);
        int heightSpecSize = MeasureSpec.getSize(heightMeasureSpec);
        if(widthSpecMode == MeasureSpec.AT_MOST && heightSpecMode == MeasureSpec.AT_MOST){
            setMeasuredDimension(200,200);
        }else if(widthSpecMode == MeasureSpec.AT_MOST){
            setMeasuredDimension(200,heightSpecSize);
        }else if(heightSpecMode == MeasureSpec.AT_MOST){
            setMeasuredDimension(widthSpecSize,200);
        }
    }
}
```