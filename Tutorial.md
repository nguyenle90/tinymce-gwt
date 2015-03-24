# Introduction #

It is really simple to use and configure the editor at your needs. In the future there will be more funtionality through the java code. For now you can only set the init parameters using a configuration instance.

## Step 1 ##
Copy the jar in the WEB\_INF/lib directory

## Step 2 ##
In your module xml configuration file insert the line
```
<inherits name="gr.open.TinymceGwt"/>
```


# Details #

## Simple editor ##
The most simple way to create a tinyMCE widget (using the default configuration) is:
```
	public void onModuleLoad() {
		RootPanel.get().add(new TinyMCE());
	}
```

## Using own configuration ##
If you want to use your own configuration, to change for example the skin, or the icons, you can create your own Configuration Class, extending the AbstractTinyMCEConfiguration class.

If you don't want to do something like that, you can use the following code:
```
	public void onModuleLoad() {
		TinyMCE editor = new TinyMCE();
		editor.getConfig().setTheme("simple");
		RootPanel.get().add(editor);
	}
```

This would create a simple editor.