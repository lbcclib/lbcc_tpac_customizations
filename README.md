# tpac_customizations
Some changes we've made to our Evergreen OPAC

Most of these go in `/openils/var/templates/opac`, but the `icon_formats` directory should go in `/openils/var/web/images/format_icons`

The following commands -- run as `opensrf` -- should get all our customizations into an existing Evergreen installation:

    cd /openils/var/templates/opac
    git init
    echo "*" >> .gitignore
    git remote add origin https://github.com/lbcclib/tpac_customizations
    git pull origin master
    git reset --hard origin/master
    cp -R icon_format/* /openils/var/web/images/format_icons/icon_format/
