# Script to restart icinga2 and print its state

I built this script since you cannot use this as an alias:

    alias kick_icinga="service icinga2 restart && service icinga2 status"

When you are working on an icinga host you might have to restart icinga2 sometimes.
Then you can use this script and use this alias in your **.bashrc**:

    alias kick_icinga="/opt/scripts/icinga_kicker"

If you don't want to restart the service you might want to use the **icinga_reloader**:

    alias reload_icinga="/opt/scripts/icinga_reloader"

### Usage

Just clone them, move them and chmod them:

    git clone https://github.com/MrAwesomeBro/icinga-kicker.git
    cd icinga-kicker
    mkdir /opt/scripts
    mv icinga_* /opt/scripts/
    chmod +x /opt/scripts/icinga_*

Then set your aliases in you **.bashrc** or **.bash_aliases**:

    alias kick_icinga="/opt/scripts/icinga_kicker"
    alias reload_icinga="/opt/scripts/icinga_reloader"

That's it.
