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
