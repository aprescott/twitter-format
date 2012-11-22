# About

What would a man page for Twitter's syntax look like?

# tweet-format(7)

## SYNOPSIS

_message_<br>
**@**_user_ _message_<br>

**.@**_user_ _message_<br>
**RT** **@**_user_ _message_<br>
**OH:** _quote_<br>
**#**_hashtag_

## DESCRIPTION

Twitter supports simple messages as sequences of characters. In addition to the
syntax for replying to a tweet poster, there are various conventions for
non-reply messages.

## PLAIN TWEETS

_message_

The core message is a string of characters which does not begin with **@**.

There are additional conventions within a message itself. See the section on
[MESSAGE CONVENTIONS][].

## @-REPLIES

**@**_user_ _message_

If _message_ is preceded with **@**_user_, the tweet will be visible to the
user with account name _user_ and any users who are following both you (as the
sender) and _user_.

## MENTION-REPLY

**.@**_user_ _message_

If the leading **@** is preceded by any other character, commonly **.**, the
message is no longer an @reply tweet and will be visible to anyone following
you (as the sender).

This convention is frequently used to reply to _user_'s tweet while making your
reply visible to others, or to refer to _user_ in a "new" tweet without causing
its contents to become invisible to your follows.

## RETWEETING

**RT** **@**_user_ _message_

If **@** is preceded by **RT**, this is a convention indicating that you are
_retweeting_ someone's _message_. Doing so makes _message_ available to all
your followers.

## OVERHEARD SENTENCES

**OH:** _quote_<br>
**OH** **@**_user_**:** _quote_

If _message_ begins with **OH:**, then what follows is a _quote_ (which may or
may not be wrapped in actual quotation marks) which has been **O**ver**H**eard.

Sometimes the user is included, such as:

**OH** **@**_user_**:** _quote_

This means, of course, that _user_ was overheard saying _quote_.

## MESSAGE CONVENTIONS

**@**_usermention_

_message_ can itself contain **@**_user_ references, called _mentions_, which
_user_ can see.

**#**_hashtag_

Any words in _message_ which begin with **#** are called _hashtags_ and are
used to tag the message as related to some particular topic.

## EXAMPLES

* **Simple message**:
  I'm on twitter!

* **Reply**:
  @twitter agreed.

* **Overheard**:
  OH: "140 characters? That'll never take off."

* **Overheard with a user mention**:
  OH @typed: "A man page? For Twitter? That's stupid."

* **Retweet**:
  RT @jack just setting up my twttr

* **Hashtag**:
  Writing a man page for tweets. #pointless

## ABOUT THIS MAN PAGE

This `tweet-format(7)` man page was written for fun by [Adam Prescott](http://aprescott.com/). You can find its source on [GitHub](https://github.com/aprescott/twitter-format).

It is released under the terms of the MIT License with the copyright notice:

Copyright (c) 2012 Adam Prescott &lt;adam@aprescott.com&gt;
