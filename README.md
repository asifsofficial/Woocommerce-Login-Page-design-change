# Woocommerce-Login-Page-design-change

## Location:
```
functions.php
```
```
// Add custom code for change admin login page
function custom_login_logo() {
  echo '<style type="text/css">
    h1 a {
      position: relative;
      animation: moveLogo 2s ease-in-out 1;
      background-image: url(https://hobyshop.com/wp-content/uploads/2023/08/hobyshop-logo-drack.svg) !important;
      background-size: 210px !important;
      width: 210px !important;
      height: 50px !important;
    }

    @keyframes moveLogo {
      0% {
        transform: translateY(100%);
      }
      100% {
        transform: translateY(0);
      }
    }
    
    .login h1 a {
      position: relative;
      animation: moveLogo 2s ease-in-out 1;
      background-image: url(https://hobyshop.com/wp-content/uploads/2023/08/hobyshop-logo-drack.svg) !important;
      background-size: 210px !important;
      width: 210px !important;
      height: 50px !important;
    }
  </style>';
}

add_action('login_head', 'custom_login_logo');

function my_custom_login_logo() {
    echo '<style type="text/css">
        body.login {
            background-image: url(https://shopeybd.com/wp-content/uploads/2021/09/Thank-You-BG.jpg) !important;
            background-repeat: no-repeat !important;
            background-size: cover !important;
        }
        .login form {
            border-radius: 10px;
            background: #ffffff45;
        }
        .login * {
            color: #ffffff;
        }
        .login #backtoblog a, .login #nav a {
            color: #ffffff;
        }
        .login .button.wp-hide-pw .dashicons {
            color: black;
        }
        .login #login_error {
            background-color: transparent;
            border: 1px solid;
            border-radius: 10px;
        }
        .login .button.wp-hide-pw {
            border: 1px solid; 
        }
        .login #loginform .countrycode {
            max-width: 70px !important;
        }
        .wcpa_form_outer .wcpa_form_item select { 
		    border-radius: var(--wd-form-brd-radius);
        }
        .login form {
            border-radius: 10px;
            background: #ffffff45;
        }
        h1.entry-title {
            font-size: 22px;
		    font-weight: 400;
        }
    </style>';
}
add_action('login_head', 'my_custom_login_logo');

function custom_login_footer() {
    $site_name = get_bloginfo( 'name' );
echo '<style type="text/css">
        a:hover {
            color: #e6dbdb;
        }
        </style>
        <div style="position: absolute; bottom: 10px; text-align:center; width:100%"><a href="'.home_url().'" target="_blank" style="text-decoration: none; font-weight: bold;">'.$site_name.'</a> © 2020 - 2023 CREATED BY <img src="/wp-content/uploads/2022/07/asifsofficial-logo.webp" alt="ASIFSOFFICIAL" style="max-width:50px; vertical-align:text-bottom;"/><a href="https://asifsofficial.com" target="_blank" style="text-decoration: none; font-weight: bold;">-SIFSOFFICIAL</a></div>';
}
add_action('login_footer','custom_login_footer');
```
