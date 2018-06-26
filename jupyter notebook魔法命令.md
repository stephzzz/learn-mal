
# Jupter Nootbook高级-魔法命令

## %run


```python
%run py-pro/first.py
```

    1
    

## %timeit多次測試運行時間


```python
%timeit L = [i**2 for i in range(1000)]
```

    309 µs ± 3.46 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
    


```python
%timeit L = [i**2 for i in range(10000)]
```

    3.11 ms ± 39.6 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
    


```python
%%timeit
L = []
for i in range(1000):
    L.append(i**2)
```

    351 µs ± 3.44 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
    

## %time單次時間



```python
%time L = [i**2 for i in range(1000)]
```

    Wall time: 0 ns
    


```python
%%time
L = []
for i in range(1000):
    L.append(i**2)
```

    Wall time: 997 µs
    


```python
import random
L = [random.random() for i in range(100000)]
%timeit L.sort()
```

    1.37 ms ± 43.6 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
    

## 其他魔法命令


```python
%lsmagic
```




    Available line magics:
    %alias  %alias_magic  %autocall  %automagic  %autosave  %bookmark  %cd  %clear  %cls  %colors  %config  %connect_info  %copy  %ddir  %debug  %dhist  %dirs  %doctest_mode  %echo  %ed  %edit  %env  %gui  %hist  %history  %killbgscripts  %ldir  %less  %load  %load_ext  %loadpy  %logoff  %logon  %logstart  %logstate  %logstop  %ls  %lsmagic  %macro  %magic  %matplotlib  %mkdir  %more  %notebook  %page  %pastebin  %pdb  %pdef  %pdoc  %pfile  %pinfo  %pinfo2  %popd  %pprint  %precision  %profile  %prun  %psearch  %psource  %pushd  %pwd  %pycat  %pylab  %qtconsole  %quickref  %recall  %rehashx  %reload_ext  %ren  %rep  %rerun  %reset  %reset_selective  %rmdir  %run  %save  %sc  %set_env  %store  %sx  %system  %tb  %time  %timeit  %unalias  %unload_ext  %who  %who_ls  %whos  %xdel  %xmode
    
    Available cell magics:
    %%!  %%HTML  %%SVG  %%bash  %%capture  %%cmd  %%debug  %%file  %%html  %%javascript  %%js  %%latex  %%markdown  %%perl  %%prun  %%pypy  %%python  %%python2  %%python3  %%ruby  %%script  %%sh  %%svg  %%sx  %%system  %%time  %%timeit  %%writefile
    
    Automagic is ON, % prefix IS NOT needed for line magics.




```python
%run?
```
