## Child theme

Create a [child theme](http://codex.wordpress.org/Child_Themes) and override Largo default styles using `style.css`

## Modify Largo

1. Modify the LESS files in `less/`
    * If you're working on an existing component, edit the appropriate existing file(s) in `less/inc/`
    * If you're working on a new component, create a new file in `less/inc/` and import that file in `less/style.less`

For example, from the root directory of the Largo repository:

    $ touch less/inc/yournewcomponent.less

Edit `less/inc/yournewcomponent.less`, then in `less/style.css`:

    ...
    @import "inc/yournewcomponent.less";
    ...

2. Recompile the LESS into CSS in `css/`. From the root of the Largo repository, run:

    $ lessc -x less/style.less > css/style.css

## Useful links

- [LESS](http://lesscss.org/)
- [Bootstrap 2.3](http://getbootstrap.com/2.3.2/) (Assumption, based on `fonts/fontello/demo.html`)
