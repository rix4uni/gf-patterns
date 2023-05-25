# gf-patterns
grep parameters (allparam,idor,lfi,rce,redirect,sqli,ssrf,ssti,xss)

# Setup
```
go install github.com/tomnomnom/gf@latest && git clone https://github.com/rix4uni/gf-patterns.git ~/.gf
```

# Patterns Files
The pattern definitions are stored in ~/.gf as little JSON files that can be kept under version control:

**gf allparam**
```bash
▶ cat ~/.gf/allparam.json

{
    "flags": "-E",
    "pattern": "[?].*[&]?"
}
```

**gf idor**
```bash
▶ cat ~/.gf/idor.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(id=|user=|account=|number=|order=|no=|doc=|key=|email=|group=|profile=|edit=|report=)"
}
```

**gf lfi**
```bash
▶ cat ~/.gf/lfi.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(file=|document=|folder=|root=|path=|pg=|style=|pdf=|template=|php_path=|doc=|page=|name=|cat=|dir=|action=|board=|date=|detail=|download=|prefix=|include=|inc=|locate=|show=|site=|type=|view=|content=|layout=|mod=|conf=|url=)"
}
```

**gf rce**
```bash
▶ cat ~/.gf/rce.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(daemon=|upload=|dir=|download=|log=|ip=|cli=|cmd=|exec=|command=|execute=|ping=|query=|jump=|code=|reg=|do=|func=|arg=|option=|load=|process=|step=|read=|function|req=|feature=|exe=|module=|payload=|run=|print=)"
}
```

**gf redirect**
```bash
▶ cat ~/.gf/redirect.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(Lmage_url=|Open=|callback=|cgi-bin/redirect.cgi|cgi-bin/redirect.cgi?|checkout=|checkout_url=|continue=|data=|dest=|destination=|dir=|domain=|feed=|file=|file_name=|file_url=|folder=|folder_url=|forward=|from_url=|go=|goto=|host=|html=|image_url=|img_url=|load_file=|load_url=|login?to=|login_url=|logout=|navigation=|next=|next_page=|out=|page=|page_url=|path=|port=|redir=|redirect=|redirect_to=|redirect_uri=|redirect_url=|reference=|return=|returnTo=|return_path=|return_to=|return_url=|rt=|rurl=|show=|site=|target=|to=|uri=|url=|val=|validate=|view=|window=)"
}
```

**gf sqli**
```bash
▶ cat ~/.gf/sqli.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(id=|select=|report=|role=|update=|query=|user=|name=|sort=|where=|search=|params=|process=|row=|view=|table=|from=|sel=|results=|sleep=|fetch=|order=|keyword=|column=|field=|delete=|string=|number=|filter=)"
}
```

**gf ssrf**
```bash
▶ cat ~/.gf/ssrf.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(access=|admin=|dbg=|debug=|edit=|grant=|test=|alter=|clone=|create=|delete=|disable=|enable=|exec=|execute=|load=|make=|modify=|rename=|reset=|shell=|toggle=|adm=|root=|cfg=|dest=|redirect=|uri=|path=|continue=|url=|window=|next=|data=|reference=|site=|html=|val=|validate=|domain=|callback=|return=|page=|feed=|host=|port=|to=|out=|view=|dir=|show=|navigation=|open=|file=|document=|folder=|pg=|php_path=|style=|doc=|img=|filename=)"
}
```

**gf ssti**
```bash
▶ cat ~/.gf/ssti.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(template=|preview=|id=|view=|activity=|name=|content=|redirect=)"
}
```

**gf xss**
```bash
▶ cat ~/.gf/xss.json

{
    "flags": "-E",
    "pattern": "(\\?|&)(p=|q=|s=|search=|lang=|keyword=|query=|page=|keywords=|year=|view=|email=|type=|name=|callback=|jsonp=|api_key=|api=|password=|email=|emailto=|token=|username=|csrf_token=|unsubscribe_token=|id=|item=|page_id=|month=|immagine=|list_type=|url=|terms=|categoryid=|key=|l=|begindate=|enddate=)"
}
```
