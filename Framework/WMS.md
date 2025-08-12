## Windows
查看窗口层级树：
dumpsys window containers

# UI框架
UI框架
      --窗口管理
         --基础流程
             --窗口类型
             --树状结构
             --窗口添加/移除
             --窗口布局和显示
             --焦点管理
               
         --屏幕旋转
             --屏幕方向计算
             --冻屏/解冻流程
              
         --动画系统
             --LockFree动画流程
             --AppTransition-远程动画  系统动画
             --窗口动画
             --Insets动画
               
         --系统窗口处理
             --壁纸
             --Inset机制
             --状态栏/导航栏
             --锁屏
             --输入法
          
               
        
      --渲染合成
         --硬件加速原理
         --GraphicBuffer生产和消费流程
         --Layer合成流程
         --V-Sync机制
         --SurfaceView和TextureView原理
         
      --公共控件
         --控件布局/绘制流程
         --控件动画系统
         
      --输入系统
          --InputReader
                --输入设备管理流程
                --输入事件解析流程
                --Viewport创建和使用
          --InputDispathcer
                --Key派发流程
                --Motion派发流程
                --InputFilter
                --InputMotion
                --事件传输过程InputTransport
                
          --View事件分发流程
      
      --屏幕管理
          --屏幕类型
          --屏幕添加和移除
          --屏幕映射原理
          --镜像模式\拓展模式原理
          --应用启动到目标屏幕
         
      

# Wm-Shell
运行在systemui进程里面，framework维护

# Window Manager Services

## 动画
请求动画：
Requesting StartTransition:|Starting Transition
动画开始，动画参数info：
WindowManagerShell: onTransitionReady|Set transition ready
结束动画,请求到结束的时间：
finishTransition transition|WindowManager: Finish Transition
收集动画：
Collecting in|Checking filter Pair
可见性：
WindowManager: commitVisibility:|Transition: hasChanged
动画类型:
WindowManagerShell: start
动画堆栈：
TransitionController:
动画发起方：
animated by
动画info：
WindowManager:     info=
 
 
 
关键动画流程：
请求动画                 开始动画         结束动画
Requesting StartTransition:|onTransitionReady|Finish Transition

