# Run Load Test With Static Page

To reproduce runs this script:
```
ab -c 1 -t 60 http://localhost:6868/
```

Results:


| C | LA1   | LA5    | LA15 | RAM Avg NodeJS | RAM Avg MySQL | CPU Avg NodeJS App | CPU Avg MySQL | 
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 0.242 | 0.173 | 0.144 | 1.73%    | 3.01 %   |  64.37% | 0.18% | 
| 20 | 0.397 | 0.298 | 0.218 | 1.73%   |  3.01 %  |  10.5% | 0.137% |
| 50 | 0.405 | 0.370 | 0.300 | 1.74% | 3.01% |  6.10% | 0.144% | 

# Run Load Test Against a Page With DB Request

To reproduce runs this script:
```
 ab -c 1 -t 60 http://localhost:6868/api/tutorials
```

Results:

| C | LA1   | LA5    | LA15 | RAM Avg NodeJS | RAM Avg MySQL | CPU Avg NodeJS App | CPU Avg MySQL | 
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 0.799 | 0.442 | 0.317 | 3.01% | 1.75% | 44.6% | 7.78% | 
| 20 | 1.34 | 0.652 | 0.405 | 1.77% | 3.02% | 68.2% | 13.5% | 
| 50 | 1.32 | 0.817 | 0.511 | 1.76% | 3.02% | 77.0% | 16.3% | 

