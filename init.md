# init 调用的情况：
1. 当canister第一次被安装时，会被调用
2. 用--mode=reisntall后，会被调用
3. upgrade canister时，不会被调用，这时系统会对旧版本先调用canister_pre_upgrader, 然后对新版本调用canister_post_upgrader.

## 这意味着如果你没有指定使用稳定内存的upgrade钩子来更新canister， 所有的状态将会失去。



