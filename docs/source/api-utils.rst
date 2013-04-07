======================
:mod:`blackhole.utils`
======================

.. module:: blackhole.utils
    :platform: Unix
    :synopsis: Utils
.. moduleauthor:: Kura <kura@kura.io>

A utility module used for
methods and features that do not belong in
their own module.

blackhole.utils
===================

.. function:: setgid()

    Change our existing group.

    Used to drop from root privileges down to a less
    privileged group.

    MUST be called BEFORE setuid, not after.

.. function:: setuid()

    Change our existing user.

    Used to drop from root privileges down to a less
    privileged user

    MUST be called AFTER setgid, not before.

.. function:: terminate(signum, frame)

    Terminate the parent process and send signals
    to shut down it's children

    Iterates over the child pids in the frame
    and sends the SIGTERM signal to shut them
    down.