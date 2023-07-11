Let's set up a few things so the bot can detect new boosters properly.

!!! Caution "Detecting members who boosted before the bot was added:"

    By default, the bot adds existing boosters to the booster database with `1x boost`, but there is NO WAY for the bot (or anyone else) to see how many times someone has boosted.
    However, you can edit anyone's number of boosts with [Booster Bot Premium](https://boosterbot.xyz/premium).

1. Enable Discord's system boost message -- to detect boosts.
2. Give the bot read message permission in the system channel -- to see system messages.
3. Send messages & embed links perms in `greet-channel` & `log-channel` (optional).

Server settings screenshot:
![Server settings screenshot](./images/server-settings.png)

However, there are a few things to note here -

!!! info "

    `1.` In some cases, someone boosts two times rapidly (1 by 1), and if the bot has any occasional lag simultaneously, the bot will count that as one boost instead of 2.

    `2.` If you've not set up the bot correctly OR the bot had any downtime, you can add missed booster with the `bb boosters add @user` command, and the booster will be added with `1x boost`.

---

Now that you've set up the new boost detection let's continue with the boost removal part.

-   Bot will detect that someone removed boost only if Discord's default booster role is removed from them.
    This means it'll only detach when the booster removes all its active boosts from the server.
-   Ex - if someone had two boosts and removed 1, no one (including the bot) can detach if they pulled the boost. It is something that Discord needs to improve.

---

With all your information on how the bot works, we can begin with greeting & logging.

**Greet Message:**

Thank you. Message for boosts can be set up with the `bb greet` command.
You can check more about that command [here](/commands/greet) OR type `bb help greet,` the bot will show you all available options to customize the message.

**Log Message:**

Updates on boost added/removed can be set up with the `bb setup log-channel` OR `bb setup log-events` command.
As the bot offers many things to boosters, it can log everything you need with the `log-channel` command in 1 channel. You can use ' log-events ' if you need a separate track for separate events OR you only want specific events like boost-added logs.
