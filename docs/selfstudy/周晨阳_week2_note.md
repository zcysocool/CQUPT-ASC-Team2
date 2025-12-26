 Week 2 Learning Record
Completed Tasks：
This week, I focused on the HPCG (High Performance Conjugate Gradient) benchmark test. After debugging, I successfully ran the single-process test in Linux, obtained the core result of `1.75771 GFLOP/s`, and archived the required document and screenshot. I also mastered WinSCP file transfer and basic GitHub repository operations.

Key Challenges & Troubleshooting：
Two main issues took time:
1. Environment configuration: Unfamiliar with Linux network settings caused SSH port listening failures and WinSCP timeouts, resolved by updating the virtual machine IP and disabling the firewall.
2. HPCG timeout: Oversized grid parameters in `hpcg.dat` led to timeouts; adjusting `nx`/`ny`/`nz` to match hardware fixed it.

Unfamiliar Concepts & Follow-up Plans：
I lack deep understanding of HPCG parameter tuning (e.g., grid size/iteration adjustments for different hardware). Next, I’ll consolidate Linux environment skills, study HPCG’s official docs, and practice Git/PR operations for smooth assignment submission.
