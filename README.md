# Plotting Ribbons

Dependencie: 
[fogleman/ribbon](https://github.com/fogleman/ribbon

```bash
git clone git@github.com:piebro/ribbon.git
cd ribbon

names="7D7V 7AZB 6V13 6V2K"
names="7DDN 7DDD 6ZUL 6ZY2 6ZYE"

names="7DDN 7DDD 6ZUL 6ZY2 6ZYE"
for name in $names; do echo $name; go run cmd/lines/main.go $name | python -c "import sys;paths=['M{},{} L{},{}'.format(*[(float(f)+1)*500 for f in p.replace('\n','').replace(';',',').split(',')]) for p in sys.stdin];f=open('$name.svg','w');f.write(('\n').join(['<svg xmlns=\"http://www.w3.org/2000/svg\" height=\"30.0cm\" viewBox=\"0 0 1000 1000\" width=\"30.0cm\">','<g stroke=\"#00f\">','<path d=\"']+paths+['\"/>','</g>','</svg>']));f.close()"; done


# scale to the right format
vpype read 6PLB.svg scaleto 190mm 190mm linemerge linesimplify -t 0.05mm write --page-format 200x200mm --center plot.svg

# generate preview with axicli
axicli plot.svg -vg3 --report_time -o preview.svg --model 2

# plot with axicli
axicli plot.svg --pen_pos_down 40 --speed_pendown 10 --model 2; axicli -m align


vpype read 7AZB.svg scaleto 220mm 220mm linemerge linesimplify -t 0.05mm write --page-format 405x297mm --center plot.svg
```

Find more proteins at: <http://www.rcsb.org/search?q=*>

Dataset?