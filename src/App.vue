<template>
  <div id="app">
    <div id="nav"></div>
    <router-view />
  </div>
</template>

<script>
import store from "./store/index";

export default {
  store,
};
</script>

<style>
html{
  font-family: Arial, Helvetica, sans-serif;
}
.tabs-custom {
  display: flex;
  height: 68px;
  align-items: flex-end;
  position: fixed;
  bottom: -1px;
  z-index: 1000;
  background: var(--tocotoco-color-white);
  width: 100%;
  padding: 0 15px 10px;
  box-shadow: 0 3px 25px 0 rgba(0, 0, 0, 0.1);
}

.tabs-custom .tab-item.tab-rewards {
  width: 22%;
  text-align: center;
}

.tabs-custom .tab-item.tab-store {
  width: 21%;
  text-align: center;
}

.tabs-custom .tab-item.tab-18pc {
  width: 18%;
}

.tabs-custom .tab-item.tab-16pc {
  width: 16%;
}

.tabs-custom .tab-item a {
  text-decoration: none;
  display: inline-block;
  cursor: pointer;
  text-align: center;
}

.tabs-custom .tab-item.tab-middle {
  text-align: center;
  position: relative;
  height: 100%;
  width: 23% !important;
}

.tabs-custom .tab-item.tab-middle a {
  position: absolute;
  top: -28px;
  left: calc(50% - 35px);
  border-radius: 50%;
  height: 72px;
  width: 72px;
  line-height: 92px;
  background: rgba(216, 185, 121, 0.302);
}

.tabs-custom .tab-item.tab-middle a .tab-item--icon {
  height: 62px;
  width: 62px;
  padding: 0;
  border-radius: 50%;
  background: #d8b979;
  margin-left: 5px;
  margin-top: 5px;
}

.tabs-custom .tab-item.tab-middle a img {
  height: 41px;
  margin-left: 5px;
  transition: all 0.3s ease-in-out;
}

.tabs-custom .tab-item.tab-middle .tab-item--label {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
}

.tabs-custom .tab-item.tab-middle .divide-bt {
  background: var(--tocotoco-color-dark-bg);
  border-radius: 10px;
  height: 6px;
  position: absolute;
  width: 100%;
  bottom: 10px;
}

.tabs-custom .tab-item .tab-item--label {
  font-size: 10px;
  color: #d7d7d7;
  text-decoration: none;
  letter-spacing: 1px;
  padding-top: 3px;
  font-weight: 600;
  transition: all 0.3s ease-in-out;
}

.tabs-custom .tab-item .active .tab-item--label {
  color: var(--tocotoco-color-primary);
  transition: all 0.3s ease-in-out;
}

.tabs-custom .tab-item .active .tab-item--icon img:not(.tab-icon--midden) {
  -webkit-filter: invert(0.332) sepia(60) saturate(1.38) hue-rotate(0);
  filter: invert(0.332) sepia(60) saturate(1.38) hue-rotate(0);
}

.tabs-custom .tab-item:last-child {
  text-align: right;
}

.tabs-custom .tab-item:first-child .active .tab-item--icon img {
  opacity: 0;
}

.tabs-custom .tab-item:first-child .active .tab-item--icon img.active {
  opacity: 1;
}

.tabs-custom .tab-item .tab-item--icon {
  padding: 0 10px;
  height: 26px;
  position: relative;
  transition: all 0.3s ease-in-out;
}

.tabs-custom .tab-item .tab-item--icon img {
  transition: all 0.3s ease-in-out;
  opacity: 1;
}

.tabs-custom .tab-item .tab-item--icon img:not(.icon-menu) {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}

.tabs-custom .tab-item .tab-item--icon img.active {
  opacity: 0;
  transition: all 0.3s ease-in-out;
}

.tabs-custom .tab-item .tab-item--icon .img-tab {
  background-color: red;
}

.user-mobile-inner {
  display: flex;
  align-items: center;
  cursor: pointer;
  margin-right: 20px;
}

.user-mobile-inner .user--ava {
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 30px;
  width: 30px;
  border-radius: 50%;
}

.arround-acc-inner {
  background: var(--tocotoco-color-bg);
  border-radius: 50%;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0;
}

.arround-acc-inner img {
  -webkit-filter: invert(0.68) sepia(43) saturate(0) hue-rotate(0);
  filter: invert(0.68) sepia(43) saturate(0) hue-rotate(0);
}

.toolbar-menu-list {
  background: var(--tocotoco-color-white);
  box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.06);
  height: auto !important;
}

.toolbar-menu-list .toolbar-store-detail {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.toolbar-menu-list .title-search-nav {
  position: relative;
  width: 90%;
}

.toolbar-menu-list .title-search-nav input {
  border: none;
  background: #fbfbfb;
  height: 32px;
  padding: 0 20px 0 30px;
  border-radius: 30px;
  width: 100%;
  outline: 0;
  box-shadow: unset;
  font-size: 14px;
}

.toolbar-menu-list .title-search-nav img {
  position: absolute;
  top: 50%;
  left: 10px;
  transform: translateY(-50%);
}

.toolbar-menu-list .toolbar-login,
.toolbar-menu-list .toolbar-logo {
  display: none;
}

.toolbar-menu-list .toolbar-group {
  position: relative;
}

.toolbar-menu-list .toolbar-group .toolbar-group-icon {
  display: flex;
  align-items: center;
}

.toolbar-menu-list .toolbar-group .toolbar-group-info {
  position: absolute;
  bottom: -3px;
  right: -3px;
  background: var(--tocotoco-color-primary);
  height: 13px;
  width: 13px;
  line-height: 13px;
  text-align: center;
  border-radius: 50%;
  color: var(--tocotoco-color-white);
  font-size: 14px;
}

.region-city {
  font-weight: 600;
  font-size: 14px;
}

.region-city img {
  margin-right: 5px;
}

.menu-list-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  border-top: 1px solid var(--tocotoco-color-border-exlight);
  height: 44px;
}

.menu-list-top .btn-creat-group {
  border: none;
  box-shadow: none;
  background: var(--tocotoco-color-primary);
  color: var(--tocotoco-color-white);
  border-radius: 30px;
  height: 30px;
  padding: 0 16px;
  font-size: 15px;
}

.menu-list-top .btn-view-grid {
  margin-right: 10px;
}

.menu-list-top .btn-view-grid,
.menu-list-top .btn-view-list {
  border: 1px solid #b8b8b8;
  border-radius: 6px;
  background: var(--tocotoco-color-white);
  height: 28px;
  width: 28px;
  line-height: 29px;
  color: #b8b8b8;
  transition: all 0.3s ease-in-out;
  display: inline-flex;
  align-items: center;
  padding: 0 6px !important;
}

.menu-list-top .btn-view-grid img,
.menu-list-top .btn-view-list img {
  -webkit-filter: invert(0.42) sepia(43) saturate(0) hue-rotate(0);
  filter: invert(0.42) sepia(43) saturate(0) hue-rotate(0);
  height: 14px;
}

.menu-list-top .btn-view-grid.active,
.menu-list-top .btn-view-list.active {
  transition: all 0.3s ease-in-out;
  background: var(--tocotoco-color-primary);
  border: 1px solid var(--tocotoco-color-primary);
  color: var(--tocotoco-color-white);
}

.menu-list-top .btn-view-grid.active img {
  -webkit-filter: invert(1) sepia(43) saturate(0) hue-rotate(0);
  filter: invert(1) sepia(43) saturate(0) hue-rotate(0);
}

.menu-list-top .btn-view-list.active img {
  -webkit-filter: invert(0) sepia(43) saturate(0) hue-rotate(0);
  filter: invert(0) sepia(43) saturate(0) hue-rotate(0);
}

.menu-list-wrapper {
  margin-top: 115px;
}

.btn-menu-fab {
  position: fixed;
  left: 20px;
  bottom: 80px;
  background: var(--tocotoco-color-primary);
  border-radius: 50%;
  height: 40px;
  width: 40px;
  box-shadow: 2px 2px 12px 1px rgba(0, 0, 0, 0.18);
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  outline: 0;
  z-index: 1000;
}

.btn-menu-fab.show-menu {
  z-index: 1009;
}

.btn-menu-fab i {
  color: var(--tocotoco-color-white);
}

.btn-menu-fab .close-menu {
  opacity: 0;
  display: none;
}

.btn-menu-fab .open-menu {
  opacity: 1;
  display: block;
}

.bg-bt-divide {
  width: 100%;
  height: 30px;
  position: fixed;
  bottom: 0;
  background-image: linear-gradient(
    to top,
    #fff 15%,
    rgba(255, 255, 255, 0.3) 82%,
    rgba(255, 255, 255, 0.01) 109%
  );
  z-index: 1001;
}

.bg-bt-divide .bt-group {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.bg-bt-divide.show-dialog {
  z-index: 1000;
}

.bg-bt-divide.show-dialog .checkout-bt-inner {
  border-top: 1px solid !important;
  box-shadow: none !important;
}

.bg-bt-divide .divide-bt-log {
  background: #282828;
  border-radius: 10px;
  height: 6px;
  position: fixed;
  width: 140px;
  bottom: 10px;
  left: calc(50% - 70px);
}

.bg-bt-divide.has-product {
  background: #fff;
  height: 60px;
}

.bg-bt-divide.has-product .checkout-bt-inner {
  position: fixed;
  width: 100%;
  bottom: 15px;
  background: #fff;
  padding: 15px 20px 0;
  box-shadow: 0 -2px 5px 0 rgba(0, 0, 0, 0.06);
}

.bg-bt-divide.has-product .checkout-bt-inner .cus-global-overlay-wrapper {
  display: none;
}

.bg-bt-divide.has-product .checkout-bt--left {
  font-weight: 600;
  display: flex;
  align-items: center;
  width: calc(100% - 115px);
}

.bg-bt-divide.has-product .checkout-bt--left span {
  padding: 0 3px;
}

.bg-bt-divide.has-product .checkout-bt--left span.text-primary {
  color: var(--tocotoco-color-brown-dark);
}

.bg-bt-divide.has-product .checkout-bt--left span.price-compare {
  font-weight: 400;
  font-size: 12px;
  text-decoration: line-through;
}

.bg-bt-divide.has-product .checkout-bt--right {
  border: none;
  box-shadow: none;
  background: var(--tocotoco-color-primary);
  color: var(--tocotoco-color-white);
  border-radius: 30px;
  height: 30px;
  padding: 0 16px;
  font-size: 15px;
  z-index: 2;
}

.skeleton-item {
  display: flex;
  padding: 5px;
  background: #fff;
  border-bottom: 1px solid var(--tocotoco-color-border);
}

.skeleton-item:first-child {
  padding-top: 20px;
}

.skeleton-item:last-child {
  padding-bottom: 20px;
}

.skeleton-item .skeleton-img {
  width: 70px;
  height: 70px;
  -webkit-animation: 1.7s linear infinite loading;
  animation: 1.7s linear infinite loading;
  background: var(--tocotoco-color-border-gray);
  background-image: linear-gradient(
    to right,
    var(--tocotoco-color-border-gray) 0,
    #f2f3f5 20%,
    var(--tocotoco-color-border-gray) 40%,
    var(--tocotoco-color-border-gray) 100%
  );
  background-repeat: no-repeat;
  margin-right: 10px;
}

.skeleton-item .skeleton-price,
.skeleton-item .skeleton-title {
  height: 12px;
  -webkit-animation: 1.7s linear infinite loading;
  animation: 1.7s linear infinite loading;
  background: var(--tocotoco-color-border-gray);
  background-image: linear-gradient(
    to right,
    var(--tocotoco-color-border-gray) 0,
    #f2f3f5 20%,
    var(--tocotoco-color-border-gray) 40%,
    var(--tocotoco-color-border-gray) 100%
  );
  background-repeat: no-repeat;
  margin-bottom: 5px;
}

.skeleton-item .skeleton-title {
  width: 250px;
}

.skeleton-item .skeleton-price {
  width: 150px;
}

@media screen and (min-width: 769px) {
  .toolbar-store {
    padding: 0 !important;
    height: 52px !important;
    min-height: 52px !important;
  }

  .toolbar-store .toolbar-group {
    display: none;
  }

  .menu-list-top-inside {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 38px;
    width: calc(100% - 4px);
    background-color: #fff;
    padding: 0 20px;
    margin-left: 4px;
    margin-bottom: 15px;
  }

  .menu-list-top {
    margin-left: calc(25% + 20px);
    width: calc(50% - 49px);
    z-index: 1;
    background-color: #fbfbfb;
    height: 74px !important;
    border-top: 0 !important;
    position: fixed;
    top: 49px;
    padding: 0 !important;
    align-items: flex-end !important;
  }

  .menu-list-wrapper {
    display: flex;
    align-items: flex-start;
    margin-top: 70px !important;
    max-width: 1200px;
    margin-left: auto;
    margin-right: auto;
  }

  .menu-list-wrapper .menu-list-sidebar {
    max-width: 25%;
    width: 25%;
    position: fixed;
    display: block !important;
    margin: 0 15px;
  }

  .menu-list-wrapper .menu-list-sidebar .menu-categories--title {
    text-align: left !important;
    text-transform: uppercase;
    font-size: 14px !important;
    padding: 10px 20px !important;
  }

  .menu-list-wrapper .menu-list-sidebar ul.menu-list {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .menu-list-wrapper .menu-list-sidebar ul.menu-list li.menu-item a {
    border-bottom: 1px solid #f8f8f8;
    text-decoration: none;
    color: var(--tocotoco-color-brown-dark);
    display: block;
    padding: 10px 15px;
    transition: 0.3s;
    border-left: 2px solid transparent;
  }

  .menu-list-wrapper .menu-list-sidebar ul.menu-list li.menu-item a.active,
  .menu-list-wrapper .menu-list-sidebar ul.menu-list li.menu-item a:hover {
    color: var(--tocotoco-color-primary);
    border-left: 2px solid var(--tocotoco-color-primary);
  }

  .menu-list-wrapper .menu-list-content {
    max-width: 50%;
    width: 50%;
    margin: 0;
    margin-left: calc(25% + 25px);
    padding-top: 44px;
  }

  .menu-list-wrapper .bg-bt-divide,
  .menu-list-wrapper .checkout-bt-inner,
  .menu-list-wrapper .divide-bt-log {
    position: static !important;
    z-index: 0;
  }

  .menu-list-wrapper .bg-bt-divide {
    max-width: 25%;
    margin: 0 15px;
    height: auto;
  }

  .menu-list-wrapper .checkout-bt-inner {
    width: 25% !important;
    text-align: center;
    display: block !important;
    position: fixed !important;
    top: 69px;
    height: -webkit-max-content;
    height: -moz-max-content;
    height: max-content;
  }

  .menu-list-wrapper .checkout-bt-inner .checkout-bt--left {
    margin-bottom: 15px;
    width: 100%;
  }

  .menu-list-wrapper .checkout-bt-inner .checkout-bt--right {
    width: 100%;
    margin-bottom: 15px;
  }

  .menu-list-wrapper .checkout-bt-inner .cus-global-overlay-wrapper {
    display: block !important;
    margin: -15px -20px 0;
  }

  .menu-list-wrapper
    .checkout-bt-inner
    .cus-global-overlay-wrapper
    .dialog-title--left {
    text-align: left;
    text-transform: uppercase;
  }

  .menu-list-wrapper
    .checkout-bt-inner
    .cus-global-overlay-wrapper
    .dialog-close {
    display: none !important;
  }

  .menu-list-wrapper
    .checkout-bt-inner
    .cus-global-overlay-wrapper
    .menu-item-order {
    padding: 7px 0 !important;
  }

  .menu-list-wrapper .checkout-bt-inner .bt-group {
    flex-direction: column;
    margin-top: 15px;
    align-items: flex-start;
  }

  .menu-list-wrapper .divide-bt-log {
    margin: auto !important;
  }

  .toolbar-menu-list .router-link-cus {
    display: none;
  }

  .toolbar-menu-list .toolbar-login {
    display: block !important;
  }

  .toolbar-menu-list .toolbar-logo {
    display: flex !important;
    align-items: center;
  }

  .toolbar-menu-list .toolbar-logo img {
    width: 150px;
  }

  .toolbar-menu-list .title-search-nav {
    width: 40% !important;
  }

  .toolbar-menu-list .toolbar-login a {
    display: inline-block;
    padding: 6px 15px;
    background: var(--tocotoco-color-primary);
    color: var(--tocotoco-color-white);
    text-decoration: none;
    font-size: 14px;
    line-height: normal;
    border-radius: 25px;
  }

  .toolbar-menu-list .toolbar-login .user-info {
    display: flex;
    align-items: center;
    cursor: pointer;
  }

  .toolbar-menu-list .toolbar-login .user-info .user-avatar {
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 30px;
    width: 30px;
    border-radius: 50%;
  }

  .toolbar-menu-list .toolbar-login .user-info .user-display-name {
    font-size: 14px;
    margin-left: 7px;
    font-weight: 400;
  }

  .mat-dialog-container app-authentication,
  .mat-dialog-container app-login-by-email,
  .mat-dialog-container app-register {
    height: 550px !important;
    display: flex !important;
    align-items: center;
    justify-content: flex-end;
  }

  .mat-dialog-container app-authentication .authentication-inner,
  .mat-dialog-container app-authentication .login-inner,
  .mat-dialog-container app-authentication .register-inner,
  .mat-dialog-container app-login-by-email .authentication-inner,
  .mat-dialog-container app-login-by-email .login-inner,
  .mat-dialog-container app-login-by-email .register-inner,
  .mat-dialog-container app-register .authentication-inner,
  .mat-dialog-container app-register .login-inner,
  .mat-dialog-container app-register .register-inner {
    height: auto !important;
    padding: 0 !important;
    width: 42%;
  }

  .mat-dialog-container app-authentication .authentication-inner .btn-close,
  .mat-dialog-container app-authentication .login-inner .btn-close,
  .mat-dialog-container app-authentication .register-inner .btn-close,
  .mat-dialog-container app-login-by-email .authentication-inner .btn-close,
  .mat-dialog-container app-login-by-email .login-inner .btn-close,
  .mat-dialog-container app-login-by-email .register-inner .btn-close,
  .mat-dialog-container app-register .authentication-inner .btn-close,
  .mat-dialog-container app-register .login-inner .btn-close,
  .mat-dialog-container app-register .register-inner .btn-close {
    left: auto !important;
    right: 10px;
    top: 10px !important;
  }

  .mat-dialog-container app-authentication .authentication-inner button,
  .mat-dialog-container app-authentication .login-inner button,
  .mat-dialog-container app-authentication .register-inner button,
  .mat-dialog-container app-login-by-email .authentication-inner button,
  .mat-dialog-container app-login-by-email .login-inner button,
  .mat-dialog-container app-login-by-email .register-inner button,
  .mat-dialog-container app-register .authentication-inner button,
  .mat-dialog-container app-register .login-inner button,
  .mat-dialog-container app-register .register-inner button {
    font-size: 12px;
  }

  .mat-dialog-container
    app-authentication
    .authentication-inner
    button.btn-log-fb
    img,
  .mat-dialog-container
    app-authentication
    .authentication-inner
    button.btn-log-gg
    img,
  .mat-dialog-container app-authentication .login-inner button.btn-log-fb img,
  .mat-dialog-container app-authentication .login-inner button.btn-log-gg img,
  .mat-dialog-container
    app-authentication
    .register-inner
    button.btn-log-fb
    img,
  .mat-dialog-container
    app-authentication
    .register-inner
    button.btn-log-gg
    img,
  .mat-dialog-container
    app-login-by-email
    .authentication-inner
    button.btn-log-fb
    img,
  .mat-dialog-container
    app-login-by-email
    .authentication-inner
    button.btn-log-gg
    img,
  .mat-dialog-container app-login-by-email .login-inner button.btn-log-fb img,
  .mat-dialog-container app-login-by-email .login-inner button.btn-log-gg img,
  .mat-dialog-container
    app-login-by-email
    .register-inner
    button.btn-log-fb
    img,
  .mat-dialog-container
    app-login-by-email
    .register-inner
    button.btn-log-gg
    img,
  .mat-dialog-container
    app-register
    .authentication-inner
    button.btn-log-fb
    img,
  .mat-dialog-container
    app-register
    .authentication-inner
    button.btn-log-gg
    img,
  .mat-dialog-container app-register .login-inner button.btn-log-fb img,
  .mat-dialog-container app-register .login-inner button.btn-log-gg img,
  .mat-dialog-container app-register .register-inner button.btn-log-fb img,
  .mat-dialog-container app-register .register-inner button.btn-log-gg img {
    margin: 12px 5px !important;
  }

  .mat-dialog-container app-authentication .register-inner .btn-regis-email,
  .mat-dialog-container app-authentication .register-inner .register-title,
  .mat-dialog-container app-authentication .register-inner .switch-register,
  .mat-dialog-container app-login-by-email .register-inner .btn-regis-email,
  .mat-dialog-container app-login-by-email .register-inner .register-title,
  .mat-dialog-container app-login-by-email .register-inner .switch-register,
  .mat-dialog-container app-register .register-inner .btn-regis-email,
  .mat-dialog-container app-register .register-inner .register-title,
  .mat-dialog-container app-register .register-inner .switch-register {
    margin-bottom: 15px !important;
  }

  .mat-dialog-container app-authentication .register-inner .item-inpt-regis,
  .mat-dialog-container app-login-by-email .register-inner .item-inpt-regis,
  .mat-dialog-container app-register .register-inner .item-inpt-regis {
    padding-top: 0 !important;
  }
}

@media screen and (min-width: 1200px) {
  .menu-list-top {
    margin-left: calc((1200px * 0.25) + 20px) !important;
    width: calc((1200px * 0.5) - 49px) !important;
  }

  .menu-list-wrapper .menu-list-sidebar {
    max-width: calc(1200px * 0.25) !important;
    width: calc(1200px * 0.25) !important;
  }

  .menu-list-wrapper .checkout-bt-inner {
    width: calc(1200px * 0.25) !important;
  }
}

@media (-ms-high-contrast: active) {
  .mat-toolbar {
    outline: solid 1px;
  }
}

.mat-toolbar-row,
.mat-toolbar-single-row {
  display: flex;
  box-sizing: border-box;
  padding: 0 16px;
  width: 100%;
  flex-direction: row;
  align-items: center;
  white-space: nowrap;
}

.mat-toolbar-multiple-rows {
  display: flex;
  box-sizing: border-box;
  flex-direction: column;
  width: 100%;
}

.mat-toolbar-multiple-rows {
  min-height: 64px;
}

.mat-toolbar-row,
.mat-toolbar-single-row {
  height: 64px;
}

@media (max-width: 599px) {
  .mat-toolbar-multiple-rows {
    min-height: 56px;
  }

  .mat-toolbar-row,
  .mat-toolbar-single-row {
    height: 56px;
  }
}

.overlay-menu-categories {
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.2);
}

.menu-categories-inner .menu-categories--title {
  border-bottom: 1px solid var(--tocotoco-color-border-exlight);
  padding: 0 15px 15px;
  text-align: center;
  font-weight: 600;
  font-size: 18px;
}

.menu-categories-inner .menu-categories--content {
  padding: 0 20px 10px;
  max-height: 380px;
  overflow-y: auto;
}

.menu-categories-inner .menu-categories--content::-webkit-scrollbar {
  width: 4px;
  height: 10px;
  background-color: #f2f2f2;
  border-bottom-left-radius: 0;
}

.menu-categories-inner .menu-categories--content::-webkit-scrollbar-thumb {
  border-radius: 20px;
  background-color: #999;
}

.menu-categories-inner .menu-categories--content::-webkit-scrollbar-track {
  box-shadow: none;
  background-color: #f2f2f2;
  border-bottom-left-radius: 0;
}

.menu-categories-inner .menu-categories--content .menu-categories--item {
  display: flex;
  padding: 8px 20px;
  background-color: white;
  align-items: center;
  justify-content: space-between;
  font-weight: 500;
  margin-top: 5px;
  cursor: pointer;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.menu-categories-inner
  .menu-categories--content
  .menu-categories--item:last-child {
  border-bottom: none;
}

.menu-categories-inner
  .menu-categories--content
  .menu-categories--item
  .item--count {
  color: var(--tocotoco-color-brown-dark);
}

.customized-categories-dialog {
  margin-left: 20px !important;
}

.customized-categories-dialog .mat-dialog-container {
  padding: 15px 0;
}

@media screen and (min-width: 769px) {
  .menu-categories-inner .menu-categories--content {
    max-height: calc(100vh - 130px);
    min-height: 200px;
  }
}

.customized-order-dialog {
  max-width: 100vw !important;
}

.customized-order-dialog .mat-dialog-container {
  padding: 0;
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-top {
  text-align: center;
  position: fixed;
  width: 100%;
  background: var(--tocotoco-color-white);
  padding: 10px 15px;
  border-bottom: 1px solid #f8f8f8;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.cus-global-overlay-wrapper
  .dialog-title
  .dialog-title-top
  .dialog-title--left {
  width: calc(100% - 53px);
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-top .orders-title {
  font-weight: 600;
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-top .dialog-close {
  background: #7e7e7e;
  border: 0;
  border-radius: 50%;
  width: 20px;
  height: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  top: 50%;
  left: 15px;
  transform: translateY(-50%);
  color: #fff;
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-top .dialog-close i {
  font-size: 18px;
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-top .btn-group {
  font-size: 12px;
  cursor: pointer;
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #fbfbfb;
  padding: 7px 15px;
}

.cus-global-overlay-wrapper
  .dialog-title
  .dialog-title-bottom.no-group
  .title-group {
  background: var(--tocotoco-color-dark-bg);
  font-weight: 500;
}

.cus-global-overlay-wrapper
  .dialog-title
  .dialog-title-bottom.no-group
  .btn-group {
  cursor: pointer;
}

.cus-global-overlay-wrapper .dialog-title .dialog-title-bottom .title-group {
  background: #799dd9;
  color: #fff;
  border-radius: 5px;
  padding: 7px 15px;
}

.cus-global-overlay-wrapper .dialog-list-item {
  max-height: 170px;
  overflow: auto;
  text-align: left;
  padding-top: 38px;
}

.cus-global-overlay-wrapper .dialog-list-item .no-item {
  padding: 20px 15px;
}

.cus-global-overlay-wrapper .dialog-list-item.no-group {
  max-height: 70vh;
}

.cus-global-overlay-wrapper .dialog-list-item::-webkit-scrollbar {
  width: 4px;
  height: 10px;
  background-color: #f2f2f2;
  border-bottom-left-radius: 0;
}

.cus-global-overlay-wrapper .dialog-list-item::-webkit-scrollbar-thumb {
  border-radius: 20px;
  background-color: #999;
}

.cus-global-overlay-wrapper .dialog-list-item::-webkit-scrollbar-track {
  box-shadow: none;
  background-color: #f2f2f2;
  border-bottom-left-radius: 0;
}

.cus-global-overlay-wrapper .dialog-group-info {
  padding-bottom: 80px;
}

.cus-global-overlay-wrapper .dialog-group-info .group-selected-title {
  display: flex;
  align-items: center;
  position: relative;
  background: #fbfbfb;
  padding: 7px 15px;
}

.cus-global-overlay-wrapper
  .dialog-group-info
  .group-selected-title
  .ava-selected {
  padding-left: 5px;
}

.cus-global-overlay-wrapper
  .dialog-group-info
  .group-selected-title
  .ava-selected
  img {
  width: 35px;
  margin-left: -5px;
  border-radius: 50%;
  float: left;
}

.cus-global-overlay-wrapper
  .dialog-group-info
  .group-selected-title
  .quantity-selected {
  font-weight: 600;
  margin-left: 15px;
}

.cus-global-overlay-wrapper
  .dialog-group-info
  .group-selected-title
  .icon-selected {
  position: absolute;
  right: 15px;
}

.cus-global-overlay-wrapper .dialog-group-info .group-list-item {
  overflow-x: auto;
  overflow-y: visible;
  white-space: nowrap;
  width: calc(100% - 15px);
  min-width: calc(100% - 15px);
  padding: 16px 0 16px 15px;
  display: flex;
  border-bottom: 1px solid #f8f8f8;
}

.cus-global-overlay-wrapper
  .dialog-group-info
  .group-list-item::-webkit-scrollbar {
  display: none;
}

.cus-global-overlay-wrapper .dialog-group-info .group-list-item app-group-item {
  position: relative;
  text-align: center;
  width: 30%;
  min-width: 30%;
  margin-right: 10px;
  border-radius: 5px;
  box-shadow: 0 0 1px 0 rgba(0, 0, 0, 0.15);
}

.cus-global-overlay-wrapper .dialog-group-info .group-add {
  text-align: center;
  padding: 15px;
}

.cus-global-overlay-wrapper .dialog-group-info .group-add button {
  background: 0 0;
  border: 1px solid var(--tocotoco-color-primary);
  color: var(--tocotoco-color-primary);
  border-radius: 25px;
  display: flex;
  margin: auto;
  align-items: center;
  padding: 5px 20px;
}

.cus-global-overlay-wrapper .dialog-group-info .group-add button i {
  font-size: 18px;
}

@media screen and (min-width: 769px) {
  .cus-global-overlay-wrapper .dialog-title-top {
    position: relative !important;
  }

  .cus-global-overlay-wrapper .dialog-list-item {
    padding: 10px 0 !important;
  }

  .cus-global-overlay-wrapper .dialog-list-item.no-group {
    max-height: 62vh;
  }
}

.toast-cus {
  color: var(--tocotoco-color-white);
  background: rgba(40, 40, 40, 0.68);
  width: 88px;
  height: 88px;
  border-radius: 6px;
  left: 50%;
  top: 50%;
  position: fixed;
  contain: strict;
  z-index: -1;
  pointer-events: none;
  opacity: 0;
  transform: translate(-50%, -50%);
  transition: all 0.3s ease-in-out;
}

.toast-cus.show-toast {
  opacity: 1;
  z-index: 60001;
  transition: all 0.3s ease-in-out;
}

.toast-cus .toast-wrapper {
  left: 0;
  right: 0;
  margin: auto;
  display: block;
  position: absolute;
  width: 100%;
  height: 100%;
  max-width: 700px;
  z-index: 10;
}

.toast-cus .toast-wrapper .toast-container {
  display: flex;
  align-items: center;
  pointer-events: auto;
  contain: content;
  margin: auto;
  height: 100%;
  text-align: center;
}

.toast-cus .toast-wrapper .toast-container .toast-message {
  flex: 1;
}

.toast-cus .toast-wrapper .toast-container .toast-message i {
  font-size: 38px;
  font-weight: 400;
}

.menu-item-order {
  display: flex;
  align-items: center;
  margin: 0 15px;
  padding: 7px;
  border-bottom: 1px solid #f8f8f8;
}

.menu-item-order .item-info {
  width: 75%;
  padding-right: 3px;
}

.menu-item-order .item-info .item-title {
  font-weight: 600;
  margin-bottom: 5px;
}

.menu-item-order .item-info .item-topping {
  color: var(--tocotoco-color-gray);
  margin-bottom: 5px;
}

.menu-item-order .item-info .item-quantity {
  color: var(--tocotoco-color-brown-dark);
  font-weight: 500;
}

.menu-item-order .item-action {
  width: 25%;
  text-align: right;
  display: flex;
  justify-content: space-between;
}

.menu-item-order .item-action .change-quantity {
  color: var(--tocotoco-color-white);
  background: #799dd9;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 0;
  line-height: 15px;
  font-size: 26px;
  font-weight: 600;
  text-align: center;
  cursor: pointer;
}

:last-child .menu-group-inner .menu-group-list.active {
  padding-bottom: 110px;
}

.menu-group-inner {
  transition: all 0.3s ease-in-out;
}

.menu-group-inner .group-title {
  height: 38px;
  display: flex;
  align-items: center;
  padding: 0 20px;
  justify-content: space-between;
}

.menu-group-inner .group-title:not(.active) {
  border-bottom: 1px solid var(--tocotoco-color-border-exlight);
}

.menu-group-inner .group-title .group-title--label {
  font-weight: 600;
}

.menu-group-inner .group-title .group-title--right {
  color: var(--tocotoco-color-gray);
  display: flex;
  align-items: normal;
}

.menu-group-inner .group-title .group-title--right .count-product {
  opacity: 1;
  transition: all 0.3s ease-in-out;
  padding-right: 5px;
}

.menu-group-inner .group-title i {
  font-size: 16px;
  color: var(--tocotoco-color-gray);
  margin-right: -4px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.menu-group-inner .group-title.active .group-title--right .count-product {
  opacity: 0;
  transition: all 0.3s ease-in-out;
}

.menu-group-inner .group-title.active i {
  transform: rotate(180deg);
  transition: all 0.3s ease-in-out;
}

.menu-group-inner .menu-group-list {
  position: relative;
  max-height: 0;
  overflow-y: hidden;
  transition: max-height 0.3s ease-out;
  display: flex;
  flex-wrap: wrap;
}

.menu-group-inner .menu-group-list.active {
  max-height: -webkit-max-content;
  max-height: -moz-max-content;
  max-height: max-content;
  overflow-y: auto;
  transition: max-height 0.3s ease-out;
}

.menu-group-inner .menu-group-list .app-menu-item-product {
  transition: all 0.3s ease-in-out;
}

.menu-group-inner .no-product {
  background: var(--tocotoco-color-white);
  padding: 10px 20px;
  font-style: italic;
  width: 100%;
}

@media screen and (min-width: 769px) {
  .menu-group-list {
    margin-left: -10px;
  }

  .no-product {
    margin-left: 10px;
  }
}

.item-left {
  margin: 0 5px 10px 20px;
}

.item-right {
  margin: 0 20px 10px 5px;
}

.item-menu-product-inner {
  padding: 15px;
  transition: all 0.3s ease-in-out;
}

.item-menu-product-inner .product-feature-img {
  width: 100%;
  background-size: cover !important;
  background-position: center !important;
  background-repeat: no-repeat !important;
  height: 135px;
  position: relative;
}

.item-menu-product-inner .product-feature-img img {
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%);
  max-height: 135px;
  left: 50%;
}

.item-menu-product-inner .item-mn-product-infor {
  padding-top: 5px;
}

.item-menu-product-inner .item-mn-product-infor .product-title {
  font-weight: 600;
  padding: 5px 0;
}

.item-menu-product-inner .item-mn-product-infor .product-title a {
  color: var(--tocotoco-color-dark-bg);
  height: 36px;
  -webkit-box-orient: vertical;
  display: block;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  overflow: hidden;
  text-overflow: ellipsis;
}

.item-menu-product-inner .item-mn-product-infor .product-price {
  display: flex;
  align-items: baseline;
}

.item-menu-product-inner .item-mn-product-infor .product-price .price-current {
  color: var(--tocotoco-color-brown-dark);
  font-weight: 600;
  padding-right: 6px;
}

.item-menu-product-inner .item-mn-product-infor .product-price .price-compare {
  font-size: 12px;
  text-decoration: line-through;
  color: #535353;
}

.item-menu-product-inner .item-mn-product-action {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  position: absolute;
  right: 15px;
  bottom: 15px;
}

.item-menu-product-inner .item-mn-product-action .item-mn-product-quantity {
  transition: all 0.3s ease-in-out;
  font-weight: 600;
  padding: 0 8px;
}

.item-menu-product-inner .item-mn-product-action .item-mn-product-add,
.item-menu-product-inner .item-mn-product-action .item-mn-product-remove {
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease-in-out;
  border-radius: 50%;
  background: rgb(216, 185, 121);
  color: var(--tocotoco-color-white);
  height: 20px;
  width: 20px;
  text-align: center;
  line-height: 15px;
  font-size: 26px;
  font-weight: 600;
}

.btn-action div {
  float: left;
  text-align: center;
  width: 20px;
  border-radius: 50%;
  background-color: rgb(216, 185, 121);
  cursor: pointer;
  margin-right: 5px;
}

.text-between-btn {
  float: left;
  margin-right: 5px;
}

.app-menu-item-product-grid {
  width: 29%;
  position: relative;
  background-color: white;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.cart-item {
  padding: 5px 30px;
  margin-top: 5px;
  box-shadow: rgba(0, 0, 0, 0.1);
  border-bottom: 1px solid grey;
}

.cart-item:last-child {
  border-bottom: none;
}

.total {
  display: flex;
  align-items: center;
  padding: 20px 30px;
}

.total img {
  width: 20px;
}

.cart-title {
  background-color: white;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  flex-direction: row;
  display: flex;
}

.cart-title h3 {
  margin: 0;
  padding: 10px 30px;
  font-weight: bold;
}

.cart-title div {
  padding: 10px 10px;
  color: turquoise;
  cursor: pointer;
}

h1 {
  text-align: center;
  font-family: Arial, sans-serif;
  color: #06d85f;
  margin: 80px 0;
}

.box {
  width: 40%;
  margin: 0 auto;
  background: rgba(255, 255, 255, 0.2);
  padding: 35px;
  border: 2px solid #fff;
  border-radius: 20px/50px;
  background-clip: padding-box;
  text-align: center;
}

.button {
  font-size: 1em;
  padding: 10px;
  color: #fff;
  border: 2px solid #06d85f;
  border-radius: 20px/50px;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease-out;
}
.button:hover {
  background: #06d85f;
}

.overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.7);
  transition: opacity 500ms;
  visibility: hidden;
  opacity: 0;
}
.overlay:target {
  visibility: visible;
  opacity: 1;
}

.popup {
  margin: 70px auto;
  padding: 20px;
  background: #fff;
  border-radius: 5px;
  width: 30%;
  position: relative;
  transition: all 5s ease-in-out;
}

.popup h2 {
  margin-top: 0;
  color: #333;
  font-family: Arial, sans-serif;
}
.popup .close {
  position: absolute;
  top: 20px;
  right: 30px;
  transition: all 200ms;
  font-size: 30px;
  font-weight: bold;
  text-decoration: none;
  color: #333;
}
.popup .close:hover {
  color: #06d85f;
}
.popup .content {
  max-height: 30%;
  overflow: auto;
}

/* Popup box BEGIN */
.hover_bkgr_fricc {
  background: rgba(0, 0, 0, 0.4);
  cursor: pointer;
  display: none;
  height: 100%;
  position: fixed;
  text-align: center;
  top: 0;
  width: 100%;
  z-index: 10000;
}
.hover_bkgr_fricc .helper {
  display: inline-block;
  height: 100%;
  vertical-align: middle;
}
.hover_bkgr_fricc > div {
  background-color: #fff;
  box-shadow: 10px 10px 60px #555;
  display: inline-block;
  height: auto;
  max-width: 551px;
  min-height: 100px;
  vertical-align: middle;
  width: 60%;
  position: relative;
  border-radius: 8px;
}
.popupCloseButton {
  background-color: #fff;
  border: 3px solid #999;
  border-radius: 50px;
  cursor: pointer;
  display: inline-block;
  font-family: arial;
  font-weight: bold;
  position: absolute;
  top: -20px;
  right: -20px;
  font-size: 25px;
  line-height: 30px;
  width: 30px;
  height: 30px;
  text-align: center;
}
.popupCloseButton:hover {
  background-color: #ccc;
}
.trigger_popup_fricc {
  cursor: pointer;
  font-size: 20px;
  margin: 20px;
  display: inline-block;
  font-weight: bold;
  background-color: rgb(216, 185, 121);
  padding: 10px;
  border-radius: 20px;
}
/* Popup box BEGIN */

#style-2::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  border-radius: 10px;
  background-color: #f5f5f5;
}

#style-2::-webkit-scrollbar {
  width: 12px;
  background-color: #f5f5f5;
}

#style-2::-webkit-scrollbar-thumb {
  border-radius: 10px;
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  background-color: #535353;
}
.scrollbar {
  background-color: white;
  float: left;
  height: 300px;
  width: 100%;
  overflow-y: scroll;
  margin-bottom: 25px;
}
.scrollbar.sd {
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>
