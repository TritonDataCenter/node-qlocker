<!--
    This Source Code Form is subject to the terms of the Mozilla Public
    License, v. 2.0. If a copy of the MPL was not distributed with this
    file, You can obtain one at http://mozilla.org/MPL/2.0/.
-->

<!--
    Copyright 2019 Joyent, Inc.
-->

# node-qlocker: Ordered file locks

The qlocker module is intended to replace locker.js that has been copied around
many Joyent repositories.  Known locations are:

    eng/tools/buildimage/lib/imgadm/lib/locker.js
    sdc-cn-agent/node_modules/locker.js
    sdc-firewaller-agent/deps/fw-overlay/lib/locker.js
    sdc-firewaller-agent/deps/fw/lib/locker.js
    sdcadm/lib/locker.js
    smartos-live/src/fw/lib/locker.js
    smartos-live/src/vm/node_modules/locker.js

There already exists node-locker in the npm registry, so a new name was
required.  For intraprocess locking, a queue is maintained - hence qlocker.  A
better name must exist.

Future commits will add code and a proper readme.
