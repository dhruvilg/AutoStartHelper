# AutoStartHelper

include the AutoStartHelper.java file in your android studio.

call this code where ever you want, most probably before login.

        sharedpreferences = getSharedPreferences(MainActivity.MyPREFERENCES, Context.MODE_PRIVATE);
        autoStart = sharedpreferences.getString("autoStart", "");
        if (autoStart.equals("")) {
            AutoStartHelper.getInstance().getAutoStartPermission(this);
        }

now when the app is been enabled from auto start, it will start receiving the push notification even when the app is killed
