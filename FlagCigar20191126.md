# 1. Explain BAM FLAG value： 143

## 答：PAIRED, PROPER_PAIR, UNMAP, MUNMAP, READ2
## 该 read 是成对的 paired reads 中的第二条，paired reads 中每个都正确比对到参考序列上，该 read 及与该 read 成对的 matepair read 没有比对到参考序列上
### 注：ROPER_PAIR 与 UNMAP, MUNMAP 应该是冲突的吧？怎么可以既比对上了，又没有比对上呢？


## 2. Explain BAM FLAG value： 99

    答：PAIRED, PROPER_PAIR, MREVERSE, READ1
	该 read 是成对的 paired reads 中的第一条，paired reads 中每个都正确比对到参考序列上，与该 read 成对的 matepair read 其反向互补序列能够比对到参考序列


## 3. Explain BAM FLAG value：516

    答：UNMAP, QCFAIL
	该 read 没比对到参考序列上，该 read 没有通过质量控制

4. Explain BAM FLAG value： 2064

    答：REVERSE, SUPPLEMENTARY
	该 read 其反向互补序列能够比对到参考序列，补充匹配的 read

5. Explain BAM FLAG value： 147

    答：PAIRED, PROPER_PAIR, REVERSE, READ2

	该 read 是成对的 paired reads 中的第二条，paired reads 中每个都正确比对到参考序列上，该read其反向互补序列能够比对到参考序列

6. Explain BAM CIGAR：14M2D31M

    答：表示该 read 相对于参考序列来说，14 bp 能 match，随后有 2 bp 的 delete，紧接着的 31 bp 能 match

7. Explain BAM CIGAR：3S6M1D5M

    答：表示该 read 相对于参考序列来说，前 3 bp 不能 match，接着 6 bp 能 match，随后有 1 bp 的 delete，之后的 5 bp 能 match

8. Explain BAM CIGAR: 6M14N5M

    答：表示该 read 相对于参考序列来说，前 6 bp 能 match，之后跳过 14 bp ，剩下的 5 bp 能 match

9. Explain BAM CIGAR: 7M5D8M2I14M  (小写：7m5d8m2i14m）

    答：表示该 read 相对于参考序列来说，前 7 bp 能 match，之后有 5 bp 的 delete，随后的 8 bp 能 match，然后发生了 2 bp 的 insert，最后 14 bp 能 match

10. how long is the read with alignment CIGAR of 7M5D8M2I14M

    答：31
