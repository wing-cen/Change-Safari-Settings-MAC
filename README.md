# How-to-change-Mac-Safari-settings-in-code
<h3>Mac Safari 设置代码修改实现</h3>
最近由于工作上遇到一个问题需要修改Safari的设置程序才能正常运行，所以研究了一下怎么在代码中修改Safari的设置。</br>
主要方法是通过使用system（）函数在命令行修改设置。</br>
在我们电脑的~/Library/Preferences/com.apple.Safari.plist 路径下有个Safari设置文件如下</br>


<h3>源码</h3>
system([@"defaults write ~/Library/Preferences/com.apple.Safari.plist LocalFileRestrictionsEnabled -bool FALSE" UTF8String]);
system([@"defaults write ~/Library/Preferences/com.apple.Safari.plist WebKitAllowUniversalAccessFromFileURLs -bool TRUE" UTF8String]);
system([@"defaults write ~/Library/Preferences/com.apple.Safari.plist WebKitAllowFileAccessFromFileURLs -bool TRUE" UTF8String]);
system([@"defaults write ~/Library/Preferences/com.apple.Safari.plist com.apple.Safari.ContentPageGroupIdentifier.WebKit2JavaEnabledForLocalFiles -bool TRUE" UTF8String]);
system([@"defaults write ~/Library/Preferences/com.apple.Safari.plist com.apple.Safari.ContentPageGroupIdentifier.WebKit2AllowFileAccessFromFileURLs -bool TRUE" UTF8String]);
system([@"defaults write ~/Library/Preferences/com.apple.Safari.plist com.apple.Safari.ContentPageGroupIdentifier.WebKit2AllowUniversalAccessFromFileURLs -bool TRUE" UTF8String]);
