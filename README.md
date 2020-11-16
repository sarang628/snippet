# snippet

```
InputStream is = getResources().openRawResource(R.raw.json_file);
Writer writer = new StringWriter();
char[] buffer = new char[1024];
try {
    Reader reader = new BufferedReader(new InputStreamReader(is, "UTF-8"));
    int n;
    while ((n = reader.read(buffer)) != -1) {
        writer.write(buffer, 0, n);
    }
} finally {
    is.close();
}

String jsonString = writer.toString();
                
```

```
fun getDummy(application: Application): String {
        val inputStream = application.getResources()
            .openRawResource(com.example.screen_cardinfo.R.raw.restaurant_list);
        val writer = StringWriter();
        var buffer = CharBuffer.allocate(1024)
        try {
            var reader = BufferedReader(InputStreamReader(inputStream, "UTF-8"));
            var n: Int

            n = reader.read(buffer)

            while (n != -1) {
                writer.write(buffer.array(), 0, n);
                buffer.clear()
                n = reader.read(buffer)
            }
        } catch (e: Exception) {
        } finally {
            try {
                inputStream.close();
            } catch (e: IOException) {
                Log.e("sarang", e.toString())
                e.printStackTrace()
            }
        }
        var jsonString = writer.toString();
        return jsonString
    }
```

```
object getRawToString {
    fun getDummy(context: Context): String {
        val inputStream = context.getResources().openRawResource(R.raw.alarm);
        val writer = StringWriter();
        var buffer = CharBuffer.allocate(1024)
        try {
            var reader = BufferedReader(InputStreamReader(inputStream, "UTF-8"));
            var n: Int
            n = reader.read(buffer)
            while (n != -1) {
                writer.write(buffer.array(), 0, n);
                buffer.clear()
                n = reader.read(buffer)
            }
        } catch (e: Exception) {
        } finally {
            try {
                inputStream.close();
            } catch (e: IOException) {
                Log.e("__sarang", e.toString())
                e.printStackTrace()
            }
        }
        var jsonString = writer.toString();
        return jsonString
    }

    fun Context.getRawtoString(id: Int): String {
        val inputStream = getResources().openRawResource(id);
        val writer = StringWriter();
        var buffer = CharBuffer.allocate(1024)
        try {
            var reader = BufferedReader(InputStreamReader(inputStream, "UTF-8"));
            var n: Int
            n = reader.read(buffer)
            while (n != -1) {
                writer.write(buffer.array(), 0, n);
                buffer.clear()
                n = reader.read(buffer)
            }
        } catch (e: Exception) {
        } finally {
            try {
                inputStream.close();
            } catch (e: IOException) {
                Log.e("__sarang", e.toString())
                e.printStackTrace()
            }
        }
        var jsonString = writer.toString();
        return jsonString
    }
}
```
