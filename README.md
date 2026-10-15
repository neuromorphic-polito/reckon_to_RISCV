# reckon_to_RISCV
ReckOn - based AXI IP for integration with RISC-V SoC

- To create .mem files for BRAM initialization, run 

```
make chs-create-memfile LABEL_DELAY=4 DS_PATH=<subdir containing the files>
```

- To generate random weights, run 

```
make chs-gen-weights-w<layer> WGEN_PRE=38 WGEN_POST=38 WGEN_SEED=42
```
`<layer>` can be inp, rec or out. WGEN_SEED is optional.

## License

Unless stated otherwise in the file header, the content of this repository is
Copyright 2026 Michelangelo Barocci, Politecnico di Torino, and is released under:

- **Software** (`src/sw/`): [Apache License 2.0](LICENSE)
  (`SPDX-License-Identifier: Apache-2.0`).
- **Hardware** (`src/hw/`): [Solderpad Hardware License v2.1](LICENSE-SHL)
  (`SPDX-License-Identifier: Apache-2.0 WITH SHL-2.1`). The SHL v2.1 is a
  wraparound license of the Apache License 2.0, which is therefore also required
  to read and apply it.

Third-party files keep their original license and copyright, as stated in their headers:

- `src/hw/rtl/reckon/`: [ReckOn](https://github.com/ChFrenkel/ReckOn),
  Copyright University of Zurich, `Apache-2.0 WITH SHL-2.1`.

- `src/hw/rtl/BRAM_1port_we.v`, `src/hw/rtl/BRAM_2ports_we.v`: based on the AMD/Xilinx Vivado language templates.

- `/src/sw/dataset_ESA` contains the dataset used for the demonstrator if the ReckOn accelerator with the Cheshire SoC. The dataset has been created starting from the [ESA-ADB](https://github.com/kplabs-pl/ESA-ADB), that we encoded starting from a subset of channels containing anomaly readings.
