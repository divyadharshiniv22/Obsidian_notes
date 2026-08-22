**Jinja2 Templates** என்பது **Python-க்கு ஒரு Template Engine**.

HTML-ல் Python data-வை dynamic-ஆக காட்ட உதவும் tool தான் Jinja2.

## Jinja2 Syntax

### Variable

```
{{ variable }}
```

Example

```
{{ name }}
```

Output

```
Divya
```


## Jinja2 எப்படி வேலை செய்கிறது?

Python-ல்

```
name = "Divya"
```

இந்த value-யை HTML-க்கு அனுப்புகிறோம்.

HTML-ல்

```
<h1>Welcome {{ name }}</h1>
```

`{{ name }}`

என்ற இடத்தில் Jinja2

```
Divya
```

என்று replace செய்து browser-க்கு அனுப்பும்.

Browser-ல்

```
Welcome Divya
```

என்று தெரியும்.

---

# ஏன் Jinja2 பயன்படுத்துகிறோம்?

### 1. Dynamic Data காட்ட

Python

```
name = "Divya"
age = 22
```

HTML

```
<h1>{{ name }}</h1>
<p>{{ age }}</p>
```

Output

```
Divya
22
```

### 2. Database Data காட்ட

Database-ல்

```
ID  Name
1   Apple
2   Orange
3   Mango
```

Python

```
products = ["Apple", "Orange", "Mango"]
```

HTML

```
<ul>
{% for item in products %}
<li>{{ item }}</li>
{% endfor %}
</ul>
```

Output

```
• Apple
• Orange
• Mango
```

### 3. Conditions எழுத

Python

```
logged_in = True
```

HTML

```
{% if logged_in %}
<h1>Welcome</h1>
{% else %}
<h1>Please Login</h1>
{% endif %}
```

Output

```
Welcome
```
### 4. Repeating Content

100 products இருந்தால்

HTML-ல்

```
<li>Apple</li>
<li>Orange</li>
<li>Mango</li>
```

இப்படி 100 lines எழுத வேண்டாம்.

Jinja2 loop போதும்.

```
{% for product in products %}
<li>{{ product }}</li>
{% endfor %}
```

Jinja2-ல் **dynamic** என்றால், HTML-ல் உள்ள content **ஒரே மாதிரி fixed-ஆக இல்லாமல், Python-லிருந்து வரும் data-க்கு ஏற்ப மாறுவது**.

### Static vs Dynamic

**Static HTML:**

```
<h1>Hello Divya</h1>
```

எப்போதும்:

```
Hello Divya
```

தான் வரும்.

---

### Dynamic Jinja2

Python:

```
name = "Divya"
```

HTML:

```
<h1>Hello {{ name }}</h1>
```

Output:

```
Hello Divya
```

`name`-ஐ மாற்றினால்:

```
name = "Arun"
```

Output:

```
Hello Arun
```

இதுதான் **dynamic**.