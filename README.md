# CSS Framework

This is the [CodyFrame CSS Framework](https://codyhouse.co) I used for my [portfolio website](https://www.robotsaint.com).
You can read more about the framework [here](https://codyhouse.co/ds/docs/framework).

# Quick start
Create a style.scss file and import the CodyFrame files:

````python
  @use 'reset'; // ← reset
  @use 'config' as *; // ← customize the framework
  
  // ↓ copy & modify these templates locally
  @use 'typography';
  @use 'icons';
  @use 'buttons';
  @use 'forms';
  
  // ↓ import here the CodyHouse components
  @use 'components/_1_header' as *;
  @use 'components/_1_footer' as *;
  // ...
  
  @use 'util'; // ← utility classes
````
The _config.scss file is used to customize the framework (i.e., to edit the [breakpoints](https://codyhouse.co/ds/docs/framework/breakpoints) or to modify the [spacing scale](https://codyhouse.co/ds/docs/framework/spacing)).

Here's a list of all possible configurations:
````
    @use 'config' as * with (
    $util-prefix: '',
    $breakpoints: (
      'xs': '32rem',
      'sm': '48rem',
      'md': '64rem',
      'lg': '80rem',
      'xl': '90rem'
    ),
    $grid-columns: 12,
    $spacing: (
      '4xs': '0.125rem',
      '3xs': '0.25rem',
      '2xs': '0.5rem',
      'xs': '0.75rem',
      'sm': '1rem',
      'md': '1.5rem',
      'lg': '2.25rem',
      'xl': '3.5rem',
      '2xl': '5.75rem',
      '3xl': '9.25rem',
      '4xl': '15rem'
    ),
    $font-family: (
      'primary': 'system-ui, sans-serif'
    ),
    $font-size: (
      'xs': '0.6875rem',
      'sm': '0.8125rem',
      'base': '1rem',
      'md': '1.1875rem',
      'lg': '1.4375rem',
      'xl': '1.75rem',
      '2xl': '2.0625rem',
      '3xl': '2.5rem',
      '4xl': '3rem'
    ),
    $line-height: (
      'xs': '1.1',
      'sm': '1.2',
      'md': '1.4',
      'lg': '1.58',
      'xl': '1.72'
    ),
    $colors: (
      'default': (
        'primary': (
          'darker': '250, 84%, 38%',
          'dark': '250, 84%, 46%',
          'base': '250, 84%, 54%',
          'light': '250, 84%, 60%',
          'lighter': '250, 84%, 67%'
        ),
        'accent': (
          'darker': '342, 89%, 38%',
          'dark': '342, 89%, 43%',
          'base': '342, 89%, 48%',
          'light': '342, 89%, 56%',
          'lighter': '342, 89%, 62%'
        ),
        'black': (
          'base': '230, 13%, 9%'
        ),
        'white': (
          'base': '0, 0%, 100%'
        ),
        'warning': (
          'darker': '35, 79%, 48%',
          'dark': '35, 79%, 56%',
          'base': '35, 79%, 66%',
          'light': '35, 79%, 74%',
          'lighter': '35, 79%, 82%'
        ),
        'success': (
          'darker': '170, 78%, 26%',
          'dark': '170, 78%, 31%',
          'base': '170, 78%, 36%',
          'light': '170, 78%, 42%',
          'lighter': '170, 78%, 47%'
        ),
        'error': (
          'darker': '342, 89%, 38%',
          'dark': '342, 89%, 43%',
          'base': '342, 89%, 48%',
          'light': '342, 89%, 56%',
          'lighter': '342, 89%, 62%'
        ),
        'bg': (
          'darker': '240, 4%, 90%',
          'dark': '240, 4%, 95%',
          'base': '0, 0%, 100%',
          'light': '0, 0%, 100%',
          'lighter': '0, 0%, 100%'
        ),
        'contrast': (
          'lower': '240, 4%, 85%',
          'low': '240, 4%, 65%',
          'medium': '225, 4%, 47%',
          'high': '230, 7%, 23%',
          'higher': '230, 13%, 9%'
        )
      ),
      'dark': (
        'primary': (
          'darker': '250, 100%, 60%',
          'dark': '250, 100%, 64%',
          'base': '250, 100%, 69%',
          'light': '250, 100%, 72%',
          'lighter': '250, 100%, 76%'
        ),
        'accent': (
          'darker': '342, 92%, 41%',
          'dark': '342, 92%, 47%',
          'base': '342, 92%, 54%',
          'light': '342, 92%, 60%',
          'lighter': '342, 92%, 65%'
        ),
        'black': (
          'base': '230, 13%, 9%'
        ),
        'white': (
          'base': '0, 0%, 100%'
        ),
        'warning': (
          'darker': '35, 79%, 48%',
          'dark': '35, 79%, 56%',
          'base': '35, 79%, 66%',
          'light': '35, 79%, 74%',
          'lighter': '35, 79%, 82%'
        ),
        'success': (
          'darker': '170, 78%, 26%',
          'dark': '170, 78%, 31%',
          'base': '170, 78%, 36%',
          'light': '170, 78%, 42%',
          'lighter': '170, 78%, 47%'
        ),
        'error': (
          'darker': '342, 92%, 41%',
          'dark': '342, 92%, 47%',
          'base': '342, 92%, 54%',
          'light': '342, 92%, 60%',
          'lighter': '342, 92%, 65%'
        ),
        'bg': (
          'darker': '232, 7%, 8%',
          'dark': '233, 8%, 11%',
          'base': '232, 11%, 15%',
          'light': '233, 8%, 19%',
          'lighter': '232, 7%, 22%'
        ),
        'contrast': (
          'lower': '240, 6%, 26%',
          'low': '240, 3%, 41%',
          'medium': '231, 3%, 57%',
          'high': '240, 5%, 82%',
          'higher': '240, 100%, 99%'
        )
      )
    ),
    $aspect-ratio: (16 9, 3 2, 4 3, 5 4, 1 1, 4 5, 3 4, 2 3, 9 16),
    $media-wrapper: (16 9, 3 2, 4 3, 1 1),
    $width: (
      '4xs': '0.25rem',
      '3xs': '0.5rem',
      '2xs': '0.75rem',
      'xs': '1rem',
      'sm': '1.5rem',
      'md': '2rem',
      'lg': '3rem',
      'xl': '4rem',
      '2xl': '6rem',
      '3xl': '8rem',
      '4xl': '16rem',
      0: '0',
      10\%: '10%',
      20\%: '20%',
      25\%: '25%',
      30\%: '30%',
      33\%: '33%',
      40\%: '40%',
      50\%: '50%',
      60\%: '60%',
      70\%: '70%',
      75\%: '75%',
      80\%: '80%',
      90\%: '90%',
      100\%: '100%'
    ),
    $height: (
      '4xs': '0.25rem',
      '3xs': '0.5rem',
      '2xs': '0.75rem',
      'xs': '1rem',
      'sm': '1.5rem',
      'md': '2rem',
      'lg': '3rem',
      'xl': '4rem',
      '2xl': '6rem',
      '3xl': '8rem',
      '4xl': '16rem',
      0: '0',
      10\%: '10%',
      20\%: '20%',
      25\%: '25%',
      30\%: '30%',
      33\%: '33%',
      40\%: '40%',
      50\%: '50%',
      60\%: '60%',
      70\%: '70%',
      75\%: '75%',
      80\%: '80%',
      90\%: '90%',
      100\%: '100%'
    ),
    $max-width: (
      '3xs': '20rem',
      '2xs': '26rem',
      'xs': '32rem',
      'sm': '48rem',
      'md': '64rem',
      'lg': '80rem',
      'xl': '90rem'
    ),
    $container-margin-x: var(--space-md),
    $box-shadow: (
      'ring': '0 0 0 1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.05)',
      'xs': '0 0 0 1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.02), 0 1px 3px -1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.2)',
      'sm': '0 0.3px 0.4px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.02), 0 0.9px 1.5px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.045), 0 3.5px 6px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.09)',
      'md': '0 0.9px 1.25px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.025), 0 3px 5px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.05), 0 12px 20px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.09)',
      'lg': '0 1.2px 1.9px -1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.01), 0 3px 5px -1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.015), 0 8px 15px -1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.05), 0 28px 40px -1px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.1)',
      'xl': '0 1.5px 2.1px -6px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.009), 0 3.6px 5.2px -6px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.0115), 0 7.3px 10.6px -6px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.0125), 0 16.2px 21.9px -6px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.025), 0 46px 60px -6px hsla(var(--color-black-h), var(--color-black-s), var(--color-black-l), 0.15)'
    ),
    $inner-glow: (
      'glow': 'inset 0 0 0.5px 1px hsla(var(--color-white-h), var(--color-white-s), var(--color-white-l), 0.075)',
      'glow-top': 'inset 0 1px 0.5px hsla(var(--color-white-h), var(--color-white-s), var(--color-white-l), 0.075)'
    ),
    $border-radius: (
      'sm': '0.1875em',
      'md': '0.375em',
      'lg': '0.75em'
    ),
    $z-index: (
      'header': '3',
      'popover': '5',
      'fixed-element': '10',
      'overlay': '15'
    )
  );
````
If you prefer working with CSS (without a preprocessor)
````
  @import 'https://unpkg.com/codyframe/main/css/reset.css'; /* ← reset */
  
  /* ↓ copy these templates from Github & modify them locally */
  @import 'typography.css';
  @import 'icons.css';
  @import 'buttons.css';
  @import 'forms.css';
  
  /* ↓ import here the CodyHouse components */
  @import 'components/_1_header.css';
  @import 'components/_1_footer.css';
  /* ... */
  
  @import 'https://unpkg.com/codyframe/main/css/util.css'; /* ← utility classes */
````
# Node module
To install CodyFrame as node module:
````bash
  # using npm
  npm i codyframe
  
  # using Yarn
  yarn add codyframe
````
If you install CodyFrame as node module, import the reset, config, and util modules from the node package...

````
  @use '../../../node_modules/codyframe/main/scss/reset';
  @use '../../../node_modules/codyframe/main/scss/config' as *;
  
  // ↓ copy & modify these templates locally
  @use 'typography';
  @use 'icons';
  @use 'buttons';
  @use 'forms';
  
  // ↓ import here the CodyHouse components
  @use 'components/_1_header' as *;
  @use 'components/_1_footer' as *;
  // ...
  
  @use '../../../node_modules/codyframe/main/scss/util';
````
...and update the link to the config module in each SCSS file.

Example 1: update the the @use rule in the buttons.scss file:
````
  
  @use '../../../node_modules/codyframe/main/scss/config' as *;
  // --- ↑ update this path according to your content structure
  
  .btn {
    position: relative;
    display: inline-flex;
    // ...
  }
````
  Example 2: update the @use rule in each component SCSS file:
  
````
    @use '../../../node_modules/codyframe/main/scss/config' as *;
  
  /* ----↑ */
  @use '_1_collapse.scss' as *;
  @use '_1_anim-menu-btn.scss' as *;
  
  /* -------------------------------- 
  
  File#: _2_morphing-navigation
  Title: Morphing Navigation
  Descr: Header Template with a morphing dropdown
  Usage: codyhouse.co/license
  
  -------------------------------- */
  
  .morph-nav {
    z-index: var(--z-index-header);
    height: var(--morph-nav-height);
    /* ... */
  }
````
