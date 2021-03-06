# Device tree

`platform_device.c` together with its kernel and QEMU forks contains a minimal runnable example.

Good format descriptions:

- <https://www.raspberrypi.org/documentation/configuration/device-tree.md>

Minimal example

    /dts-v1/;

    / {
        a;
    };

Check correctness with:

    dtc a.dts

Separate nodes are simply merged by node path, e.g.:

    /dts-v1/;

    / {
        a;
    };

    / {
        b;
    };

then `dtc a.dts` gives:


    /dts-v1/;

    / {
            a;
            b;
    };
