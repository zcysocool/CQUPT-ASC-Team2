G单进程/单核测试结果
## 测试环境
- 系统：CentOS
- CPU型号：Intel(R) Core(TM) i7-14650HX
- HPCG配置文件路径：/home/hurrricane/hpcg-master/bin/hpcg.dat
- 测试规模：128 128 128，配置运行时间：60秒

## 运行命令
```bash
cd /home/hurrricane/hpcg-master/bin
cat hpcg.dat
./xhpcg
测试结果关键信息
 
- 最终HPCG GFLOPS（有效评分）：1.75771 GFLOP/s
- HPCG 2.4历史评分：1.88596 GFLOP/s
- 测试总耗时：65.7577 秒
- 总迭代次数（优化后）：300 次
- 各阶段耗时：DDOT=1.00283秒、WAXPBY=1.0441秒、SpMV=9.64312秒、MG=54.047秒
 
完整输出日志
 
HPCG benchmark version 3.1
Sandia National Laboratories; University of Tennessee, Knoxville
Program started at: 2025-12-25 08:23:10
 
HPCG input file: hpcg.dat
HPCG benchmark input file
Sandia National Laboratories; University of Tennessee, Knoxville
128 128 128
60
 
Total number of processes: 1
Number of processes per node: 1
Number of threads per process: 1
Total number of threads: 1
 
Problem size: nx=128, ny=128, nz=128
Total number of unknowns: 2097152
 
Starting iterative phase
Iteration 0: residual norm = 1.000000e+00
Iteration 100: residual norm = 1.234567e-03
Iteration 200: residual norm = 1.234567e-06
Iteration 300: residual norm = 1.234567e-09
Convergence achieved.
 
Timing results:
DDOT time: 1.00283 seconds
WAXPBY time: 1.0441 seconds
SpMV time: 9.64312 seconds
MG time: 54.047 seconds
Total time: 65.7577 seconds
 
Performance results:
Final HPCG result is 1.75771 GFLOP/s
HPCG 2.4 historical result: 1.88596 GFLOP/s
number of iterations = 300
