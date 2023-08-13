# Erasure Coding Performance Comparison: Reed-Solomon vs. Cauchy Reed-Solomon

This project aims to compare the performance of Reed-Solomon encoding and Cauchy Reed-Solomon encoding algorithms in terms of encoding and decoding speeds. The experiments were conducted using the [klauspost/reedsolomon](https://github.com/klauspost/reedsolomon) library implemented in Go. The results were then compared with the findings presented in the paper titled "A Performance Evaluation and Examination of {Open-Source} Erasure Coding Libraries for Storage," presented in FAST '09 by James S. Plank.

## Experiments

### Experiment 1: Increasing Data Block Size

In this experiment, the effect of increasing the data block size on the encoding performance was examined. The initial performance shows an increase, followed by stabilization. The optimal block size for Cauchy RS was found to be 7500 KB (8000 Mbps), while for RS, it was 5000 KB (7000 Mbps).

### Experiment 2: Increasing Parity Blocks

The second experiment involved increasing the number of parity blocks and analyzing its impact on performance. It was observed that performance decreases with the increase in parity blocks. Moreover, the performance of Cauchy RS was found to be superior to Reed-Solomon.

### Experiment 3: Decoding Speed Comparison

This experiment focused on comparing the decoding speeds of Cauchy RS and Reed-Solomon. Cauchy RS demonstrated better decoding speed than Reed-Solomon.

## Observations

- Cauchy RS consistently outperforms Reed-Solomon in terms of performance.
- Larger block sizes can enhance encoding speeds.
- An increase in parity blocks can lead to a decrease in encoding speeds.
- Notable performance drops were observed, which can be attributed to collisions in L1-Cache.

## Conclusion

The findings suggest that default values of erasure coding algorithms might not yield optimal performance. Cauchy Reed-Solomon encoding demonstrated better performance than Reed-Solomon encoding, both in terms of encoding and decoding files, as expected. This comparison underscores the significance of algorithm choice in achieving efficient erasure coding. By conducting these experiments and comparing the results against a recognized paper, this project contributes to a better understanding of erasure coding algorithm performance and its implications for storage systems.
