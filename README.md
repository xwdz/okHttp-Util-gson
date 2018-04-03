### 添加依赖

> todo


### Get

```
MethodGet methodGet = OkHttpRun.get("url");
        methodGet.addParams("user_key", "6a78a77c1ab1416582166e3b02446eea");
        // or methodGet.addParams(new LinkedHashMap<String, String>());
        methodGet.execute(new CallBack() {
            @Override
            public void onError(Call call, Exception e) {

            }

            @Override
            public void onResponse(Call call, Object response) {

            }
        });
```


### POST

```
 MethodPost post = OkHttpRun.post("url");
        post.addParams("username","abc");
        post.addParams("password","000000");
        //设置解析bean
        post.setClass(Test2.class);
        post.execute(new CallBack<Test2>() {
            @Override
            public void onError(Call call, Exception e) {

            }

            @Override
            public void onResponse(Call call, Test2 response) {
                mTextView.setText(response.toString());
            }
        });
```


### 配置OkHttpClient

> 添加拦截器到默认client

```
HttpManager.getInstance().addInterceptor();
HttpManager.getInstance().addNetworkInterceptor();
```

> 获取内置OkHttpClient

```
HttpManager.getInstance().getDefaultClient();
```

> todo




