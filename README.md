# analiseDesempenhoJacobi
Trabalho de arquitetura de computadores que tem como objetivo otimizar um código de multiplicação de matrizes

# Configuração da Máquina 1

```
Arquitetura:                             x86_64
Modo(s) operacional da CPU:              32-bit, 64-bit
Address sizes:                           48 bits physical, 48 bits virtual
Ordem dos bytes:                         Little Endian
CPU(s):                                  12
Lista de CPU(s) on-line:                 0-11
ID de fornecedor:                        AuthenticAMD
Nome do modelo:                          AMD Ryzen 5 5600G with Radeon Graphics
Família da CPU:                          25
Modelo:                                  80
Thread(s) per núcleo:                    2
Núcleo(s) por soquete:                   6
Soquete(s):                              1
Step:                                    0
CPU MHz máx.:                            4464,0000
CPU MHz mín.:                            400,0000
BogoMIPS:                                7785.34
Opções:                                  fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl nonstop_tsc cpuid extd_apicid aperfmperf rapl pni pclmulqdq monitor ssse3 fma cx16 sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand lahf_lm cmp_legacy svm extapic cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw ibs skinit wdt tce topoext perfctr_core perfctr_nb bpext perfctr_llc mwaitx cpb cat_l3 cdp_l3 hw_pstate ssbd mba ibrs ibpb stibp vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid cqm rdt_a rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves cqm_llc cqm_occup_llc cqm_mbm_total cqm_mbm_local user_shstk clzero irperf xsaveerptr rdpru wbnoinvd cppc arat npt lbrv svm_lock nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold avic v_vmsave_vmload vgif v_spec_ctrl umip pku ospke vaes vpclmulqdq rdpid overflow_recov succor smca fsrm debug_swap ibpb_exit_to_user

Virtualização:                           AMD-V
cache de L1d:                            192 KiB (6 instances)
cache de L1i:                            192 KiB (6 instances)
cache de L2:                             3 MiB (6 instances)
cache de L3:                             16 MiB (1 instance)
Nó(s) de NUMA:                           1
CPU(s) de nó0 NUMA:                      0-11

Vulnerability Tsx async abort:           Not affected
Vulnerability Vmscape:                   Mitigation; IBPB before exit to userspace
```



## Teste de Validação da Matriz

```bash
./diff-mat.exec 1E-10 X1000.bin saida-teste.bin
```

Verificação
<img width="623" height="171" alt="image" src="https://github.com/user-attachments/assets/983b20ef-726e-487f-974f-7c1d8c00d25a" />

  
Essa saída está dizendo que a sua simulação/cálculo aproximado funcionou perfeitamente e atingiu a precisão exigida.
O programa comparou a matriz que você gerou com a matriz gabarito (exata) e validou o seguinte:
• O parâmetro inserido (1E-10): Você definiu que a tolerância máxima aceitável para o erro era de 1.00 × 10⁻¹⁰ (um valor extremamente pequeno).
• O Erro Absoluto Realizado (|EA|): A diferença real calculada entre a sua matriz aproximada (saida-teste.bin) e a exata (X1000.bin) foi de apenas 4.07 × 10⁻¹¹.
• O resultado [true]: Como o erro real (4.07 × 10⁻¹¹) é menor do que o erro máximo permitido (1.00 × 10⁻¹⁰), o teste passou com sucesso.
