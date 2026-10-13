import json, os, urllib.request, datetime, math
from pathlib import Path
USER=os.getenv('LEETCODE_USERNAME','anie25')
query={'query':'query calendar($username: String!) { matchedUser(username: $username) { userCalendar { submissionCalendar } } }','variables':{'username':USER}}
req=urllib.request.Request('https://leetcode.com/graphql/',data=json.dumps(query).encode(),headers={'Content-Type':'application/json','User-Agent':'Mozilla/5.0','Referer':'https://leetcode.com/'})
with urllib.request.urlopen(req,timeout=25) as r: data=json.load(r)
user=data.get('data',{}).get('matchedUser')
if not user: raise RuntimeError('LeetCode calendar not available for '+USER)
calendar=json.loads(user['userCalendar']['submissionCalendar'] or '{}')
counts={datetime.datetime.fromtimestamp(int(k),datetime.timezone.utc).date():int(v) for k,v in calendar.items()}
today=datetime.datetime.now(datetime.timezone.utc).date()
start=today-datetime.timedelta(days=364)
start-=datetime.timedelta(days=(start.weekday()+1)%7)
weeks=math.ceil(((today-start).days+1)/7)
W=weeks*14+40; H=7*14+66
Path('dist').mkdir(exist_ok=True)
for dark in (False,True):
 bg='#0d1117' if dark else '#ffffff'; fg='#e6edf3' if dark else '#24292f'; zero='#161b22' if dark else '#ebedf0'; colors=['#0e4429','#006d32','#26a641','#39d353'] if dark else ['#9be9a8','#40c463','#30a14e','#216e39']; snake='#ffcc00' if dark else '#ed8936'
 cells=[]; active=[]
 for x in range(weeks):
  for y in range(7):
   day=start+datetime.timedelta(days=x*7+y)
   if day>today:continue
   n=counts.get(day,0); color=zero if not n else colors[min(3,int(math.log2(n+1))//2)]
   px=20+x*14;py=42+y*14
   cells.append(f'<rect x="{px}" y="{py}" width="10" height="10" rx="2" fill="{color}"/>')
   if n:active.append((px+5,py+5))
 # Animated snake path follows submission cells, ordered from older to newer.
 # Avoid excessive SVG size by sampling at most 140 points.
 if len(active)>140:active=[active[round(i*(len(active)-1)/139)] for i in range(140)]
 if not active:active=[(20,47)]
 points=';'.join(f'{x},{y}' for x,y in active)
 dur=max(10,len(active)*0.13)
 svg=f'''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 {W} {H}" role="img" aria-label="Animated LeetCode submission activity for {USER}"><rect width="100%" height="100%" rx="12" fill="{bg}"/><text x="20" y="24" fill="{fg}" font-family="Arial,sans-serif" font-size="14" font-weight="bold">LeetCode submissions · {USER}</text>{''.join(cells)}<circle r="6" fill="{snake}" stroke="{bg}" stroke-width="1.5"><animate attributeName="cx" values="{';'.join(str(x) for x,y in active)}" dur="{dur}s" repeatCount="indefinite"/><animate attributeName="cy" values="{';'.join(str(y) for x,y in active)}" dur="{dur}s" repeatCount="indefinite"/></circle><text x="20" y="{H-10}" fill="{fg}" font-family="Arial,sans-serif" font-size="11">Daily submissions · Updated automatically</text></svg>'''
 Path('dist/leetcode-snake'+('-dark' if dark else '')+'.svg').write_text(svg)
print('Generated SVGs for',USER,'with',len(active),'active dates')
