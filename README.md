About
=====

A simple RC car kit firmware and simple bash script to control it via curl commands.

How to build
------------

See [this Spark Docs page](http://docs.spark.io/#/shields/spark-rc-car-kit) for details of how to build

- [Robot Assembly Guide](http://www.dfrobot.com/wiki/index.php/3PA_Assembly_Guide_%28SKU:ROB0005%29)
- [Advanced Robot Assembly Guide](http://www.dfrobot.com/wiki/index.php?title=Basic_Kit_for_Turtle_2WD_SKU:ROB0118)
- [Arduino Motor Shield](http://www.dfrobot.com/wiki/index.php?title=Arduino_Motor_Shield_%28L298N%29_%28SKU:DRI0009%29)
- [Controls the rc-car demo via tweets](https://github.com/spark/rc-car-twitter)
- [Spark RC Car iOS app](https://github.com/spark/rc-car-ios)

How to Use
----------

The bash script is essentially a loop that listens for keyboard input and invokes API
commands corresponding with forware, backword, left, right, and stop instructions.

### Open up a bash shell + go to controllers dir

    cd rc_car/controllers

### Set 2 env vars:

    export SPARK_CORE_DEVICE_ID="PUT_YOUR_DEVICE_ID_HERE!!!! i.e. acefdc000a01a411587f65d5"
    export SPARK_CORE_ACCESS_TOKEN="PUT_YOUR_ACCESS_TOKEN_HERE!!!! i.e. 3651b73e632b86881d47c65e7b0f59d511e97520"

### Load some bash functions into the current shell:

    source application.sh

### Then run the input loop function:

    rc_while
