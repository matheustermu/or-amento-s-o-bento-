<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
/*! normalize.css v4.1.1 | MIT License | github.com/necolas/normalize.css */
html {
    font-family: sans-serif;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%
}

body {
    margin: 0
}

article,aside,details,figcaption,figure,footer,header,main,menu,nav,section {
    display: block
}

summary {
    display: list-item
}

audio,canvas,progress,video {
    display: inline-block
}

audio:not([controls]) {
    display: none;
    height: 0
}

progress {
    vertical-align: baseline
}

template,[hidden] {
    display: none !important
}

a {
    background-color: transparent
}

a:active,a:hover {
    outline-width: 0
}

abbr[title] {
    border-bottom: none;
    text-decoration: underline;
    text-decoration: underline dotted
}

b,strong {
    font-weight: inherit
}

b,strong {
    font-weight: bolder
}

dfn {
    font-style: italic
}

h1 {
    font-size: 2em;
    margin: 0.67em 0
}

mark {
    background-color: #ff0;
    color: #000
}

small {
    font-size: 80%
}

sub,sup {
    font-size: 75%;
    line-height: 0;
    position: relative;
    vertical-align: baseline
}

sub {
    bottom: -0.25em
}

sup {
    top: -0.5em
}

img {
    border-style: none
}

svg:not(:root) {
    overflow: hidden
}

code,kbd,pre,samp {
    font-family: monospace, monospace;
    font-size: 1em
}

figure {
    margin: 1em 40px
}

hr {
    box-sizing: content-box;
    height: 0;
    overflow: visible
}

button,input,select,textarea {
    font: inherit;
    margin: 0
}

optgroup {
    font-weight: bold
}

button,input {
    overflow: visible
}

button,select {
    text-transform: none
}

button,html [type="button"],[type="reset"],[type="submit"] {
    -webkit-appearance: button
}

button::-moz-focus-inner,[type="button"]::-moz-focus-inner,[type="reset"]::-moz-focus-inner,[type="submit"]::-moz-focus-inner {
    border-style: none;
    padding: 0
}

button:-moz-focusring,[type="button"]:-moz-focusring,[type="reset"]:-moz-focusring,[type="submit"]:-moz-focusring {
    outline: 1px dotted ButtonText
}

fieldset {
    border: 1px solid #c0c0c0;
    margin: 0 2px;
    padding: 0.35em 0.625em 0.75em
}

legend {
    box-sizing: border-box;
    color: inherit;
    display: table;
    max-width: 100%;
    padding: 0;
    white-space: normal
}

textarea {
    overflow: auto
}

[type="checkbox"],[type="radio"] {
    box-sizing: border-box;
    padding: 0
}

[type="number"]::-webkit-inner-spin-button,[type="number"]::-webkit-outer-spin-button {
    height: auto
}

[type="search"] {
    -webkit-appearance: textfield;
    outline-offset: -2px
}

[type="search"]::-webkit-search-cancel-button,[type="search"]::-webkit-search-decoration {
    -webkit-appearance: none
}

::-webkit-input-placeholder {
    color: inherit;
    opacity: 0.54
}

::-webkit-file-upload-button {
    -webkit-appearance: button;
    font: inherit
}

* {
    box-sizing: border-box
}

input,select,textarea,button {
    font-family: inherit;
    font-size: inherit;
    line-height: inherit
}

body {
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-size: 14px;
    line-height: 1.5;
    color: #24292e;
    background-color: #fff
}

a {
    color: #0366d6;
    text-decoration: none
}

a:hover {
    text-decoration: underline
}

b,strong {
    font-weight: 600
}

hr,.rule {
    height: 0;
    margin: 15px 0;
    overflow: hidden;
    background: transparent;
    border: 0;
    border-bottom: 1px solid #dfe2e5
}

hr::before,.rule::before {
    display: table;
    content: ""
}

hr::after,.rule::after {
    display: table;
    clear: both;
    content: ""
}

table {
    border-spacing: 0;
    border-collapse: collapse
}

td,th {
    padding: 0
}

button {
    cursor: pointer;
    border-radius: 0
}

[hidden][hidden] {
    display: none !important
}

details summary {
    cursor: pointer
}

details:not([open])>*:not(summary) {
    display: none !important
}

h1,h2,h3,h4,h5,h6 {
    margin-top: 0;
    margin-bottom: 0
}

h1 {
    font-size: 32px;
    font-weight: 600
}

h2 {
    font-size: 24px;
    font-weight: 600
}

h3 {
    font-size: 20px;
    font-weight: 600
}

h4 {
    font-size: 16px;
    font-weight: 600
}

h5 {
    font-size: 14px;
    font-weight: 600
}

h6 {
    font-size: 12px;
    font-weight: 600
}

p {
    margin-top: 0;
    margin-bottom: 10px
}

small {
    font-size: 90%
}

blockquote {
    margin: 0
}

ul,ol {
    padding-left: 0;
    margin-top: 0;
    margin-bottom: 0
}

ol ol,ul ol {
    list-style-type: lower-roman
}

ul ul ol,ul ol ol,ol ul ol,ol ol ol {
    list-style-type: lower-alpha
}

dd {
    margin-left: 0
}

tt,code {
    font-family: "SFMono-Regular",Consolas,"Liberation Mono",Menlo,Courier,monospace;
    font-size: 12px
}

pre {
    margin-top: 0;
    margin-bottom: 0;
    font-family: "SFMono-Regular",Consolas,"Liberation Mono",Menlo,Courier,monospace;
    font-size: 12px
}

.octicon {
    vertical-align: text-bottom
}

.anim-fade-in {
    animation-name: fade-in;
    animation-duration: 1s;
    animation-timing-function: ease-in-out
}

.anim-fade-in.fast {
    animation-duration: 300ms
}

@keyframes fade-in {
    0% {
        opacity: 0
    }

    100% {
        opacity: 1
    }
}

.anim-fade-out {
    animation-name: fade-out;
    animation-duration: 1s;
    animation-timing-function: ease-out
}

.anim-fade-out.fast {
    animation-duration: 0.3s
}

@keyframes fade-out {
    0% {
        opacity: 1
    }

    100% {
        opacity: 0
    }
}

.anim-fade-up {
    opacity: 0;
    animation-name: fade-up;
    animation-duration: 0.3s;
    animation-fill-mode: forwards;
    animation-timing-function: ease-out;
    animation-delay: 1s
}

@keyframes fade-up {
    0% {
        opacity: 0.8;
        transform: translateY(100%)
    }

    100% {
        opacity: 1;
        transform: translateY(0)
    }
}

.anim-fade-down {
    animation-name: fade-down;
    animation-duration: 0.3s;
    animation-fill-mode: forwards;
    animation-timing-function: ease-in
}

@keyframes fade-down {
    0% {
        opacity: 1;
        transform: translateY(0)
    }

    100% {
        opacity: 0.5;
        transform: translateY(100%)
    }
}

.anim-grow-x {
    width: 0%;
    animation-name: grow-x;
    animation-duration: 0.3s;
    animation-fill-mode: forwards;
    animation-timing-function: ease;
    animation-delay: 0.5s
}

@keyframes grow-x {
    to {
        width: 100%
    }
}

.anim-shrink-x {
    animation-name: shrink-x;
    animation-duration: 0.3s;
    animation-fill-mode: forwards;
    animation-timing-function: ease-in-out;
    animation-delay: 0.5s
}

@keyframes shrink-x {
    to {
        width: 0%
    }
}

.anim-scale-in {
    animation-name: scale-in;
    animation-duration: 0.15s;
    animation-timing-function: cubic-bezier(0.2, 0, 0.13, 1.5)
}

@keyframes scale-in {
    0% {
        opacity: 0;
        transform: scale(0.5)
    }

    100% {
        opacity: 1;
        transform: scale(1)
    }
}

.anim-pulse {
    animation-name: pulse;
    animation-duration: 2s;
    animation-timing-function: linear;
    animation-iteration-count: infinite
}

@keyframes pulse {
    0% {
        opacity: 0.3
    }

    10% {
        opacity: 1
    }

    100% {
        opacity: 0.3
    }
}

.anim-pulse-in {
    animation-name: pulse-in;
    animation-duration: 0.5s
}

@keyframes pulse-in {
    0% {
        transform: scale3d(1, 1, 1)
    }

    50% {
        transform: scale3d(1.1, 1.1, 1.1)
    }

    100% {
        transform: scale3d(1, 1, 1)
    }
}

.hover-grow {
    transition: transform 0.3s;
    backface-visibility: hidden
}

.hover-grow:hover {
    transform: scale(1.025)
}

.border {
    border: 1px #e1e4e8 solid !important
}

.border-y {
    border-top: 1px #e1e4e8 solid !important;
    border-bottom: 1px #e1e4e8 solid !important
}

.border-0 {
    border: 0 !important
}

.border-dashed {
    border-style: dashed !important
}

.border-blue {
    border-color: #0366d6 !important
}

.border-blue-light {
    border-color: #c8e1ff !important
}

.border-green {
    border-color: #34d058 !important
}

.border-green-light {
    border-color: #a2cbac !important
}

.border-red {
    border-color: #d73a49 !important
}

.border-red-light {
    border-color: #cea0a5 !important
}

.border-purple {
    border-color: #6f42c1 !important
}

.border-yellow {
    border-color: #d9d0a5 !important
}

.border-gray-light {
    border-color: #eaecef !important
}

.border-gray-dark {
    border-color: #d1d5da !important
}

.border-black-fade {
    border-color: rgba(27,31,35,0.15) !important
}

.border-top {
    border-top: 1px #e1e4e8 solid !important
}

.border-right {
    border-right: 1px #e1e4e8 solid !important
}

.border-bottom {
    border-bottom: 1px #e1e4e8 solid !important
}

.border-left {
    border-left: 1px #e1e4e8 solid !important
}

.border-top-0 {
    border-top: 0 !important
}

.border-right-0 {
    border-right: 0 !important
}

.border-bottom-0 {
    border-bottom: 0 !important
}

.border-left-0 {
    border-left: 0 !important
}

.rounded-0 {
    border-radius: 0 !important
}

.rounded-1 {
    border-radius: 3px !important
}

.rounded-2 {
    border-radius: 6px !important
}

.rounded-top-0 {
    border-top-left-radius: 0 !important;
    border-top-right-radius: 0 !important
}

.rounded-top-1 {
    border-top-left-radius: 3px !important;
    border-top-right-radius: 3px !important
}

.rounded-top-2 {
    border-top-left-radius: 6px !important;
    border-top-right-radius: 6px !important
}

.rounded-right-0 {
    border-top-right-radius: 0 !important;
    border-bottom-right-radius: 0 !important
}

.rounded-right-1 {
    border-top-right-radius: 3px !important;
    border-bottom-right-radius: 3px !important
}

.rounded-right-2 {
    border-top-right-radius: 6px !important;
    border-bottom-right-radius: 6px !important
}

.rounded-bottom-0 {
    border-bottom-right-radius: 0 !important;
    border-bottom-left-radius: 0 !important
}

.rounded-bottom-1 {
    border-bottom-right-radius: 3px !important;
    border-bottom-left-radius: 3px !important
}

.rounded-bottom-2 {
    border-bottom-right-radius: 6px !important;
    border-bottom-left-radius: 6px !important
}

.rounded-left-0 {
    border-bottom-left-radius: 0 !important;
    border-top-left-radius: 0 !important
}

.rounded-left-1 {
    border-bottom-left-radius: 3px !important;
    border-top-left-radius: 3px !important
}

.rounded-left-2 {
    border-bottom-left-radius: 6px !important;
    border-top-left-radius: 6px !important
}

@media (min-width: 544px) {
    .border-sm-top {
        border-top:1px #e1e4e8 solid !important
    }

    .border-sm-right {
        border-right: 1px #e1e4e8 solid !important
    }

    .border-sm-bottom {
        border-bottom: 1px #e1e4e8 solid !important
    }

    .border-sm-left {
        border-left: 1px #e1e4e8 solid !important
    }

    .border-sm-top-0 {
        border-top: 0 !important
    }

    .border-sm-right-0 {
        border-right: 0 !important
    }

    .border-sm-bottom-0 {
        border-bottom: 0 !important
    }

    .border-sm-left-0 {
        border-left: 0 !important
    }

    .rounded-sm-0 {
        border-radius: 0 !important
    }

    .rounded-sm-1 {
        border-radius: 3px !important
    }

    .rounded-sm-2 {
        border-radius: 6px !important
    }

    .rounded-sm-top-0 {
        border-top-left-radius: 0 !important;
        border-top-right-radius: 0 !important
    }

    .rounded-sm-top-1 {
        border-top-left-radius: 3px !important;
        border-top-right-radius: 3px !important
    }

    .rounded-sm-top-2 {
        border-top-left-radius: 6px !important;
        border-top-right-radius: 6px !important
    }

    .rounded-sm-right-0 {
        border-top-right-radius: 0 !important;
        border-bottom-right-radius: 0 !important
    }

    .rounded-sm-right-1 {
        border-top-right-radius: 3px !important;
        border-bottom-right-radius: 3px !important
    }

    .rounded-sm-right-2 {
        border-top-right-radius: 6px !important;
        border-bottom-right-radius: 6px !important
    }

    .rounded-sm-bottom-0 {
        border-bottom-right-radius: 0 !important;
        border-bottom-left-radius: 0 !important
    }

    .rounded-sm-bottom-1 {
        border-bottom-right-radius: 3px !important;
        border-bottom-left-radius: 3px !important
    }

    .rounded-sm-bottom-2 {
        border-bottom-right-radius: 6px !important;
        border-bottom-left-radius: 6px !important
    }

    .rounded-sm-left-0 {
        border-bottom-left-radius: 0 !important;
        border-top-left-radius: 0 !important
    }

    .rounded-sm-left-1 {
        border-bottom-left-radius: 3px !important;
        border-top-left-radius: 3px !important
    }

    .rounded-sm-left-2 {
        border-bottom-left-radius: 6px !important;
        border-top-left-radius: 6px !important
    }
}

@media (min-width: 768px) {
    .border-md-top {
        border-top:1px #e1e4e8 solid !important
    }

    .border-md-right {
        border-right: 1px #e1e4e8 solid !important
    }

    .border-md-bottom {
        border-bottom: 1px #e1e4e8 solid !important
    }

    .border-md-left {
        border-left: 1px #e1e4e8 solid !important
    }

    .border-md-top-0 {
        border-top: 0 !important
    }

    .border-md-right-0 {
        border-right: 0 !important
    }

    .border-md-bottom-0 {
        border-bottom: 0 !important
    }

    .border-md-left-0 {
        border-left: 0 !important
    }

    .rounded-md-0 {
        border-radius: 0 !important
    }

    .rounded-md-1 {
        border-radius: 3px !important
    }

    .rounded-md-2 {
        border-radius: 6px !important
    }

    .rounded-md-top-0 {
        border-top-left-radius: 0 !important;
        border-top-right-radius: 0 !important
    }

    .rounded-md-top-1 {
        border-top-left-radius: 3px !important;
        border-top-right-radius: 3px !important
    }

    .rounded-md-top-2 {
        border-top-left-radius: 6px !important;
        border-top-right-radius: 6px !important
    }

    .rounded-md-right-0 {
        border-top-right-radius: 0 !important;
        border-bottom-right-radius: 0 !important
    }

    .rounded-md-right-1 {
        border-top-right-radius: 3px !important;
        border-bottom-right-radius: 3px !important
    }

    .rounded-md-right-2 {
        border-top-right-radius: 6px !important;
        border-bottom-right-radius: 6px !important
    }

    .rounded-md-bottom-0 {
        border-bottom-right-radius: 0 !important;
        border-bottom-left-radius: 0 !important
    }

    .rounded-md-bottom-1 {
        border-bottom-right-radius: 3px !important;
        border-bottom-left-radius: 3px !important
    }

    .rounded-md-bottom-2 {
        border-bottom-right-radius: 6px !important;
        border-bottom-left-radius: 6px !important
    }

    .rounded-md-left-0 {
        border-bottom-left-radius: 0 !important;
        border-top-left-radius: 0 !important
    }

    .rounded-md-left-1 {
        border-bottom-left-radius: 3px !important;
        border-top-left-radius: 3px !important
    }

    .rounded-md-left-2 {
        border-bottom-left-radius: 6px !important;
        border-top-left-radius: 6px !important
    }
}

@media (min-width: 1012px) {
    .border-lg-top {
        border-top:1px #e1e4e8 solid !important
    }

    .border-lg-right {
        border-right: 1px #e1e4e8 solid !important
    }

    .border-lg-bottom {
        border-bottom: 1px #e1e4e8 solid !important
    }

    .border-lg-left {
        border-left: 1px #e1e4e8 solid !important
    }

    .border-lg-top-0 {
        border-top: 0 !important
    }

    .border-lg-right-0 {
        border-right: 0 !important
    }

    .border-lg-bottom-0 {
        border-bottom: 0 !important
    }

    .border-lg-left-0 {
        border-left: 0 !important
    }

    .rounded-lg-0 {
        border-radius: 0 !important
    }

    .rounded-lg-1 {
        border-radius: 3px !important
    }

    .rounded-lg-2 {
        border-radius: 6px !important
    }

    .rounded-lg-top-0 {
        border-top-left-radius: 0 !important;
        border-top-right-radius: 0 !important
    }

    .rounded-lg-top-1 {
        border-top-left-radius: 3px !important;
        border-top-right-radius: 3px !important
    }

    .rounded-lg-top-2 {
        border-top-left-radius: 6px !important;
        border-top-right-radius: 6px !important
    }

    .rounded-lg-right-0 {
        border-top-right-radius: 0 !important;
        border-bottom-right-radius: 0 !important
    }

    .rounded-lg-right-1 {
        border-top-right-radius: 3px !important;
        border-bottom-right-radius: 3px !important
    }

    .rounded-lg-right-2 {
        border-top-right-radius: 6px !important;
        border-bottom-right-radius: 6px !important
    }

    .rounded-lg-bottom-0 {
        border-bottom-right-radius: 0 !important;
        border-bottom-left-radius: 0 !important
    }

    .rounded-lg-bottom-1 {
        border-bottom-right-radius: 3px !important;
        border-bottom-left-radius: 3px !important
    }

    .rounded-lg-bottom-2 {
        border-bottom-right-radius: 6px !important;
        border-bottom-left-radius: 6px !important
    }

    .rounded-lg-left-0 {
        border-bottom-left-radius: 0 !important;
        border-top-left-radius: 0 !important
    }

    .rounded-lg-left-1 {
        border-bottom-left-radius: 3px !important;
        border-top-left-radius: 3px !important
    }

    .rounded-lg-left-2 {
        border-bottom-left-radius: 6px !important;
        border-top-left-radius: 6px !important
    }
}

@media (min-width: 1280px) {
    .border-xl-top {
        border-top:1px #e1e4e8 solid !important
    }

    .border-xl-right {
        border-right: 1px #e1e4e8 solid !important
    }

    .border-xl-bottom {
        border-bottom: 1px #e1e4e8 solid !important
    }

    .border-xl-left {
        border-left: 1px #e1e4e8 solid !important
    }

    .border-xl-top-0 {
        border-top: 0 !important
    }

    .border-xl-right-0 {
        border-right: 0 !important
    }

    .border-xl-bottom-0 {
        border-bottom: 0 !important
    }

    .border-xl-left-0 {
        border-left: 0 !important
    }

    .rounded-xl-0 {
        border-radius: 0 !important
    }

    .rounded-xl-1 {
        border-radius: 3px !important
    }

    .rounded-xl-2 {
        border-radius: 6px !important
    }

    .rounded-xl-top-0 {
        border-top-left-radius: 0 !important;
        border-top-right-radius: 0 !important
    }

    .rounded-xl-top-1 {
        border-top-left-radius: 3px !important;
        border-top-right-radius: 3px !important
    }

    .rounded-xl-top-2 {
        border-top-left-radius: 6px !important;
        border-top-right-radius: 6px !important
    }

    .rounded-xl-right-0 {
        border-top-right-radius: 0 !important;
        border-bottom-right-radius: 0 !important
    }

    .rounded-xl-right-1 {
        border-top-right-radius: 3px !important;
        border-bottom-right-radius: 3px !important
    }

    .rounded-xl-right-2 {
        border-top-right-radius: 6px !important;
        border-bottom-right-radius: 6px !important
    }

    .rounded-xl-bottom-0 {
        border-bottom-right-radius: 0 !important;
        border-bottom-left-radius: 0 !important
    }

    .rounded-xl-bottom-1 {
        border-bottom-right-radius: 3px !important;
        border-bottom-left-radius: 3px !important
    }

    .rounded-xl-bottom-2 {
        border-bottom-right-radius: 6px !important;
        border-bottom-left-radius: 6px !important
    }

    .rounded-xl-left-0 {
        border-bottom-left-radius: 0 !important;
        border-top-left-radius: 0 !important
    }

    .rounded-xl-left-1 {
        border-bottom-left-radius: 3px !important;
        border-top-left-radius: 3px !important
    }

    .rounded-xl-left-2 {
        border-bottom-left-radius: 6px !important;
        border-top-left-radius: 6px !important
    }
}

.circle {
    border-radius: 50% !important
}

.box-shadow {
    box-shadow: 0 1px 1px rgba(27,31,35,0.1) !important
}

.box-shadow-medium {
    box-shadow: 0 1px 5px rgba(27,31,35,0.15) !important
}

.box-shadow-large {
    box-shadow: 0 1px 15px rgba(27,31,35,0.15) !important
}

.box-shadow-extra-large {
    box-shadow: 0 10px 50px rgba(27,31,35,0.07) !important
}

.box-shadow-none {
    box-shadow: none !important
}

.bg-white {
    background-color: #fff !important
}

.bg-blue {
    background-color: #0366d6 !important
}

.bg-blue-light {
    background-color: #f1f8ff !important
}

.bg-gray-dark {
    background-color: #24292e !important
}

.bg-gray {
    background-color: #f6f8fa !important
}

.bg-gray-light {
    background-color: #fafbfc !important
}

.bg-green {
    background-color: #28a745 !important
}

.bg-green-light {
    background-color: #dcffe4 !important
}

.bg-red {
    background-color: #d73a49 !important
}

.bg-red-light {
    background-color: #ffdce0 !important
}

.bg-yellow {
    background-color: #ffd33d !important
}

.bg-yellow-light {
    background-color: #fff5b1 !important
}

.bg-purple {
    background-color: #6f42c1 !important
}

.bg-purple-light {
    background-color: #f5f0ff !important
}

.bg-shade-gradient {
    background-image: linear-gradient(180deg, rgba(27,31,35,0.065), rgba(27,31,35,0)) !important;
    background-repeat: no-repeat !important;
    background-size: 100% 200px !important
}

.text-blue {
    color: #0366d6 !important
}

.text-red {
    color: #cb2431 !important
}

.text-gray-light {
    color: #6a737d !important
}

.text-gray {
    color: #586069 !important
}

.text-gray-dark {
    color: #24292e !important
}

.text-green {
    color: #28a745 !important
}

.text-orange {
    color: #a04100 !important
}

.text-orange-light {
    color: #e36209 !important
}

.text-purple {
    color: #6f42c1 !important
}

.text-white {
    color: #fff !important
}

.text-inherit {
    color: inherit !important
}

.text-pending {
    color: #b08800 !important
}

.bg-pending {
    color: #dbab09 !important
}

.link-gray {
    color: #586069 !important
}

.link-gray:hover {
    color: #0366d6 !important
}

.link-gray-dark {
    color: #24292e !important
}

.link-gray-dark:hover {
    color: #0366d6 !important
}

.link-hover-blue:hover {
    color: #0366d6 !important
}

.muted-link {
    color: #586069 !important
}

.muted-link:hover {
    color: #0366d6 !important;
    text-decoration: none
}

.details-overlay[open]>summary::before {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 80;
    display: block;
    cursor: default;
    content: " ";
    background: transparent
}

.details-overlay-dark[open]>summary::before {
    z-index: 99;
    background: rgba(27,31,35,0.5)
}

.flex-row {
    flex-direction: row !important
}

.flex-row-reverse {
    flex-direction: row-reverse !important
}

.flex-column {
    flex-direction: column !important
}

.flex-wrap {
    flex-wrap: wrap !important
}

.flex-nowrap {
    flex-wrap: nowrap !important
}

.flex-justify-start {
    justify-content: flex-start !important
}

.flex-justify-end {
    justify-content: flex-end !important
}

.flex-justify-center {
    justify-content: center !important
}

.flex-justify-between {
    justify-content: space-between !important
}

.flex-justify-around {
    justify-content: space-around !important
}

.flex-items-start {
    align-items: flex-start !important
}

.flex-items-end {
    align-items: flex-end !important
}

.flex-items-center {
    align-items: center !important
}

.flex-items-baseline {
    align-items: baseline !important
}

.flex-items-stretch {
    align-items: stretch !important
}

.flex-content-start {
    align-content: flex-start !important
}

.flex-content-end {
    align-content: flex-end !important
}

.flex-content-center {
    align-content: center !important
}

.flex-content-between {
    align-content: space-between !important
}

.flex-content-around {
    align-content: space-around !important
}

.flex-content-stretch {
    align-content: stretch !important
}

.flex-auto {
    flex: 1 1 auto !important
}

.flex-shrink-0 {
    flex-shrink: 0 !important
}

.flex-self-auto {
    align-self: auto !important
}

.flex-self-start {
    align-self: flex-start !important
}

.flex-self-end {
    align-self: flex-end !important
}

.flex-self-center {
    align-self: center !important
}

.flex-self-baseline {
    align-self: baseline !important
}

.flex-self-stretch {
    align-self: stretch !important
}

.flex-item-equal {
    flex-grow: 1;
    flex-basis: 0
}

@media (min-width: 544px) {
    .flex-sm-row {
        flex-direction:row !important
    }

    .flex-sm-row-reverse {
        flex-direction: row-reverse !important
    }

    .flex-sm-column {
        flex-direction: column !important
    }

    .flex-sm-wrap {
        flex-wrap: wrap !important
    }

    .flex-sm-nowrap {
        flex-wrap: nowrap !important
    }

    .flex-sm-justify-start {
        justify-content: flex-start !important
    }

    .flex-sm-justify-end {
        justify-content: flex-end !important
    }

    .flex-sm-justify-center {
        justify-content: center !important
    }

    .flex-sm-justify-between {
        justify-content: space-between !important
    }

    .flex-sm-justify-around {
        justify-content: space-around !important
    }

    .flex-sm-items-start {
        align-items: flex-start !important
    }

    .flex-sm-items-end {
        align-items: flex-end !important
    }

    .flex-sm-items-center {
        align-items: center !important
    }

    .flex-sm-items-baseline {
        align-items: baseline !important
    }

    .flex-sm-items-stretch {
        align-items: stretch !important
    }

    .flex-sm-content-start {
        align-content: flex-start !important
    }

    .flex-sm-content-end {
        align-content: flex-end !important
    }

    .flex-sm-content-center {
        align-content: center !important
    }

    .flex-sm-content-between {
        align-content: space-between !important
    }

    .flex-sm-content-around {
        align-content: space-around !important
    }

    .flex-sm-content-stretch {
        align-content: stretch !important
    }

    .flex-sm-auto {
        flex: 1 1 auto !important
    }

    .flex-sm-shrink-0 {
        flex-shrink: 0 !important
    }

    .flex-sm-self-auto {
        align-self: auto !important
    }

    .flex-sm-self-start {
        align-self: flex-start !important
    }

    .flex-sm-self-end {
        align-self: flex-end !important
    }

    .flex-sm-self-center {
        align-self: center !important
    }

    .flex-sm-self-baseline {
        align-self: baseline !important
    }

    .flex-sm-self-stretch {
        align-self: stretch !important
    }

    .flex-sm-item-equal {
        flex-grow: 1;
        flex-basis: 0
    }
}

@media (min-width: 768px) {
    .flex-md-row {
        flex-direction:row !important
    }

    .flex-md-row-reverse {
        flex-direction: row-reverse !important
    }

    .flex-md-column {
        flex-direction: column !important
    }

    .flex-md-wrap {
        flex-wrap: wrap !important
    }

    .flex-md-nowrap {
        flex-wrap: nowrap !important
    }

    .flex-md-justify-start {
        justify-content: flex-start !important
    }

    .flex-md-justify-end {
        justify-content: flex-end !important
    }

    .flex-md-justify-center {
        justify-content: center !important
    }

    .flex-md-justify-between {
        justify-content: space-between !important
    }

    .flex-md-justify-around {
        justify-content: space-around !important
    }

    .flex-md-items-start {
        align-items: flex-start !important
    }

    .flex-md-items-end {
        align-items: flex-end !important
    }

    .flex-md-items-center {
        align-items: center !important
    }

    .flex-md-items-baseline {
        align-items: baseline !important
    }

    .flex-md-items-stretch {
        align-items: stretch !important
    }

    .flex-md-content-start {
        align-content: flex-start !important
    }

    .flex-md-content-end {
        align-content: flex-end !important
    }

    .flex-md-content-center {
        align-content: center !important
    }

    .flex-md-content-between {
        align-content: space-between !important
    }

    .flex-md-content-around {
        align-content: space-around !important
    }

    .flex-md-content-stretch {
        align-content: stretch !important
    }

    .flex-md-auto {
        flex: 1 1 auto !important
    }

    .flex-md-shrink-0 {
        flex-shrink: 0 !important
    }

    .flex-md-self-auto {
        align-self: auto !important
    }

    .flex-md-self-start {
        align-self: flex-start !important
    }

    .flex-md-self-end {
        align-self: flex-end !important
    }

    .flex-md-self-center {
        align-self: center !important
    }

    .flex-md-self-baseline {
        align-self: baseline !important
    }

    .flex-md-self-stretch {
        align-self: stretch !important
    }

    .flex-md-item-equal {
        flex-grow: 1;
        flex-basis: 0
    }
}

@media (min-width: 1012px) {
    .flex-lg-row {
        flex-direction:row !important
    }

    .flex-lg-row-reverse {
        flex-direction: row-reverse !important
    }

    .flex-lg-column {
        flex-direction: column !important
    }

    .flex-lg-wrap {
        flex-wrap: wrap !important
    }

    .flex-lg-nowrap {
        flex-wrap: nowrap !important
    }

    .flex-lg-justify-start {
        justify-content: flex-start !important
    }

    .flex-lg-justify-end {
        justify-content: flex-end !important
    }

    .flex-lg-justify-center {
        justify-content: center !important
    }

    .flex-lg-justify-between {
        justify-content: space-between !important
    }

    .flex-lg-justify-around {
        justify-content: space-around !important
    }

    .flex-lg-items-start {
        align-items: flex-start !important
    }

    .flex-lg-items-end {
        align-items: flex-end !important
    }

    .flex-lg-items-center {
        align-items: center !important
    }

    .flex-lg-items-baseline {
        align-items: baseline !important
    }

    .flex-lg-items-stretch {
        align-items: stretch !important
    }

    .flex-lg-content-start {
        align-content: flex-start !important
    }

    .flex-lg-content-end {
        align-content: flex-end !important
    }

    .flex-lg-content-center {
        align-content: center !important
    }

    .flex-lg-content-between {
        align-content: space-between !important
    }

    .flex-lg-content-around {
        align-content: space-around !important
    }

    .flex-lg-content-stretch {
        align-content: stretch !important
    }

    .flex-lg-auto {
        flex: 1 1 auto !important
    }

    .flex-lg-shrink-0 {
        flex-shrink: 0 !important
    }

    .flex-lg-self-auto {
        align-self: auto !important
    }

    .flex-lg-self-start {
        align-self: flex-start !important
    }

    .flex-lg-self-end {
        align-self: flex-end !important
    }

    .flex-lg-self-center {
        align-self: center !important
    }

    .flex-lg-self-baseline {
        align-self: baseline !important
    }

    .flex-lg-self-stretch {
        align-self: stretch !important
    }

    .flex-lg-item-equal {
        flex-grow: 1;
        flex-basis: 0
    }
}

@media (min-width: 1280px) {
    .flex-xl-row {
        flex-direction:row !important
    }

    .flex-xl-row-reverse {
        flex-direction: row-reverse !important
    }

    .flex-xl-column {
        flex-direction: column !important
    }

    .flex-xl-wrap {
        flex-wrap: wrap !important
    }

    .flex-xl-nowrap {
        flex-wrap: nowrap !important
    }

    .flex-xl-justify-start {
        justify-content: flex-start !important
    }

    .flex-xl-justify-end {
        justify-content: flex-end !important
    }

    .flex-xl-justify-center {
        justify-content: center !important
    }

    .flex-xl-justify-between {
        justify-content: space-between !important
    }

    .flex-xl-justify-around {
        justify-content: space-around !important
    }

    .flex-xl-items-start {
        align-items: flex-start !important
    }

    .flex-xl-items-end {
        align-items: flex-end !important
    }

    .flex-xl-items-center {
        align-items: center !important
    }

    .flex-xl-items-baseline {
        align-items: baseline !important
    }

    .flex-xl-items-stretch {
        align-items: stretch !important
    }

    .flex-xl-content-start {
        align-content: flex-start !important
    }

    .flex-xl-content-end {
        align-content: flex-end !important
    }

    .flex-xl-content-center {
        align-content: center !important
    }

    .flex-xl-content-between {
        align-content: space-between !important
    }

    .flex-xl-content-around {
        align-content: space-around !important
    }

    .flex-xl-content-stretch {
        align-content: stretch !important
    }

    .flex-xl-auto {
        flex: 1 1 auto !important
    }

    .flex-xl-shrink-0 {
        flex-shrink: 0 !important
    }

    .flex-xl-self-auto {
        align-self: auto !important
    }

    .flex-xl-self-start {
        align-self: flex-start !important
    }

    .flex-xl-self-end {
        align-self: flex-end !important
    }

    .flex-xl-self-center {
        align-self: center !important
    }

    .flex-xl-self-baseline {
        align-self: baseline !important
    }

    .flex-xl-self-stretch {
        align-self: stretch !important
    }

    .flex-xl-item-equal {
        flex-grow: 1;
        flex-basis: 0
    }
}

.position-static {
    position: static !important
}

.position-relative {
    position: relative !important
}

.position-absolute {
    position: absolute !important
}

.position-fixed {
    position: fixed !important
}

.top-0 {
    top: 0 !important
}

.right-0 {
    right: 0 !important
}

.bottom-0 {
    bottom: 0 !important
}

.left-0 {
    left: 0 !important
}

.v-align-middle {
    vertical-align: middle !important
}

.v-align-top {
    vertical-align: top !important
}

.v-align-bottom {
    vertical-align: bottom !important
}

.v-align-text-top {
    vertical-align: text-top !important
}

.v-align-text-bottom {
    vertical-align: text-bottom !important
}

.v-align-baseline {
    vertical-align: baseline !important
}

.overflow-hidden {
    overflow: hidden !important
}

.overflow-scroll {
    overflow: scroll !important
}

.overflow-auto {
    overflow: auto !important
}

.clearfix::before {
    display: table;
    content: ""
}

.clearfix::after {
    display: table;
    clear: both;
    content: ""
}

.float-left {
    float: left !important
}

.float-right {
    float: right !important
}

.float-none {
    float: none !important
}

@media (min-width: 544px) {
    .float-sm-left {
        float:left !important
    }

    .float-sm-right {
        float: right !important
    }

    .float-sm-none {
        float: none !important
    }
}

@media (min-width: 768px) {
    .float-md-left {
        float:left !important
    }

    .float-md-right {
        float: right !important
    }

    .float-md-none {
        float: none !important
    }
}

@media (min-width: 1012px) {
    .float-lg-left {
        float:left !important
    }

    .float-lg-right {
        float: right !important
    }

    .float-lg-none {
        float: none !important
    }
}

@media (min-width: 1280px) {
    .float-xl-left {
        float:left !important
    }

    .float-xl-right {
        float: right !important
    }

    .float-xl-none {
        float: none !important
    }
}

.width-fit {
    max-width: 100% !important
}

.width-full {
    width: 100% !important
}

.height-fit {
    max-height: 100% !important
}

.height-full {
    height: 100% !important
}

.min-width-0 {
    min-width: 0 !important
}

.direction-rtl {
    direction: rtl !important
}

.direction-ltr {
    direction: ltr !important
}

@media (min-width: 544px) {
    .direction-sm-rtl {
        direction:rtl !important
    }

    .direction-sm-ltr {
        direction: ltr !important
    }
}

@media (min-width: 768px) {
    .direction-md-rtl {
        direction:rtl !important
    }

    .direction-md-ltr {
        direction: ltr !important
    }
}

@media (min-width: 1012px) {
    .direction-lg-rtl {
        direction:rtl !important
    }

    .direction-lg-ltr {
        direction: ltr !important
    }
}

@media (min-width: 1280px) {
    .direction-xl-rtl {
        direction:rtl !important
    }

    .direction-xl-ltr {
        direction: ltr !important
    }
}

.m-0 {
    margin: 0 !important
}

.mt-0 {
    margin-top: 0 !important
}

.mr-0 {
    margin-right: 0 !important
}

.mb-0 {
    margin-bottom: 0 !important
}

.ml-0 {
    margin-left: 0 !important
}

.mx-0 {
    margin-right: 0 !important;
    margin-left: 0 !important
}

.my-0 {
    margin-top: 0 !important;
    margin-bottom: 0 !important
}

.m-1 {
    margin: 4px !important
}

.mt-1 {
    margin-top: 4px !important
}

.mr-1 {
    margin-right: 4px !important
}

.mb-1 {
    margin-bottom: 4px !important
}

.ml-1 {
    margin-left: 4px !important
}

.mt-n1 {
    margin-top: -4px !important
}

.mr-n1 {
    margin-right: -4px !important
}

.mb-n1 {
    margin-bottom: -4px !important
}

.ml-n1 {
    margin-left: -4px !important
}

.mx-1 {
    margin-right: 4px !important;
    margin-left: 4px !important
}

.my-1 {
    margin-top: 4px !important;
    margin-bottom: 4px !important
}

.m-2 {
    margin: 8px !important
}

.mt-2 {
    margin-top: 8px !important
}

.mr-2 {
    margin-right: 8px !important
}

.mb-2 {
    margin-bottom: 8px !important
}

.ml-2 {
    margin-left: 8px !important
}

.mt-n2 {
    margin-top: -8px !important
}

.mr-n2 {
    margin-right: -8px !important
}

.mb-n2 {
    margin-bottom: -8px !important
}

.ml-n2 {
    margin-left: -8px !important
}

.mx-2 {
    margin-right: 8px !important;
    margin-left: 8px !important
}

.my-2 {
    margin-top: 8px !important;
    margin-bottom: 8px !important
}

.m-3 {
    margin: 16px !important
}

.mt-3 {
    margin-top: 16px !important
}

.mr-3 {
    margin-right: 16px !important
}

.mb-3 {
    margin-bottom: 16px !important
}

.ml-3 {
    margin-left: 16px !important
}

.mt-n3 {
    margin-top: -16px !important
}

.mr-n3 {
    margin-right: -16px !important
}

.mb-n3 {
    margin-bottom: -16px !important
}

.ml-n3 {
    margin-left: -16px !important
}

.mx-3 {
    margin-right: 16px !important;
    margin-left: 16px !important
}

.my-3 {
    margin-top: 16px !important;
    margin-bottom: 16px !important
}

.m-4 {
    margin: 24px !important
}

.mt-4 {
    margin-top: 24px !important
}

.mr-4 {
    margin-right: 24px !important
}

.mb-4 {
    margin-bottom: 24px !important
}

.ml-4 {
    margin-left: 24px !important
}

.mt-n4 {
    margin-top: -24px !important
}

.mr-n4 {
    margin-right: -24px !important
}

.mb-n4 {
    margin-bottom: -24px !important
}

.ml-n4 {
    margin-left: -24px !important
}

.mx-4 {
    margin-right: 24px !important;
    margin-left: 24px !important
}

.my-4 {
    margin-top: 24px !important;
    margin-bottom: 24px !important
}

.m-5 {
    margin: 32px !important
}

.mt-5 {
    margin-top: 32px !important
}

.mr-5 {
    margin-right: 32px !important
}

.mb-5 {
    margin-bottom: 32px !important
}

.ml-5 {
    margin-left: 32px !important
}

.mt-n5 {
    margin-top: -32px !important
}

.mr-n5 {
    margin-right: -32px !important
}

.mb-n5 {
    margin-bottom: -32px !important
}

.ml-n5 {
    margin-left: -32px !important
}

.mx-5 {
    margin-right: 32px !important;
    margin-left: 32px !important
}

.my-5 {
    margin-top: 32px !important;
    margin-bottom: 32px !important
}

.m-6 {
    margin: 40px !important
}

.mt-6 {
    margin-top: 40px !important
}

.mr-6 {
    margin-right: 40px !important
}

.mb-6 {
    margin-bottom: 40px !important
}

.ml-6 {
    margin-left: 40px !important
}

.mt-n6 {
    margin-top: -40px !important
}

.mr-n6 {
    margin-right: -40px !important
}

.mb-n6 {
    margin-bottom: -40px !important
}

.ml-n6 {
    margin-left: -40px !important
}

.mx-6 {
    margin-right: 40px !important;
    margin-left: 40px !important
}

.my-6 {
    margin-top: 40px !important;
    margin-bottom: 40px !important
}

.mx-auto {
    margin-right: auto !important;
    margin-left: auto !important
}

@media (min-width: 544px) {
    .m-sm-0 {
        margin:0 !important
    }

    .mt-sm-0 {
        margin-top: 0 !important
    }

    .mr-sm-0 {
        margin-right: 0 !important
    }

    .mb-sm-0 {
        margin-bottom: 0 !important
    }

    .ml-sm-0 {
        margin-left: 0 !important
    }

    .mx-sm-0 {
        margin-right: 0 !important;
        margin-left: 0 !important
    }

    .my-sm-0 {
        margin-top: 0 !important;
        margin-bottom: 0 !important
    }

    .m-sm-1 {
        margin: 4px !important
    }

    .mt-sm-1 {
        margin-top: 4px !important
    }

    .mr-sm-1 {
        margin-right: 4px !important
    }

    .mb-sm-1 {
        margin-bottom: 4px !important
    }

    .ml-sm-1 {
        margin-left: 4px !important
    }

    .mt-sm-n1 {
        margin-top: -4px !important
    }

    .mr-sm-n1 {
        margin-right: -4px !important
    }

    .mb-sm-n1 {
        margin-bottom: -4px !important
    }

    .ml-sm-n1 {
        margin-left: -4px !important
    }

    .mx-sm-1 {
        margin-right: 4px !important;
        margin-left: 4px !important
    }

    .my-sm-1 {
        margin-top: 4px !important;
        margin-bottom: 4px !important
    }

    .m-sm-2 {
        margin: 8px !important
    }

    .mt-sm-2 {
        margin-top: 8px !important
    }

    .mr-sm-2 {
        margin-right: 8px !important
    }

    .mb-sm-2 {
        margin-bottom: 8px !important
    }

    .ml-sm-2 {
        margin-left: 8px !important
    }

    .mt-sm-n2 {
        margin-top: -8px !important
    }

    .mr-sm-n2 {
        margin-right: -8px !important
    }

    .mb-sm-n2 {
        margin-bottom: -8px !important
    }

    .ml-sm-n2 {
        margin-left: -8px !important
    }

    .mx-sm-2 {
        margin-right: 8px !important;
        margin-left: 8px !important
    }

    .my-sm-2 {
        margin-top: 8px !important;
        margin-bottom: 8px !important
    }

    .m-sm-3 {
        margin: 16px !important
    }

    .mt-sm-3 {
        margin-top: 16px !important
    }

    .mr-sm-3 {
        margin-right: 16px !important
    }

    .mb-sm-3 {
        margin-bottom: 16px !important
    }

    .ml-sm-3 {
        margin-left: 16px !important
    }

    .mt-sm-n3 {
        margin-top: -16px !important
    }

    .mr-sm-n3 {
        margin-right: -16px !important
    }

    .mb-sm-n3 {
        margin-bottom: -16px !important
    }

    .ml-sm-n3 {
        margin-left: -16px !important
    }

    .mx-sm-3 {
        margin-right: 16px !important;
        margin-left: 16px !important
    }

    .my-sm-3 {
        margin-top: 16px !important;
        margin-bottom: 16px !important
    }

    .m-sm-4 {
        margin: 24px !important
    }

    .mt-sm-4 {
        margin-top: 24px !important
    }

    .mr-sm-4 {
        margin-right: 24px !important
    }

    .mb-sm-4 {
        margin-bottom: 24px !important
    }

    .ml-sm-4 {
        margin-left: 24px !important
    }

    .mt-sm-n4 {
        margin-top: -24px !important
    }

    .mr-sm-n4 {
        margin-right: -24px !important
    }

    .mb-sm-n4 {
        margin-bottom: -24px !important
    }

    .ml-sm-n4 {
        margin-left: -24px !important
    }

    .mx-sm-4 {
        margin-right: 24px !important;
        margin-left: 24px !important
    }

    .my-sm-4 {
        margin-top: 24px !important;
        margin-bottom: 24px !important
    }

    .m-sm-5 {
        margin: 32px !important
    }

    .mt-sm-5 {
        margin-top: 32px !important
    }

    .mr-sm-5 {
        margin-right: 32px !important
    }

    .mb-sm-5 {
        margin-bottom: 32px !important
    }

    .ml-sm-5 {
        margin-left: 32px !important
    }

    .mt-sm-n5 {
        margin-top: -32px !important
    }

    .mr-sm-n5 {
        margin-right: -32px !important
    }

    .mb-sm-n5 {
        margin-bottom: -32px !important
    }

    .ml-sm-n5 {
        margin-left: -32px !important
    }

    .mx-sm-5 {
        margin-right: 32px !important;
        margin-left: 32px !important
    }

    .my-sm-5 {
        margin-top: 32px !important;
        margin-bottom: 32px !important
    }

    .m-sm-6 {
        margin: 40px !important
    }

    .mt-sm-6 {
        margin-top: 40px !important
    }

    .mr-sm-6 {
        margin-right: 40px !important
    }

    .mb-sm-6 {
        margin-bottom: 40px !important
    }

    .ml-sm-6 {
        margin-left: 40px !important
    }

    .mt-sm-n6 {
        margin-top: -40px !important
    }

    .mr-sm-n6 {
        margin-right: -40px !important
    }

    .mb-sm-n6 {
        margin-bottom: -40px !important
    }

    .ml-sm-n6 {
        margin-left: -40px !important
    }

    .mx-sm-6 {
        margin-right: 40px !important;
        margin-left: 40px !important
    }

    .my-sm-6 {
        margin-top: 40px !important;
        margin-bottom: 40px !important
    }

    .mx-sm-auto {
        margin-right: auto !important;
        margin-left: auto !important
    }
}

@media (min-width: 768px) {
    .m-md-0 {
        margin:0 !important
    }

    .mt-md-0 {
        margin-top: 0 !important
    }

    .mr-md-0 {
        margin-right: 0 !important
    }

    .mb-md-0 {
        margin-bottom: 0 !important
    }

    .ml-md-0 {
        margin-left: 0 !important
    }

    .mx-md-0 {
        margin-right: 0 !important;
        margin-left: 0 !important
    }

    .my-md-0 {
        margin-top: 0 !important;
        margin-bottom: 0 !important
    }

    .m-md-1 {
        margin: 4px !important
    }

    .mt-md-1 {
        margin-top: 4px !important
    }

    .mr-md-1 {
        margin-right: 4px !important
    }

    .mb-md-1 {
        margin-bottom: 4px !important
    }

    .ml-md-1 {
        margin-left: 4px !important
    }

    .mt-md-n1 {
        margin-top: -4px !important
    }

    .mr-md-n1 {
        margin-right: -4px !important
    }

    .mb-md-n1 {
        margin-bottom: -4px !important
    }

    .ml-md-n1 {
        margin-left: -4px !important
    }

    .mx-md-1 {
        margin-right: 4px !important;
        margin-left: 4px !important
    }

    .my-md-1 {
        margin-top: 4px !important;
        margin-bottom: 4px !important
    }

    .m-md-2 {
        margin: 8px !important
    }

    .mt-md-2 {
        margin-top: 8px !important
    }

    .mr-md-2 {
        margin-right: 8px !important
    }

    .mb-md-2 {
        margin-bottom: 8px !important
    }

    .ml-md-2 {
        margin-left: 8px !important
    }

    .mt-md-n2 {
        margin-top: -8px !important
    }

    .mr-md-n2 {
        margin-right: -8px !important
    }

    .mb-md-n2 {
        margin-bottom: -8px !important
    }

    .ml-md-n2 {
        margin-left: -8px !important
    }

    .mx-md-2 {
        margin-right: 8px !important;
        margin-left: 8px !important
    }

    .my-md-2 {
        margin-top: 8px !important;
        margin-bottom: 8px !important
    }

    .m-md-3 {
        margin: 16px !important
    }

    .mt-md-3 {
        margin-top: 16px !important
    }

    .mr-md-3 {
        margin-right: 16px !important
    }

    .mb-md-3 {
        margin-bottom: 16px !important
    }

    .ml-md-3 {
        margin-left: 16px !important
    }

    .mt-md-n3 {
        margin-top: -16px !important
    }

    .mr-md-n3 {
        margin-right: -16px !important
    }

    .mb-md-n3 {
        margin-bottom: -16px !important
    }

    .ml-md-n3 {
        margin-left: -16px !important
    }

    .mx-md-3 {
        margin-right: 16px !important;
        margin-left: 16px !important
    }

    .my-md-3 {
        margin-top: 16px !important;
        margin-bottom: 16px !important
    }

    .m-md-4 {
        margin: 24px !important
    }

    .mt-md-4 {
        margin-top: 24px !important
    }

    .mr-md-4 {
        margin-right: 24px !important
    }

    .mb-md-4 {
        margin-bottom: 24px !important
    }

    .ml-md-4 {
        margin-left: 24px !important
    }

    .mt-md-n4 {
        margin-top: -24px !important
    }

    .mr-md-n4 {
        margin-right: -24px !important
    }

    .mb-md-n4 {
        margin-bottom: -24px !important
    }

    .ml-md-n4 {
        margin-left: -24px !important
    }

    .mx-md-4 {
        margin-right: 24px !important;
        margin-left: 24px !important
    }

    .my-md-4 {
        margin-top: 24px !important;
        margin-bottom: 24px !important
    }

    .m-md-5 {
        margin: 32px !important
    }

    .mt-md-5 {
        margin-top: 32px !important
    }

    .mr-md-5 {
        margin-right: 32px !important
    }

    .mb-md-5 {
        margin-bottom: 32px !important
    }

    .ml-md-5 {
        margin-left: 32px !important
    }

    .mt-md-n5 {
        margin-top: -32px !important
    }

    .mr-md-n5 {
        margin-right: -32px !important
    }

    .mb-md-n5 {
        margin-bottom: -32px !important
    }

    .ml-md-n5 {
        margin-left: -32px !important
    }

    .mx-md-5 {
        margin-right: 32px !important;
        margin-left: 32px !important
    }

    .my-md-5 {
        margin-top: 32px !important;
        margin-bottom: 32px !important
    }

    .m-md-6 {
        margin: 40px !important
    }

    .mt-md-6 {
        margin-top: 40px !important
    }

    .mr-md-6 {
        margin-right: 40px !important
    }

    .mb-md-6 {
        margin-bottom: 40px !important
    }

    .ml-md-6 {
        margin-left: 40px !important
    }

    .mt-md-n6 {
        margin-top: -40px !important
    }

    .mr-md-n6 {
        margin-right: -40px !important
    }

    .mb-md-n6 {
        margin-bottom: -40px !important
    }

    .ml-md-n6 {
        margin-left: -40px !important
    }

    .mx-md-6 {
        margin-right: 40px !important;
        margin-left: 40px !important
    }

    .my-md-6 {
        margin-top: 40px !important;
        margin-bottom: 40px !important
    }

    .mx-md-auto {
        margin-right: auto !important;
        margin-left: auto !important
    }
}

@media (min-width: 1012px) {
    .m-lg-0 {
        margin:0 !important
    }

    .mt-lg-0 {
        margin-top: 0 !important
    }

    .mr-lg-0 {
        margin-right: 0 !important
    }

    .mb-lg-0 {
        margin-bottom: 0 !important
    }

    .ml-lg-0 {
        margin-left: 0 !important
    }

    .mx-lg-0 {
        margin-right: 0 !important;
        margin-left: 0 !important
    }

    .my-lg-0 {
        margin-top: 0 !important;
        margin-bottom: 0 !important
    }

    .m-lg-1 {
        margin: 4px !important
    }

    .mt-lg-1 {
        margin-top: 4px !important
    }

    .mr-lg-1 {
        margin-right: 4px !important
    }

    .mb-lg-1 {
        margin-bottom: 4px !important
    }

    .ml-lg-1 {
        margin-left: 4px !important
    }

    .mt-lg-n1 {
        margin-top: -4px !important
    }

    .mr-lg-n1 {
        margin-right: -4px !important
    }

    .mb-lg-n1 {
        margin-bottom: -4px !important
    }

    .ml-lg-n1 {
        margin-left: -4px !important
    }

    .mx-lg-1 {
        margin-right: 4px !important;
        margin-left: 4px !important
    }

    .my-lg-1 {
        margin-top: 4px !important;
        margin-bottom: 4px !important
    }

    .m-lg-2 {
        margin: 8px !important
    }

    .mt-lg-2 {
        margin-top: 8px !important
    }

    .mr-lg-2 {
        margin-right: 8px !important
    }

    .mb-lg-2 {
        margin-bottom: 8px !important
    }

    .ml-lg-2 {
        margin-left: 8px !important
    }

    .mt-lg-n2 {
        margin-top: -8px !important
    }

    .mr-lg-n2 {
        margin-right: -8px !important
    }

    .mb-lg-n2 {
        margin-bottom: -8px !important
    }

    .ml-lg-n2 {
        margin-left: -8px !important
    }

    .mx-lg-2 {
        margin-right: 8px !important;
        margin-left: 8px !important
    }

    .my-lg-2 {
        margin-top: 8px !important;
        margin-bottom: 8px !important
    }

    .m-lg-3 {
        margin: 16px !important
    }

    .mt-lg-3 {
        margin-top: 16px !important
    }

    .mr-lg-3 {
        margin-right: 16px !important
    }

    .mb-lg-3 {
        margin-bottom: 16px !important
    }

    .ml-lg-3 {
        margin-left: 16px !important
    }

    .mt-lg-n3 {
        margin-top: -16px !important
    }

    .mr-lg-n3 {
        margin-right: -16px !important
    }

    .mb-lg-n3 {
        margin-bottom: -16px !important
    }

    .ml-lg-n3 {
        margin-left: -16px !important
    }

    .mx-lg-3 {
        margin-right: 16px !important;
        margin-left: 16px !important
    }

    .my-lg-3 {
        margin-top: 16px !important;
        margin-bottom: 16px !important
    }

    .m-lg-4 {
        margin: 24px !important
    }

    .mt-lg-4 {
        margin-top: 24px !important
    }

    .mr-lg-4 {
        margin-right: 24px !important
    }

    .mb-lg-4 {
        margin-bottom: 24px !important
    }

    .ml-lg-4 {
        margin-left: 24px !important
    }

    .mt-lg-n4 {
        margin-top: -24px !important
    }

    .mr-lg-n4 {
        margin-right: -24px !important
    }

    .mb-lg-n4 {
        margin-bottom: -24px !important
    }

    .ml-lg-n4 {
        margin-left: -24px !important
    }

    .mx-lg-4 {
        margin-right: 24px !important;
        margin-left: 24px !important
    }

    .my-lg-4 {
        margin-top: 24px !important;
        margin-bottom: 24px !important
    }

    .m-lg-5 {
        margin: 32px !important
    }

    .mt-lg-5 {
        margin-top: 32px !important
    }

    .mr-lg-5 {
        margin-right: 32px !important
    }

    .mb-lg-5 {
        margin-bottom: 32px !important
    }

    .ml-lg-5 {
        margin-left: 32px !important
    }

    .mt-lg-n5 {
        margin-top: -32px !important
    }

    .mr-lg-n5 {
        margin-right: -32px !important
    }

    .mb-lg-n5 {
        margin-bottom: -32px !important
    }

    .ml-lg-n5 {
        margin-left: -32px !important
    }

    .mx-lg-5 {
        margin-right: 32px !important;
        margin-left: 32px !important
    }

    .my-lg-5 {
        margin-top: 32px !important;
        margin-bottom: 32px !important
    }

    .m-lg-6 {
        margin: 40px !important
    }

    .mt-lg-6 {
        margin-top: 40px !important
    }

    .mr-lg-6 {
        margin-right: 40px !important
    }

    .mb-lg-6 {
        margin-bottom: 40px !important
    }

    .ml-lg-6 {
        margin-left: 40px !important
    }

    .mt-lg-n6 {
        margin-top: -40px !important
    }

    .mr-lg-n6 {
        margin-right: -40px !important
    }

    .mb-lg-n6 {
        margin-bottom: -40px !important
    }

    .ml-lg-n6 {
        margin-left: -40px !important
    }

    .mx-lg-6 {
        margin-right: 40px !important;
        margin-left: 40px !important
    }

    .my-lg-6 {
        margin-top: 40px !important;
        margin-bottom: 40px !important
    }

    .mx-lg-auto {
        margin-right: auto !important;
        margin-left: auto !important
    }
}

@media (min-width: 1280px) {
    .m-xl-0 {
        margin:0 !important
    }

    .mt-xl-0 {
        margin-top: 0 !important
    }

    .mr-xl-0 {
        margin-right: 0 !important
    }

    .mb-xl-0 {
        margin-bottom: 0 !important
    }

    .ml-xl-0 {
        margin-left: 0 !important
    }

    .mx-xl-0 {
        margin-right: 0 !important;
        margin-left: 0 !important
    }

    .my-xl-0 {
        margin-top: 0 !important;
        margin-bottom: 0 !important
    }

    .m-xl-1 {
        margin: 4px !important
    }

    .mt-xl-1 {
        margin-top: 4px !important
    }

    .mr-xl-1 {
        margin-right: 4px !important
    }

    .mb-xl-1 {
        margin-bottom: 4px !important
    }

    .ml-xl-1 {
        margin-left: 4px !important
    }

    .mt-xl-n1 {
        margin-top: -4px !important
    }

    .mr-xl-n1 {
        margin-right: -4px !important
    }

    .mb-xl-n1 {
        margin-bottom: -4px !important
    }

    .ml-xl-n1 {
        margin-left: -4px !important
    }

    .mx-xl-1 {
        margin-right: 4px !important;
        margin-left: 4px !important
    }

    .my-xl-1 {
        margin-top: 4px !important;
        margin-bottom: 4px !important
    }

    .m-xl-2 {
        margin: 8px !important
    }

    .mt-xl-2 {
        margin-top: 8px !important
    }

    .mr-xl-2 {
        margin-right: 8px !important
    }

    .mb-xl-2 {
        margin-bottom: 8px !important
    }

    .ml-xl-2 {
        margin-left: 8px !important
    }

    .mt-xl-n2 {
        margin-top: -8px !important
    }

    .mr-xl-n2 {
        margin-right: -8px !important
    }

    .mb-xl-n2 {
        margin-bottom: -8px !important
    }

    .ml-xl-n2 {
        margin-left: -8px !important
    }

    .mx-xl-2 {
        margin-right: 8px !important;
        margin-left: 8px !important
    }

    .my-xl-2 {
        margin-top: 8px !important;
        margin-bottom: 8px !important
    }

    .m-xl-3 {
        margin: 16px !important
    }

    .mt-xl-3 {
        margin-top: 16px !important
    }

    .mr-xl-3 {
        margin-right: 16px !important
    }

    .mb-xl-3 {
        margin-bottom: 16px !important
    }

    .ml-xl-3 {
        margin-left: 16px !important
    }

    .mt-xl-n3 {
        margin-top: -16px !important
    }

    .mr-xl-n3 {
        margin-right: -16px !important
    }

    .mb-xl-n3 {
        margin-bottom: -16px !important
    }

    .ml-xl-n3 {
        margin-left: -16px !important
    }

    .mx-xl-3 {
        margin-right: 16px !important;
        margin-left: 16px !important
    }

    .my-xl-3 {
        margin-top: 16px !important;
        margin-bottom: 16px !important
    }

    .m-xl-4 {
        margin: 24px !important
    }

    .mt-xl-4 {
        margin-top: 24px !important
    }

    .mr-xl-4 {
        margin-right: 24px !important
    }

    .mb-xl-4 {
        margin-bottom: 24px !important
    }

    .ml-xl-4 {
        margin-left: 24px !important
    }

    .mt-xl-n4 {
        margin-top: -24px !important
    }

    .mr-xl-n4 {
        margin-right: -24px !important
    }

    .mb-xl-n4 {
        margin-bottom: -24px !important
    }

    .ml-xl-n4 {
        margin-left: -24px !important
    }

    .mx-xl-4 {
        margin-right: 24px !important;
        margin-left: 24px !important
    }

    .my-xl-4 {
        margin-top: 24px !important;
        margin-bottom: 24px !important
    }

    .m-xl-5 {
        margin: 32px !important
    }

    .mt-xl-5 {
        margin-top: 32px !important
    }

    .mr-xl-5 {
        margin-right: 32px !important
    }

    .mb-xl-5 {
        margin-bottom: 32px !important
    }

    .ml-xl-5 {
        margin-left: 32px !important
    }

    .mt-xl-n5 {
        margin-top: -32px !important
    }

    .mr-xl-n5 {
        margin-right: -32px !important
    }

    .mb-xl-n5 {
        margin-bottom: -32px !important
    }

    .ml-xl-n5 {
        margin-left: -32px !important
    }

    .mx-xl-5 {
        margin-right: 32px !important;
        margin-left: 32px !important
    }

    .my-xl-5 {
        margin-top: 32px !important;
        margin-bottom: 32px !important
    }

    .m-xl-6 {
        margin: 40px !important
    }

    .mt-xl-6 {
        margin-top: 40px !important
    }

    .mr-xl-6 {
        margin-right: 40px !important
    }

    .mb-xl-6 {
        margin-bottom: 40px !important
    }

    .ml-xl-6 {
        margin-left: 40px !important
    }

    .mt-xl-n6 {
        margin-top: -40px !important
    }

    .mr-xl-n6 {
        margin-right: -40px !important
    }

    .mb-xl-n6 {
        margin-bottom: -40px !important
    }

    .ml-xl-n6 {
        margin-left: -40px !important
    }

    .mx-xl-6 {
        margin-right: 40px !important;
        margin-left: 40px !important
    }

    .my-xl-6 {
        margin-top: 40px !important;
        margin-bottom: 40px !important
    }

    .mx-xl-auto {
        margin-right: auto !important;
        margin-left: auto !important
    }
}

.p-0 {
    padding: 0 !important
}

.pt-0 {
    padding-top: 0 !important
}

.pr-0 {
    padding-right: 0 !important
}

.pb-0 {
    padding-bottom: 0 !important
}

.pl-0 {
    padding-left: 0 !important
}

.px-0 {
    padding-right: 0 !important;
    padding-left: 0 !important
}

.py-0 {
    padding-top: 0 !important;
    padding-bottom: 0 !important
}

.p-1 {
    padding: 4px !important
}

.pt-1 {
    padding-top: 4px !important
}

.pr-1 {
    padding-right: 4px !important
}

.pb-1 {
    padding-bottom: 4px !important
}

.pl-1 {
    padding-left: 4px !important
}

.px-1 {
    padding-right: 4px !important;
    padding-left: 4px !important
}

.py-1 {
    padding-top: 4px !important;
    padding-bottom: 4px !important
}

.p-2 {
    padding: 8px !important
}

.pt-2 {
    padding-top: 8px !important
}

.pr-2 {
    padding-right: 8px !important
}

.pb-2 {
    padding-bottom: 8px !important
}

.pl-2 {
    padding-left: 8px !important
}

.px-2 {
    padding-right: 8px !important;
    padding-left: 8px !important
}

.py-2 {
    padding-top: 8px !important;
    padding-bottom: 8px !important
}

.p-3 {
    padding: 16px !important
}

.pt-3 {
    padding-top: 16px !important
}

.pr-3 {
    padding-right: 16px !important
}

.pb-3 {
    padding-bottom: 16px !important
}

.pl-3 {
    padding-left: 16px !important
}

.px-3 {
    padding-right: 16px !important;
    padding-left: 16px !important
}

.py-3 {
    padding-top: 16px !important;
    padding-bottom: 16px !important
}

.p-4 {
    padding: 24px !important
}

.pt-4 {
    padding-top: 24px !important
}

.pr-4 {
    padding-right: 24px !important
}

.pb-4 {
    padding-bottom: 24px !important
}

.pl-4 {
    padding-left: 24px !important
}

.px-4 {
    padding-right: 24px !important;
    padding-left: 24px !important
}

.py-4 {
    padding-top: 24px !important;
    padding-bottom: 24px !important
}

.p-5 {
    padding: 32px !important
}

.pt-5 {
    padding-top: 32px !important
}

.pr-5 {
    padding-right: 32px !important
}

.pb-5 {
    padding-bottom: 32px !important
}

.pl-5 {
    padding-left: 32px !important
}

.px-5 {
    padding-right: 32px !important;
    padding-left: 32px !important
}

.py-5 {
    padding-top: 32px !important;
    padding-bottom: 32px !important
}

.p-6 {
    padding: 40px !important
}

.pt-6 {
    padding-top: 40px !important
}

.pr-6 {
    padding-right: 40px !important
}

.pb-6 {
    padding-bottom: 40px !important
}

.pl-6 {
    padding-left: 40px !important
}

.px-6 {
    padding-right: 40px !important;
    padding-left: 40px !important
}

.py-6 {
    padding-top: 40px !important;
    padding-bottom: 40px !important
}

@media (min-width: 544px) {
    .p-sm-0 {
        padding:0 !important
    }

    .pt-sm-0 {
        padding-top: 0 !important
    }

    .pr-sm-0 {
        padding-right: 0 !important
    }

    .pb-sm-0 {
        padding-bottom: 0 !important
    }

    .pl-sm-0 {
        padding-left: 0 !important
    }

    .px-sm-0 {
        padding-right: 0 !important;
        padding-left: 0 !important
    }

    .py-sm-0 {
        padding-top: 0 !important;
        padding-bottom: 0 !important
    }

    .p-sm-1 {
        padding: 4px !important
    }

    .pt-sm-1 {
        padding-top: 4px !important
    }

    .pr-sm-1 {
        padding-right: 4px !important
    }

    .pb-sm-1 {
        padding-bottom: 4px !important
    }

    .pl-sm-1 {
        padding-left: 4px !important
    }

    .px-sm-1 {
        padding-right: 4px !important;
        padding-left: 4px !important
    }

    .py-sm-1 {
        padding-top: 4px !important;
        padding-bottom: 4px !important
    }

    .p-sm-2 {
        padding: 8px !important
    }

    .pt-sm-2 {
        padding-top: 8px !important
    }

    .pr-sm-2 {
        padding-right: 8px !important
    }

    .pb-sm-2 {
        padding-bottom: 8px !important
    }

    .pl-sm-2 {
        padding-left: 8px !important
    }

    .px-sm-2 {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .py-sm-2 {
        padding-top: 8px !important;
        padding-bottom: 8px !important
    }

    .p-sm-3 {
        padding: 16px !important
    }

    .pt-sm-3 {
        padding-top: 16px !important
    }

    .pr-sm-3 {
        padding-right: 16px !important
    }

    .pb-sm-3 {
        padding-bottom: 16px !important
    }

    .pl-sm-3 {
        padding-left: 16px !important
    }

    .px-sm-3 {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .py-sm-3 {
        padding-top: 16px !important;
        padding-bottom: 16px !important
    }

    .p-sm-4 {
        padding: 24px !important
    }

    .pt-sm-4 {
        padding-top: 24px !important
    }

    .pr-sm-4 {
        padding-right: 24px !important
    }

    .pb-sm-4 {
        padding-bottom: 24px !important
    }

    .pl-sm-4 {
        padding-left: 24px !important
    }

    .px-sm-4 {
        padding-right: 24px !important;
        padding-left: 24px !important
    }

    .py-sm-4 {
        padding-top: 24px !important;
        padding-bottom: 24px !important
    }

    .p-sm-5 {
        padding: 32px !important
    }

    .pt-sm-5 {
        padding-top: 32px !important
    }

    .pr-sm-5 {
        padding-right: 32px !important
    }

    .pb-sm-5 {
        padding-bottom: 32px !important
    }

    .pl-sm-5 {
        padding-left: 32px !important
    }

    .px-sm-5 {
        padding-right: 32px !important;
        padding-left: 32px !important
    }

    .py-sm-5 {
        padding-top: 32px !important;
        padding-bottom: 32px !important
    }

    .p-sm-6 {
        padding: 40px !important
    }

    .pt-sm-6 {
        padding-top: 40px !important
    }

    .pr-sm-6 {
        padding-right: 40px !important
    }

    .pb-sm-6 {
        padding-bottom: 40px !important
    }

    .pl-sm-6 {
        padding-left: 40px !important
    }

    .px-sm-6 {
        padding-right: 40px !important;
        padding-left: 40px !important
    }

    .py-sm-6 {
        padding-top: 40px !important;
        padding-bottom: 40px !important
    }
}

@media (min-width: 768px) {
    .p-md-0 {
        padding:0 !important
    }

    .pt-md-0 {
        padding-top: 0 !important
    }

    .pr-md-0 {
        padding-right: 0 !important
    }

    .pb-md-0 {
        padding-bottom: 0 !important
    }

    .pl-md-0 {
        padding-left: 0 !important
    }

    .px-md-0 {
        padding-right: 0 !important;
        padding-left: 0 !important
    }

    .py-md-0 {
        padding-top: 0 !important;
        padding-bottom: 0 !important
    }

    .p-md-1 {
        padding: 4px !important
    }

    .pt-md-1 {
        padding-top: 4px !important
    }

    .pr-md-1 {
        padding-right: 4px !important
    }

    .pb-md-1 {
        padding-bottom: 4px !important
    }

    .pl-md-1 {
        padding-left: 4px !important
    }

    .px-md-1 {
        padding-right: 4px !important;
        padding-left: 4px !important
    }

    .py-md-1 {
        padding-top: 4px !important;
        padding-bottom: 4px !important
    }

    .p-md-2 {
        padding: 8px !important
    }

    .pt-md-2 {
        padding-top: 8px !important
    }

    .pr-md-2 {
        padding-right: 8px !important
    }

    .pb-md-2 {
        padding-bottom: 8px !important
    }

    .pl-md-2 {
        padding-left: 8px !important
    }

    .px-md-2 {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .py-md-2 {
        padding-top: 8px !important;
        padding-bottom: 8px !important
    }

    .p-md-3 {
        padding: 16px !important
    }

    .pt-md-3 {
        padding-top: 16px !important
    }

    .pr-md-3 {
        padding-right: 16px !important
    }

    .pb-md-3 {
        padding-bottom: 16px !important
    }

    .pl-md-3 {
        padding-left: 16px !important
    }

    .px-md-3 {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .py-md-3 {
        padding-top: 16px !important;
        padding-bottom: 16px !important
    }

    .p-md-4 {
        padding: 24px !important
    }

    .pt-md-4 {
        padding-top: 24px !important
    }

    .pr-md-4 {
        padding-right: 24px !important
    }

    .pb-md-4 {
        padding-bottom: 24px !important
    }

    .pl-md-4 {
        padding-left: 24px !important
    }

    .px-md-4 {
        padding-right: 24px !important;
        padding-left: 24px !important
    }

    .py-md-4 {
        padding-top: 24px !important;
        padding-bottom: 24px !important
    }

    .p-md-5 {
        padding: 32px !important
    }

    .pt-md-5 {
        padding-top: 32px !important
    }

    .pr-md-5 {
        padding-right: 32px !important
    }

    .pb-md-5 {
        padding-bottom: 32px !important
    }

    .pl-md-5 {
        padding-left: 32px !important
    }

    .px-md-5 {
        padding-right: 32px !important;
        padding-left: 32px !important
    }

    .py-md-5 {
        padding-top: 32px !important;
        padding-bottom: 32px !important
    }

    .p-md-6 {
        padding: 40px !important
    }

    .pt-md-6 {
        padding-top: 40px !important
    }

    .pr-md-6 {
        padding-right: 40px !important
    }

    .pb-md-6 {
        padding-bottom: 40px !important
    }

    .pl-md-6 {
        padding-left: 40px !important
    }

    .px-md-6 {
        padding-right: 40px !important;
        padding-left: 40px !important
    }

    .py-md-6 {
        padding-top: 40px !important;
        padding-bottom: 40px !important
    }
}

@media (min-width: 1012px) {
    .p-lg-0 {
        padding:0 !important
    }

    .pt-lg-0 {
        padding-top: 0 !important
    }

    .pr-lg-0 {
        padding-right: 0 !important
    }

    .pb-lg-0 {
        padding-bottom: 0 !important
    }

    .pl-lg-0 {
        padding-left: 0 !important
    }

    .px-lg-0 {
        padding-right: 0 !important;
        padding-left: 0 !important
    }

    .py-lg-0 {
        padding-top: 0 !important;
        padding-bottom: 0 !important
    }

    .p-lg-1 {
        padding: 4px !important
    }

    .pt-lg-1 {
        padding-top: 4px !important
    }

    .pr-lg-1 {
        padding-right: 4px !important
    }

    .pb-lg-1 {
        padding-bottom: 4px !important
    }

    .pl-lg-1 {
        padding-left: 4px !important
    }

    .px-lg-1 {
        padding-right: 4px !important;
        padding-left: 4px !important
    }

    .py-lg-1 {
        padding-top: 4px !important;
        padding-bottom: 4px !important
    }

    .p-lg-2 {
        padding: 8px !important
    }

    .pt-lg-2 {
        padding-top: 8px !important
    }

    .pr-lg-2 {
        padding-right: 8px !important
    }

    .pb-lg-2 {
        padding-bottom: 8px !important
    }

    .pl-lg-2 {
        padding-left: 8px !important
    }

    .px-lg-2 {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .py-lg-2 {
        padding-top: 8px !important;
        padding-bottom: 8px !important
    }

    .p-lg-3 {
        padding: 16px !important
    }

    .pt-lg-3 {
        padding-top: 16px !important
    }

    .pr-lg-3 {
        padding-right: 16px !important
    }

    .pb-lg-3 {
        padding-bottom: 16px !important
    }

    .pl-lg-3 {
        padding-left: 16px !important
    }

    .px-lg-3 {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .py-lg-3 {
        padding-top: 16px !important;
        padding-bottom: 16px !important
    }

    .p-lg-4 {
        padding: 24px !important
    }

    .pt-lg-4 {
        padding-top: 24px !important
    }

    .pr-lg-4 {
        padding-right: 24px !important
    }

    .pb-lg-4 {
        padding-bottom: 24px !important
    }

    .pl-lg-4 {
        padding-left: 24px !important
    }

    .px-lg-4 {
        padding-right: 24px !important;
        padding-left: 24px !important
    }

    .py-lg-4 {
        padding-top: 24px !important;
        padding-bottom: 24px !important
    }

    .p-lg-5 {
        padding: 32px !important
    }

    .pt-lg-5 {
        padding-top: 32px !important
    }

    .pr-lg-5 {
        padding-right: 32px !important
    }

    .pb-lg-5 {
        padding-bottom: 32px !important
    }

    .pl-lg-5 {
        padding-left: 32px !important
    }

    .px-lg-5 {
        padding-right: 32px !important;
        padding-left: 32px !important
    }

    .py-lg-5 {
        padding-top: 32px !important;
        padding-bottom: 32px !important
    }

    .p-lg-6 {
        padding: 40px !important
    }

    .pt-lg-6 {
        padding-top: 40px !important
    }

    .pr-lg-6 {
        padding-right: 40px !important
    }

    .pb-lg-6 {
        padding-bottom: 40px !important
    }

    .pl-lg-6 {
        padding-left: 40px !important
    }

    .px-lg-6 {
        padding-right: 40px !important;
        padding-left: 40px !important
    }

    .py-lg-6 {
        padding-top: 40px !important;
        padding-bottom: 40px !important
    }
}

@media (min-width: 1280px) {
    .p-xl-0 {
        padding:0 !important
    }

    .pt-xl-0 {
        padding-top: 0 !important
    }

    .pr-xl-0 {
        padding-right: 0 !important
    }

    .pb-xl-0 {
        padding-bottom: 0 !important
    }

    .pl-xl-0 {
        padding-left: 0 !important
    }

    .px-xl-0 {
        padding-right: 0 !important;
        padding-left: 0 !important
    }

    .py-xl-0 {
        padding-top: 0 !important;
        padding-bottom: 0 !important
    }

    .p-xl-1 {
        padding: 4px !important
    }

    .pt-xl-1 {
        padding-top: 4px !important
    }

    .pr-xl-1 {
        padding-right: 4px !important
    }

    .pb-xl-1 {
        padding-bottom: 4px !important
    }

    .pl-xl-1 {
        padding-left: 4px !important
    }

    .px-xl-1 {
        padding-right: 4px !important;
        padding-left: 4px !important
    }

    .py-xl-1 {
        padding-top: 4px !important;
        padding-bottom: 4px !important
    }

    .p-xl-2 {
        padding: 8px !important
    }

    .pt-xl-2 {
        padding-top: 8px !important
    }

    .pr-xl-2 {
        padding-right: 8px !important
    }

    .pb-xl-2 {
        padding-bottom: 8px !important
    }

    .pl-xl-2 {
        padding-left: 8px !important
    }

    .px-xl-2 {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .py-xl-2 {
        padding-top: 8px !important;
        padding-bottom: 8px !important
    }

    .p-xl-3 {
        padding: 16px !important
    }

    .pt-xl-3 {
        padding-top: 16px !important
    }

    .pr-xl-3 {
        padding-right: 16px !important
    }

    .pb-xl-3 {
        padding-bottom: 16px !important
    }

    .pl-xl-3 {
        padding-left: 16px !important
    }

    .px-xl-3 {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .py-xl-3 {
        padding-top: 16px !important;
        padding-bottom: 16px !important
    }

    .p-xl-4 {
        padding: 24px !important
    }

    .pt-xl-4 {
        padding-top: 24px !important
    }

    .pr-xl-4 {
        padding-right: 24px !important
    }

    .pb-xl-4 {
        padding-bottom: 24px !important
    }

    .pl-xl-4 {
        padding-left: 24px !important
    }

    .px-xl-4 {
        padding-right: 24px !important;
        padding-left: 24px !important
    }

    .py-xl-4 {
        padding-top: 24px !important;
        padding-bottom: 24px !important
    }

    .p-xl-5 {
        padding: 32px !important
    }

    .pt-xl-5 {
        padding-top: 32px !important
    }

    .pr-xl-5 {
        padding-right: 32px !important
    }

    .pb-xl-5 {
        padding-bottom: 32px !important
    }

    .pl-xl-5 {
        padding-left: 32px !important
    }

    .px-xl-5 {
        padding-right: 32px !important;
        padding-left: 32px !important
    }

    .py-xl-5 {
        padding-top: 32px !important;
        padding-bottom: 32px !important
    }

    .p-xl-6 {
        padding: 40px !important
    }

    .pt-xl-6 {
        padding-top: 40px !important
    }

    .pr-xl-6 {
        padding-right: 40px !important
    }

    .pb-xl-6 {
        padding-bottom: 40px !important
    }

    .pl-xl-6 {
        padding-left: 40px !important
    }

    .px-xl-6 {
        padding-right: 40px !important;
        padding-left: 40px !important
    }

    .py-xl-6 {
        padding-top: 40px !important;
        padding-bottom: 40px !important
    }
}

.p-responsive {
    padding-right: 16px !important;
    padding-left: 16px !important
}

@media (min-width: 544px) {
    .p-responsive {
        padding-right:40px !important;
        padding-left: 40px !important
    }
}

@media (min-width: 1012px) {
    .p-responsive {
        padding-right:16px !important;
        padding-left: 16px !important
    }
}

.h1 {
    font-size: 26px !important
}

@media (min-width: 768px) {
    .h1 {
        font-size:32px !important
    }
}

.h2 {
    font-size: 22px !important
}

@media (min-width: 768px) {
    .h2 {
        font-size:24px !important
    }
}

.h3 {
    font-size: 18px !important
}

@media (min-width: 768px) {
    .h3 {
        font-size:20px !important
    }
}

.h4 {
    font-size: 16px !important
}

.h5 {
    font-size: 14px !important
}

.h6 {
    font-size: 12px !important
}

.h1,.h2,.h3,.h4,.h5,.h6 {
    font-weight: 600 !important
}

.f1 {
    font-size: 26px !important
}

@media (min-width: 768px) {
    .f1 {
        font-size:32px !important
    }
}

.f2 {
    font-size: 22px !important
}

@media (min-width: 768px) {
    .f2 {
        font-size:24px !important
    }
}

.f3 {
    font-size: 18px !important
}

@media (min-width: 768px) {
    .f3 {
        font-size:20px !important
    }
}

.f4 {
    font-size: 16px !important
}

@media (min-width: 768px) {
    .f4 {
        font-size:16px !important
    }
}

.f5 {
    font-size: 14px !important
}

.f6 {
    font-size: 12px !important
}

.f00-light {
    font-size: 40px !important;
    font-weight: 300 !important
}

@media (min-width: 768px) {
    .f00-light {
        font-size:48px !important
    }
}

.f0-light {
    font-size: 32px !important;
    font-weight: 300 !important
}

@media (min-width: 768px) {
    .f0-light {
        font-size:40px !important
    }
}

.f1-light {
    font-size: 26px !important;
    font-weight: 300 !important
}

@media (min-width: 768px) {
    .f1-light {
        font-size:32px !important
    }
}

.f2-light {
    font-size: 22px !important;
    font-weight: 300 !important
}

@media (min-width: 768px) {
    .f2-light {
        font-size:24px !important
    }
}

.f3-light {
    font-size: 18px !important;
    font-weight: 300 !important
}

@media (min-width: 768px) {
    .f3-light {
        font-size:20px !important
    }
}

.text-small {
    font-size: 12px !important
}

.lead {
    margin-bottom: 30px;
    font-size: 20px;
    font-weight: 300;
    color: #586069
}

.lh-condensed-ultra {
    line-height: 1 !important
}

.lh-condensed {
    line-height: 1.25 !important
}

.lh-default {
    line-height: 1.5 !important
}

.lh-0 {
    line-height: 0 !important
}

.text-right {
    text-align: right !important
}

.text-left {
    text-align: left !important
}

.text-center {
    text-align: center !important
}

@media (min-width: 544px) {
    .text-sm-right {
        text-align:right !important
    }

    .text-sm-left {
        text-align: left !important
    }

    .text-sm-center {
        text-align: center !important
    }
}

@media (min-width: 768px) {
    .text-md-right {
        text-align:right !important
    }

    .text-md-left {
        text-align: left !important
    }

    .text-md-center {
        text-align: center !important
    }
}

@media (min-width: 1012px) {
    .text-lg-right {
        text-align:right !important
    }

    .text-lg-left {
        text-align: left !important
    }

    .text-lg-center {
        text-align: center !important
    }
}

@media (min-width: 1280px) {
    .text-xl-right {
        text-align:right !important
    }

    .text-xl-left {
        text-align: left !important
    }

    .text-xl-center {
        text-align: center !important
    }
}

.text-normal {
    font-weight: 400 !important
}

.text-bold {
    font-weight: 600 !important
}

.text-italic {
    font-style: italic !important
}

.text-uppercase {
    text-transform: uppercase !important
}

.text-underline {
    text-decoration: underline !important
}

.no-underline {
    text-decoration: none !important
}

.no-wrap {
    white-space: nowrap !important
}

.ws-normal {
    white-space: normal !important
}

.wb-break-all {
    word-break: break-all !important
}

.text-emphasized {
    font-weight: 600;
    color: #24292e
}

.list-style-none {
    list-style: none !important
}

.text-shadow-dark {
    text-shadow: 0 1px 1px rgba(27,31,35,0.25),0 1px 25px rgba(27,31,35,0.75)
}

.text-shadow-light {
    text-shadow: 0 1px 0 rgba(255,255,255,0.5)
}

.text-mono {
    font-family: "SFMono-Regular",Consolas,"Liberation Mono",Menlo,Courier,monospace
}

.user-select-none {
    user-select: none !important
}

.d-block {
    display: block !important
}

.d-flex {
    display: flex !important
}

.d-inline {
    display: inline !important
}

.d-inline-block {
    display: inline-block !important
}

.d-inline-flex {
    display: inline-flex !important
}

.d-none {
    display: none !important
}

.d-table {
    display: table !important
}

.d-table-cell {
    display: table-cell !important
}

@media (min-width: 544px) {
    .d-sm-block {
        display:block !important
    }

    .d-sm-flex {
        display: flex !important
    }

    .d-sm-inline {
        display: inline !important
    }

    .d-sm-inline-block {
        display: inline-block !important
    }

    .d-sm-inline-flex {
        display: inline-flex !important
    }

    .d-sm-none {
        display: none !important
    }

    .d-sm-table {
        display: table !important
    }

    .d-sm-table-cell {
        display: table-cell !important
    }
}

@media (min-width: 768px) {
    .d-md-block {
        display:block !important
    }

    .d-md-flex {
        display: flex !important
    }

    .d-md-inline {
        display: inline !important
    }

    .d-md-inline-block {
        display: inline-block !important
    }

    .d-md-inline-flex {
        display: inline-flex !important
    }

    .d-md-none {
        display: none !important
    }

    .d-md-table {
        display: table !important
    }

    .d-md-table-cell {
        display: table-cell !important
    }
}

@media (min-width: 1012px) {
    .d-lg-block {
        display:block !important
    }

    .d-lg-flex {
        display: flex !important
    }

    .d-lg-inline {
        display: inline !important
    }

    .d-lg-inline-block {
        display: inline-block !important
    }

    .d-lg-inline-flex {
        display: inline-flex !important
    }

    .d-lg-none {
        display: none !important
    }

    .d-lg-table {
        display: table !important
    }

    .d-lg-table-cell {
        display: table-cell !important
    }
}

@media (min-width: 1280px) {
    .d-xl-block {
        display:block !important
    }

    .d-xl-flex {
        display: flex !important
    }

    .d-xl-inline {
        display: inline !important
    }

    .d-xl-inline-block {
        display: inline-block !important
    }

    .d-xl-inline-flex {
        display: inline-flex !important
    }

    .d-xl-none {
        display: none !important
    }

    .d-xl-table {
        display: table !important
    }

    .d-xl-table-cell {
        display: table-cell !important
    }
}

.v-hidden {
    visibility: hidden !important
}

.v-visible {
    visibility: visible !important
}

@media (max-width: 544px) {
    .hide-sm {
        display:none !important
    }
}

@media (min-width: 544px) and (max-width: 768px) {
    .hide-md {
        display:none !important
    }
}

@media (min-width: 768px) and (max-width: 1012px) {
    .hide-lg {
        display:none !important
    }
}

@media (min-width: 1012px) {
    .hide-xl {
        display:none !important
    }
}

.table-fixed {
    table-layout: fixed !important
}

.sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    word-wrap: normal;
    border: 0
}

.show-on-focus {
    position: absolute;
    width: 1px;
    height: 1px;
    margin: 0;
    overflow: hidden;
    clip: rect(1px, 1px, 1px, 1px)
}

.show-on-focus:focus {
    z-index: 20;
    width: auto;
    height: auto;
    clip: auto
}

.container {
    width: 980px;
    margin-right: auto;
    margin-left: auto
}

.container::before {
    display: table;
    content: ""
}

.container::after {
    display: table;
    clear: both;
    content: ""
}

.container-md {
    max-width: 768px;
    margin-right: auto;
    margin-left: auto
}

.container-lg {
    max-width: 1012px;
    margin-right: auto;
    margin-left: auto
}

.container-xl {
    max-width: 1280px;
    margin-right: auto;
    margin-left: auto
}

.columns {
    margin-right: -10px;
    margin-left: -10px
}

.columns::before {
    display: table;
    content: ""
}

.columns::after {
    display: table;
    clear: both;
    content: ""
}

.column {
    float: left;
    padding-right: 10px;
    padding-left: 10px
}

.one-third {
    width: 33.333333%
}

.two-thirds {
    width: 66.666667%
}

.one-fourth {
    width: 25%
}

.one-half {
    width: 50%
}

.three-fourths {
    width: 75%
}

.one-fifth {
    width: 20%
}

.four-fifths {
    width: 80%
}

.centered {
    display: block;
    float: none;
    margin-right: auto;
    margin-left: auto
}

.col-1 {
    width: 8.3333333333%
}

.col-2 {
    width: 16.6666666667%
}

.col-3 {
    width: 25%
}

.col-4 {
    width: 33.3333333333%
}

.col-5 {
    width: 41.6666666667%
}

.col-6 {
    width: 50%
}

.col-7 {
    width: 58.3333333333%
}

.col-8 {
    width: 66.6666666667%
}

.col-9 {
    width: 75%
}

.col-10 {
    width: 83.3333333333%
}

.col-11 {
    width: 91.6666666667%
}

.col-12 {
    width: 100%
}

@media (min-width: 544px) {
    .col-sm-1 {
        width:8.3333333333%
    }

    .col-sm-2 {
        width: 16.6666666667%
    }

    .col-sm-3 {
        width: 25%
    }

    .col-sm-4 {
        width: 33.3333333333%
    }

    .col-sm-5 {
        width: 41.6666666667%
    }

    .col-sm-6 {
        width: 50%
    }

    .col-sm-7 {
        width: 58.3333333333%
    }

    .col-sm-8 {
        width: 66.6666666667%
    }

    .col-sm-9 {
        width: 75%
    }

    .col-sm-10 {
        width: 83.3333333333%
    }

    .col-sm-11 {
        width: 91.6666666667%
    }

    .col-sm-12 {
        width: 100%
    }
}

@media (min-width: 768px) {
    .col-md-1 {
        width:8.3333333333%
    }

    .col-md-2 {
        width: 16.6666666667%
    }

    .col-md-3 {
        width: 25%
    }

    .col-md-4 {
        width: 33.3333333333%
    }

    .col-md-5 {
        width: 41.6666666667%
    }

    .col-md-6 {
        width: 50%
    }

    .col-md-7 {
        width: 58.3333333333%
    }

    .col-md-8 {
        width: 66.6666666667%
    }

    .col-md-9 {
        width: 75%
    }

    .col-md-10 {
        width: 83.3333333333%
    }

    .col-md-11 {
        width: 91.6666666667%
    }

    .col-md-12 {
        width: 100%
    }
}

@media (min-width: 1012px) {
    .col-lg-1 {
        width:8.3333333333%
    }

    .col-lg-2 {
        width: 16.6666666667%
    }

    .col-lg-3 {
        width: 25%
    }

    .col-lg-4 {
        width: 33.3333333333%
    }

    .col-lg-5 {
        width: 41.6666666667%
    }

    .col-lg-6 {
        width: 50%
    }

    .col-lg-7 {
        width: 58.3333333333%
    }

    .col-lg-8 {
        width: 66.6666666667%
    }

    .col-lg-9 {
        width: 75%
    }

    .col-lg-10 {
        width: 83.3333333333%
    }

    .col-lg-11 {
        width: 91.6666666667%
    }

    .col-lg-12 {
        width: 100%
    }
}

@media (min-width: 1280px) {
    .col-xl-1 {
        width:8.3333333333%
    }

    .col-xl-2 {
        width: 16.6666666667%
    }

    .col-xl-3 {
        width: 25%
    }

    .col-xl-4 {
        width: 33.3333333333%
    }

    .col-xl-5 {
        width: 41.6666666667%
    }

    .col-xl-6 {
        width: 50%
    }

    .col-xl-7 {
        width: 58.3333333333%
    }

    .col-xl-8 {
        width: 66.6666666667%
    }

    .col-xl-9 {
        width: 75%
    }

    .col-xl-10 {
        width: 83.3333333333%
    }

    .col-xl-11 {
        width: 91.6666666667%
    }

    .col-xl-12 {
        width: 100%
    }
}

.gutter {
    margin-right: -16px;
    margin-left: -16px
}

.gutter>[class*="col-"] {
    padding-right: 16px !important;
    padding-left: 16px !important
}

.gutter-condensed {
    margin-right: -8px;
    margin-left: -8px
}

.gutter-condensed>[class*="col-"] {
    padding-right: 8px !important;
    padding-left: 8px !important
}

.gutter-spacious {
    margin-right: -24px;
    margin-left: -24px
}

.gutter-spacious>[class*="col-"] {
    padding-right: 24px !important;
    padding-left: 24px !important
}

@media (min-width: 544px) {
    .gutter-sm {
        margin-right:-16px;
        margin-left: -16px
    }

    .gutter-sm>[class*="col-"] {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .gutter-sm-condensed {
        margin-right: -8px;
        margin-left: -8px
    }

    .gutter-sm-condensed>[class*="col-"] {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .gutter-sm-spacious {
        margin-right: -24px;
        margin-left: -24px
    }

    .gutter-sm-spacious>[class*="col-"] {
        padding-right: 24px !important;
        padding-left: 24px !important
    }
}

@media (min-width: 768px) {
    .gutter-md {
        margin-right:-16px;
        margin-left: -16px
    }

    .gutter-md>[class*="col-"] {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .gutter-md-condensed {
        margin-right: -8px;
        margin-left: -8px
    }

    .gutter-md-condensed>[class*="col-"] {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .gutter-md-spacious {
        margin-right: -24px;
        margin-left: -24px
    }

    .gutter-md-spacious>[class*="col-"] {
        padding-right: 24px !important;
        padding-left: 24px !important
    }
}

@media (min-width: 1012px) {
    .gutter-lg {
        margin-right:-16px;
        margin-left: -16px
    }

    .gutter-lg>[class*="col-"] {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .gutter-lg-condensed {
        margin-right: -8px;
        margin-left: -8px
    }

    .gutter-lg-condensed>[class*="col-"] {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .gutter-lg-spacious {
        margin-right: -24px;
        margin-left: -24px
    }

    .gutter-lg-spacious>[class*="col-"] {
        padding-right: 24px !important;
        padding-left: 24px !important
    }
}

@media (min-width: 1280px) {
    .gutter-xl {
        margin-right:-16px;
        margin-left: -16px
    }

    .gutter-xl>[class*="col-"] {
        padding-right: 16px !important;
        padding-left: 16px !important
    }

    .gutter-xl-condensed {
        margin-right: -8px;
        margin-left: -8px
    }

    .gutter-xl-condensed>[class*="col-"] {
        padding-right: 8px !important;
        padding-left: 8px !important
    }

    .gutter-xl-spacious {
        margin-right: -24px;
        margin-left: -24px
    }

    .gutter-xl-spacious>[class*="col-"] {
        padding-right: 24px !important;
        padding-left: 24px !important
    }
}

.offset-1 {
    margin-left: 8.3333333333% !important
}

.offset-2 {
    margin-left: 16.6666666667% !important
}

.offset-3 {
    margin-left: 25% !important
}

.offset-4 {
    margin-left: 33.3333333333% !important
}

.offset-5 {
    margin-left: 41.6666666667% !important
}

.offset-6 {
    margin-left: 50% !important
}

.offset-7 {
    margin-left: 58.3333333333% !important
}

.offset-8 {
    margin-left: 66.6666666667% !important
}

.offset-9 {
    margin-left: 75% !important
}

.offset-10 {
    margin-left: 83.3333333333% !important
}

.offset-11 {
    margin-left: 91.6666666667% !important
}

@media (min-width: 544px) {
    .offset-sm-1 {
        margin-left:8.3333333333% !important
    }

    .offset-sm-2 {
        margin-left: 16.6666666667% !important
    }

    .offset-sm-3 {
        margin-left: 25% !important
    }

    .offset-sm-4 {
        margin-left: 33.3333333333% !important
    }

    .offset-sm-5 {
        margin-left: 41.6666666667% !important
    }

    .offset-sm-6 {
        margin-left: 50% !important
    }

    .offset-sm-7 {
        margin-left: 58.3333333333% !important
    }

    .offset-sm-8 {
        margin-left: 66.6666666667% !important
    }

    .offset-sm-9 {
        margin-left: 75% !important
    }

    .offset-sm-10 {
        margin-left: 83.3333333333% !important
    }

    .offset-sm-11 {
        margin-left: 91.6666666667% !important
    }
}

@media (min-width: 768px) {
    .offset-md-1 {
        margin-left:8.3333333333% !important
    }

    .offset-md-2 {
        margin-left: 16.6666666667% !important
    }

    .offset-md-3 {
        margin-left: 25% !important
    }

    .offset-md-4 {
        margin-left: 33.3333333333% !important
    }

    .offset-md-5 {
        margin-left: 41.6666666667% !important
    }

    .offset-md-6 {
        margin-left: 50% !important
    }

    .offset-md-7 {
        margin-left: 58.3333333333% !important
    }

    .offset-md-8 {
        margin-left: 66.6666666667% !important
    }

    .offset-md-9 {
        margin-left: 75% !important
    }

    .offset-md-10 {
        margin-left: 83.3333333333% !important
    }

    .offset-md-11 {
        margin-left: 91.6666666667% !important
    }
}

@media (min-width: 1012px) {
    .offset-lg-1 {
        margin-left:8.3333333333% !important
    }

    .offset-lg-2 {
        margin-left: 16.6666666667% !important
    }

    .offset-lg-3 {
        margin-left: 25% !important
    }

    .offset-lg-4 {
        margin-left: 33.3333333333% !important
    }

    .offset-lg-5 {
        margin-left: 41.6666666667% !important
    }

    .offset-lg-6 {
        margin-left: 50% !important
    }

    .offset-lg-7 {
        margin-left: 58.3333333333% !important
    }

    .offset-lg-8 {
        margin-left: 66.6666666667% !important
    }

    .offset-lg-9 {
        margin-left: 75% !important
    }

    .offset-lg-10 {
        margin-left: 83.3333333333% !important
    }

    .offset-lg-11 {
        margin-left: 91.6666666667% !important
    }
}

@media (min-width: 1280px) {
    .offset-xl-1 {
        margin-left:8.3333333333% !important
    }

    .offset-xl-2 {
        margin-left: 16.6666666667% !important
    }

    .offset-xl-3 {
        margin-left: 25% !important
    }

    .offset-xl-4 {
        margin-left: 33.3333333333% !important
    }

    .offset-xl-5 {
        margin-left: 41.6666666667% !important
    }

    .offset-xl-6 {
        margin-left: 50% !important
    }

    .offset-xl-7 {
        margin-left: 58.3333333333% !important
    }

    .offset-xl-8 {
        margin-left: 66.6666666667% !important
    }

    .offset-xl-9 {
        margin-left: 75% !important
    }

    .offset-xl-10 {
        margin-left: 83.3333333333% !important
    }

    .offset-xl-11 {
        margin-left: 91.6666666667% !important
    }
}

.markdown-body {
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-size: 16px;
    line-height: 1.5;
    word-wrap: break-word
}

.markdown-body::before {
    display: table;
    content: ""
}

.markdown-body::after {
    display: table;
    clear: both;
    content: ""
}

.markdown-body>*:first-child {
    margin-top: 0 !important
}

.markdown-body>*:last-child {
    margin-bottom: 0 !important
}

.markdown-body a:not([href]) {
    color: inherit;
    text-decoration: none
}

.markdown-body .absent {
    color: #cb2431
}

.markdown-body .anchor {
    float: left;
    padding-right: 4px;
    margin-left: -20px;
    line-height: 1
}

.markdown-body .anchor:focus {
    outline: none
}

.markdown-body p,.markdown-body blockquote,.markdown-body ul,.markdown-body ol,.markdown-body dl,.markdown-body table,.markdown-body pre {
    margin-top: 0;
    margin-bottom: 16px
}

.markdown-body hr {
    height: .25em;
    padding: 0;
    margin: 24px 0;
    background-color: #e1e4e8;
    border: 0
}

.markdown-body blockquote {
    padding: 0 1em;
    color: #6a737d;
    border-left: 0.25em solid #dfe2e5
}

.markdown-body blockquote>:first-child {
    margin-top: 0
}

.markdown-body blockquote>:last-child {
    margin-bottom: 0
}

.markdown-body kbd {
    display: inline-block;
    padding: 3px 5px;
    font-size: 11px;
    line-height: 10px;
    color: #444d56;
    vertical-align: middle;
    background-color: #fafbfc;
    border: solid 1px #c6cbd1;
    border-bottom-color: #959da5;
    border-radius: 3px;
    box-shadow: inset 0 -1px 0 #959da5
}

.markdown-body h1,.markdown-body h2,.markdown-body h3,.markdown-body h4,.markdown-body h5,.markdown-body h6 {
    margin-top: 24px;
    margin-bottom: 16px;
    font-weight: 600;
    line-height: 1.25
}

.markdown-body h1 .octicon-link,.markdown-body h2 .octicon-link,.markdown-body h3 .octicon-link,.markdown-body h4 .octicon-link,.markdown-body h5 .octicon-link,.markdown-body h6 .octicon-link {
    color: #1b1f23;
    vertical-align: middle;
    visibility: hidden
}

.markdown-body h1:hover .anchor,.markdown-body h2:hover .anchor,.markdown-body h3:hover .anchor,.markdown-body h4:hover .anchor,.markdown-body h5:hover .anchor,.markdown-body h6:hover .anchor {
    text-decoration: none
}

.markdown-body h1:hover .anchor .octicon-link,.markdown-body h2:hover .anchor .octicon-link,.markdown-body h3:hover .anchor .octicon-link,.markdown-body h4:hover .anchor .octicon-link,.markdown-body h5:hover .anchor .octicon-link,.markdown-body h6:hover .anchor .octicon-link {
    visibility: visible
}

.markdown-body h1 tt,.markdown-body h1 code,.markdown-body h2 tt,.markdown-body h2 code,.markdown-body h3 tt,.markdown-body h3 code,.markdown-body h4 tt,.markdown-body h4 code,.markdown-body h5 tt,.markdown-body h5 code,.markdown-body h6 tt,.markdown-body h6 code {
    font-size: inherit
}

.markdown-body h1 {
    padding-bottom: 0.3em;
    font-size: 2em;
    border-bottom: 1px solid #eaecef
}

.markdown-body h2 {
    padding-bottom: 0.3em;
    font-size: 1.5em;
    border-bottom: 1px solid #eaecef
}

.markdown-body h3 {
    font-size: 1.25em
}

.markdown-body h4 {
    font-size: 1em
}

.markdown-body h5 {
    font-size: 0.875em
}

.markdown-body h6 {
    font-size: 0.85em;
    color: #6a737d
}

.markdown-body ul,.markdown-body ol {
    padding-left: 2em
}

.markdown-body ul.no-list,.markdown-body ol.no-list {
    padding: 0;
    list-style-type: none
}

.markdown-body ul ul,.markdown-body ul ol,.markdown-body ol ol,.markdown-body ol ul {
    margin-top: 0;
    margin-bottom: 0
}

.markdown-body li {
    word-wrap: break-all
}

.markdown-body li>p {
    margin-top: 16px
}

.markdown-body li+li {
    margin-top: .25em
}

.markdown-body dl {
    padding: 0
}

.markdown-body dl dt {
    padding: 0;
    margin-top: 16px;
    font-size: 1em;
    font-style: italic;
    font-weight: 600
}

.markdown-body dl dd {
    padding: 0 16px;
    margin-bottom: 16px
}

.markdown-body table {
    display: block;
    width: 100%;
    overflow: auto
}

.markdown-body table th {
    font-weight: 600
}

.markdown-body table th,.markdown-body table td {
    padding: 6px 13px;
    border: 1px solid #dfe2e5
}

.markdown-body table tr {
    background-color: #fff;
    border-top: 1px solid #c6cbd1
}

.markdown-body table tr:nth-child(2n) {
    background-color: #f6f8fa
}

.markdown-body table img {
    background-color: transparent
}

.markdown-body img {
    max-width: 100%;
    box-sizing: content-box;
    background-color: #fff
}

.markdown-body img[align=right] {
    padding-left: 20px
}

.markdown-body img[align=left] {
    padding-right: 20px
}

.markdown-body .emoji {
    max-width: none;
    vertical-align: text-top;
    background-color: transparent
}

.markdown-body span.frame {
    display: block;
    overflow: hidden
}

.markdown-body span.frame>span {
    display: block;
    float: left;
    width: auto;
    padding: 7px;
    margin: 13px 0 0;
    overflow: hidden;
    border: 1px solid #dfe2e5
}

.markdown-body span.frame span img {
    display: block;
    float: left
}

.markdown-body span.frame span span {
    display: block;
    padding: 5px 0 0;
    clear: both;
    color: #24292e
}

.markdown-body span.align-center {
    display: block;
    overflow: hidden;
    clear: both
}

.markdown-body span.align-center>span {
    display: block;
    margin: 13px auto 0;
    overflow: hidden;
    text-align: center
}

.markdown-body span.align-center span img {
    margin: 0 auto;
    text-align: center
}

.markdown-body span.align-right {
    display: block;
    overflow: hidden;
    clear: both
}

.markdown-body span.align-right>span {
    display: block;
    margin: 13px 0 0;
    overflow: hidden;
    text-align: right
}

.markdown-body span.align-right span img {
    margin: 0;
    text-align: right
}

.markdown-body span.float-left {
    display: block;
    float: left;
    margin-right: 13px;
    overflow: hidden
}

.markdown-body span.float-left span {
    margin: 13px 0 0
}

.markdown-body span.float-right {
    display: block;
    float: right;
    margin-left: 13px;
    overflow: hidden
}

.markdown-body span.float-right>span {
    display: block;
    margin: 13px auto 0;
    overflow: hidden;
    text-align: right
}

.markdown-body code,.markdown-body tt {
    padding: 0.2em 0.4em;
    margin: 0;
    font-size: 85%;
    background-color: rgba(27,31,35,0.05);
    border-radius: 3px
}

.markdown-body code br,.markdown-body tt br {
    display: none
}

.markdown-body del code {
    text-decoration: inherit
}

.markdown-body pre {
    word-wrap: normal
}

.markdown-body pre>code {
    padding: 0;
    margin: 0;
    font-size: 100%;
    word-break: normal;
    white-space: pre;
    background: transparent;
    border: 0
}

.markdown-body .highlight {
    margin-bottom: 16px
}

.markdown-body .highlight pre {
    margin-bottom: 0;
    word-break: normal
}

.markdown-body .highlight pre,.markdown-body pre {
    padding: 16px;
    overflow: auto;
    font-size: 85%;
    line-height: 1.45;
    background-color: #f6f8fa;
    border-radius: 3px
}

.markdown-body pre code,.markdown-body pre tt {
    display: inline;
    max-width: auto;
    padding: 0;
    margin: 0;
    overflow: visible;
    line-height: inherit;
    word-wrap: normal;
    background-color: transparent;
    border: 0
}

.markdown-body .csv-data td,.markdown-body .csv-data th {
    padding: 5px;
    overflow: hidden;
    font-size: 12px;
    line-height: 1;
    text-align: left;
    white-space: nowrap
}

.markdown-body .csv-data .blob-num {
    padding: 10px 8px 9px;
    text-align: right;
    background: #fff;
    border: 0
}

.markdown-body .csv-data tr {
    border-top: 0
}

.markdown-body .csv-data th {
    font-weight: 600;
    background: #f6f8fa;
    border-top: 0
}

.highlight table td {
    padding: 5px
}

.highlight table pre {
    margin: 0
}

.highlight .cm {
    color: #999988;
    font-style: italic
}

.highlight .cp {
    color: #999999;
    font-weight: bold
}

.highlight .c1 {
    color: #999988;
    font-style: italic
}

.highlight .cs {
    color: #999999;
    font-weight: bold;
    font-style: italic
}

.highlight .c,.highlight .cd {
    color: #999988;
    font-style: italic
}

.highlight .err {
    color: #a61717;
    background-color: #e3d2d2
}

.highlight .gd {
    color: #000000;
    background-color: #ffdddd
}

.highlight .ge {
    color: #000000;
    font-style: italic
}

.highlight .gr {
    color: #aa0000
}

.highlight .gh {
    color: #999999
}

.highlight .gi {
    color: #000000;
    background-color: #ddffdd
}

.highlight .go {
    color: #888888
}

.highlight .gp {
    color: #555555
}

.highlight .gs {
    font-weight: bold
}

.highlight .gu {
    color: #aaaaaa
}

.highlight .gt {
    color: #aa0000
}

.highlight .kc {
    color: #000000;
    font-weight: bold
}

.highlight .kd {
    color: #000000;
    font-weight: bold
}

.highlight .kn {
    color: #000000;
    font-weight: bold
}

.highlight .kp {
    color: #000000;
    font-weight: bold
}

.highlight .kr {
    color: #000000;
    font-weight: bold
}

.highlight .kt {
    color: #445588;
    font-weight: bold
}

.highlight .k,.highlight .kv {
    color: #000000;
    font-weight: bold
}

.highlight .mf {
    color: #009999
}

.highlight .mh {
    color: #009999
}

.highlight .il {
    color: #009999
}

.highlight .mi {
    color: #009999
}

.highlight .mo {
    color: #009999
}

.highlight .m,.highlight .mb,.highlight .mx {
    color: #009999
}

.highlight .sb {
    color: #d14
}

.highlight .sc {
    color: #d14
}

.highlight .sd {
    color: #d14
}

.highlight .s2 {
    color: #d14
}

.highlight .se {
    color: #d14
}

.highlight .sh {
    color: #d14
}

.highlight .si {
    color: #d14
}

.highlight .sx {
    color: #d14
}

.highlight .sr {
    color: #009926
}

.highlight .s1 {
    color: #d14
}

.highlight .ss {
    color: #990073
}

.highlight .s {
    color: #d14
}

.highlight .na {
    color: #008080
}

.highlight .bp {
    color: #999999
}

.highlight .nb {
    color: #0086B3
}

.highlight .nc {
    color: #445588;
    font-weight: bold
}

.highlight .no {
    color: #008080
}

.highlight .nd {
    color: #3c5d5d;
    font-weight: bold
}

.highlight .ni {
    color: #800080
}

.highlight .ne {
    color: #990000;
    font-weight: bold
}

.highlight .nf {
    color: #990000;
    font-weight: bold
}

.highlight .nl {
    color: #990000;
    font-weight: bold
}

.highlight .nn {
    color: #555555
}

.highlight .nt {
    color: #000080
}

.highlight .vc {
    color: #008080
}

.highlight .vg {
    color: #008080
}

.highlight .vi {
    color: #008080
}

.highlight .nv {
    color: #008080
}

.highlight .ow {
    color: #000000;
    font-weight: bold
}

.highlight .o {
    color: #000000;
    font-weight: bold
}

.highlight .w {
    color: #bbbbbb
}

.highlight {
    background-color: #f8f8f8
}

<!-- Begin Jekyll SEO tag v2.8.0 -->
<title>or-amento-s-o-bento-</title>
<meta name="generator" content="Jekyll v3.10.0" />
<meta property="og:title" content="or-amento-s-o-bento-" />
<meta property="og:locale" content="en_US" />
<link rel="canonical" href="https://matheustermu.github.io/or-amento-s-o-bento-/" />
<meta property="og:url" content="https://matheustermu.github.io/or-amento-s-o-bento-/" />
<meta property="og:site_name" content="or-amento-s-o-bento-" />
<meta property="og:type" content="website" />
<meta name="twitter:card" content="summary" />
<meta property="twitter:title" content="or-amento-s-o-bento-" />
<script type="application/ld+json">
{"@context":"https://schema.org","@type":"WebSite","headline":"or-amento-s-o-bento-","name":"or-amento-s-o-bento-","url":"https://matheustermu.github.io/or-amento-s-o-bento-/"}</script>
<!-- End Jekyll SEO tag -->

    <link rel="stylesheet" href="/or-amento-s-o-bento-/assets/css/style.css?v=f81e55b259e208fa3e2fbd3b64a8927eb2c7c321">
    <!-- start custom head snippets, customize with your own _includes/head-custom.html file -->

<!-- Setup Google Analytics -->



<!-- You can set your favicon here -->
<!-- link rel="shortcut icon" type="image/x-icon" href="/or-amento-s-o-bento-/favicon.ico" -->

<!-- end custom head snippets -->

  </head>
  <body>
    <div class="container-lg px-3 my-5 markdown-body">
      
      <h1><a href="https://matheustermu.github.io/or-amento-s-o-bento-/">or-amento-s-o-bento-</a></h1>
      

      
<html lang="pt-BR">

<html lang="pt-BR">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Página Protegida</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f0f2f5;
            color: #333;
            text-align: center;
            flex-direction: column;
        }
        .content {
            background-color: #ffffff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            width: 90%;
            display: none; /* Esconde o conteúdo por padrão */
        }
        h1 {
            color: #007bff;
            margin-bottom: 20px;
        }
        p {
            font-size: 1.1em;
            line-height: 1.6;
        }
        .footer {
            margin-top: 30px;
            font-size: 0.85em;
            color: #666;
        }
    </style>
</head>
<body>

   
       
    &lt;/div&gt;

    <script>
        const CORRECT_PASSWORD = "102030";
        let passwordEntered = false;

        // Loop para pedir a senha até que seja correta
        while (!passwordEntered) {
            const userInput = prompt("Por favor, digite a senha para acessar esta página:");

            if (userInput === CORRECT_PASSWORD) {
                passwordEntered = true;
                alert("Senha correta! Bem-vindo.");
                document.getElementById('protectedContent').style.display = 'block'; // Mostra o conteúdo
            } else {
                alert("Senha incorreta. Tente novamente.");
            }
        }
    </script>

</body>
</html>
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Gerador de Orçamento - Posto de Molas São Bento</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&amp;display=swap" rel="stylesheet" />
    <style>
        :root {
            --primary-color: #007bff; /* Azul primário */
            --secondary-color: #28a745; /* Verde para botões de sucesso */
            --danger-color: #dc3545; /* Vermelho para botões de remoção */
            --info-color: #17a2b8; /* Azul-ciano para salvar PDF */
            --bg-color: #f8f9fa; /* Fundo claro */
            --card-bg: #ffffff; /* Fundo dos cards */
            --text-color: #343a40; /* Cor de texto principal */
            --border-color: #e9ecef; /* Cor da borda */
            --shadow-light: rgba(0, 0, 0, 0.1);
            --shadow-medium: rgba(0, 0, 0, 0.15);
        }

        body {
            font-family: 'Roboto', Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 0;
            margin: 0;
            background-color: var(--bg-color);
            min-height: 100vh;
            width: 100vw;
            overflow-x: hidden;
            color: var(--text-color);
        }

        h1 {
            color: var(--primary-color);
            margin-top: 30px;
            margin-bottom: 25px;
            font-weight: 700;
            text-shadow: 1px 1px 2px var(--shadow-light);
        }

        .container {
            display: flex;
            gap: 25px;
            width: 90%; /* Um pouco mais de margem nas laterais */
            max-width: 1500px; /* Aumenta a largura máxima */
            margin-bottom: 30px;
            flex-grow: 1;
        }

        .form-section, .canvas-preview {
            flex: 1;
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 12px var(--shadow-medium);
            transition: transform 0.3s ease-in-out;
        }

        .form-section:hover, .canvas-preview:hover {
            transform: translateY(-5px);
        }

        .canvas-container {
            border: 1px solid var(--border-color);
            background-color: #fcf9e7; /* Cor semelhante ao papel */
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: inset 0 0 5px rgba(0,0,0,0.05);
            margin-bottom: 20px; /* Espaçamento entre as páginas na visualização */
        }

        canvas {
            display: block; /* Remove espaçamento extra abaixo do canvas */
            width: 100%; /* Ajusta para preencher o container */
            height: auto;
        }

        h2, h3 {
            color: var(--primary-color);
            margin-bottom: 20px;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 5px;
            font-weight: 700;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--text-color);
            font-size: 0.95em;
        }

        input:where([type="text"], [type="number"], [type="email"], [type="date"])
        select {
            width: calc(100% - 20px); /* Ajusta padding */
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            font-size: 1em;
            color: var(--text-color);
            background-color: var(--bg-color);
            box-shadow: inset 0 1px 3px var(--shadow-light);
            transition: border-color 0.3s ease;
        }

        input:where([type="text"], [type="number"], [type="email"], [type="date"]):focus,
        select:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.25);
        }

        /* --- NOVOS ESTILOS PARA CAMPOS DE ADIÇÃO DE ITENS --- */
        .add-item-fields {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 20px;
            padding: 15px;
            border: 1px dashed var(--primary-color);
            border-radius: 8px;
            background-color: rgba(0, 123, 255, 0.05); /* Cor clara do tema */
        }
        .add-item-fields input {
            flex: 1;
            min-width: 90px;
            margin-bottom: 0;
            background-color: var(--card-bg); /* Input background in item fields */
        }
        .add-item-fields input:where([type="number"]) {
            width: 90px;
            flex: none;
        }
        .add-item-fields input:where([type="text"]).desc-input {
            flex: 4; /* Mais espaço para descrição */
            min-width: 150px;
        }

        /* --- ESTILOS PARA A LISTA DE ITENS --- */
        .item-list-container {
            margin-top: 15px;
            margin-bottom: 15px;
            border-radius: 8px;
            padding: 10px;
            background-color: var(--bg-color);
            border: 1px solid var(--border-color);
        }
        .item-display-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 15px;
            margin-bottom: 8px;
            background-color: var(--card-bg);
            border-radius: 6px;
            box-shadow: 0 2px 5px var(--shadow-light);
        }
        .item-display-row:last-child {
            margin-bottom: 0;
        }
        .item-display-row span {
            font-weight: 600;
            color: var(--text-color);
            flex-grow: 1;
            text-align: left;
            padding-right: 10px;
            font-size: 0.9em;
        }
        .item-display-row .remove-button {
            background-color: var(--danger-color);
            color: white;
            border: none;
            padding: 6px 12px;
            border-radius: 50%; /* Botão redondo */
            cursor: pointer;
            font-weight: bold;
            font-size: 0.9em;
            min-width: 30px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: background-color 0.2s ease, transform 0.2s ease;
        }
        .item-display-row .remove-button:hover {
            background-color: #c82333;
            transform: scale(1.05);
        }

        /* --- BOTÕES GERAIS --- */
        button {
            background-color: var(--secondary-color);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 15px;
            width: 100%;
            font-size: 1.1em;
            font-weight: 700;
            transition: background-color 0.2s ease, transform 0.2s ease;
            box-shadow: 0 2px 4px var(--shadow-medium);
        }
        button:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }

        /* Totais */
        .totals-section {
            margin-top: 20px;
            padding-top: 15px;
            border-top: 2px dashed var(--border-color);
        }
        .totals-section div {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: bold;
            font-size: 1.1em;
            color: var(--text-color);
        }

        /* Grupo de campo de número de orçamento com botão */
        .orcamento-numero-group {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        .orcamento-numero-group input {
            margin-bottom: 0;
            flex-grow: 1;
        }
        .orcamento-numero-group button {
            width: auto;
            padding: 8px 15px;
            margin-left: 10px;
            margin-top: 0;
            background-color: var(--primary-color); /* Azul para o botão de incremento */
            box-shadow: none; /* Remove sombra para o pequeno botão */
        }
        .orcamento-numero-group button:hover {
            background-color: #0056b3;
            transform: none; /* Remove efeito de transform do botão pequeno */
        }

        /* Estilo para o botão de Salvar PDF */
        #savePdfButton {
            background-color: var(--info-color); /* Cor azul-ciano */
        }
        #savePdfButton:hover {
            background-color: #138496;
        }

        /* --- Media Queries para Responsividade --- */
        @media (max-width: 1024px) {
            .container {
                flex-direction: column;
                width: 95%;
            }
            .form-section, .canvas-preview {
                flex: none;
                width: 100%;
            }
            .canvas-preview {
                padding: 15px; /* Reduz padding para canvas em telas menores */
            }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 1.8em;
                margin-top: 20px;
                margin-bottom: 20px;
            }
            .form-section, .canvas-preview {
                padding: 20px;
            }
            input:where([type="text"], [type="number"], [type="email"], [type="date"]), select, button {
                font-size: 0.95em;
                padding: 10px;
            }
            .add-item-fields {
                flex-direction: column; /* Pilha os inputs em telas menores */
                gap: 8px; /* Ajusta o espaçamento */
            }
            .add-item-fields input {
                width: 100%; /* Força a largura total */
                min-width: unset; /* Remove min-width para melhor flexibilidade */
            }
            .add-item-fields input:where([type="number"]) {
                width: 100%; /* Ocupa a largura total */
            }
            .add-item-fields input:where([type="text"]).desc-input {
                width: 100%; /* Ocupa a largura total */
            }
        }

        /* --- Estilos para Impressão (PDF) - Otimizados para múltiplas páginas --- */
        @media print {
            @page {
                size: A4 portrait;
                margin: 0;
            }

            body {
                background-color: white !important;
                margin: 0;
                padding: 0;
                display: block;
                overflow: hidden;
            }
            h1, .form-section, .add-item-fields, button, .item-list-container, .orcamento-numero-group {
                display: none !important; /* Oculta todo o formulário e botões */
            }
            .container {
                display: block;
                width: 100%;
                max-width: none;
                margin: 0;
                padding: 0;
            }
            .canvas-preview {
                box-shadow: none !important;
                padding: 0 !important;
                margin: 0 !important;
                background-color: white !important;
                display: block;
                width: 100%;
                height: auto; /* Deixa a altura ser definida pelo conteúdo */
            }
            .canvas-container {
                border: none !important;
                box-shadow: none !important;
                background-color: white !important;
                margin-bottom: 0 !important; /* Remove margem entre canvases impressos */
                page-break-after: always; /* Garante que cada canvas começa em uma nova página */
                position: relative; /* Necessário para o page-break-after funcionar corretamente em alguns casos */
                height: 100vh; /* Tenta forçar a altura da viewport de impressão */
                overflow: hidden; /* Garante que nada transborde */
            }
            .canvas-container:last-child {
                page-break-after: avoid; /* Não quebra depois da última página */
            }
            canvas {
                border: none !important;
                box-shadow: none !important;
                background-color: #fcf9e7 !important; /* Mantém a cor de fundo do "papel" */
                display: block;
                width: 100vw !important; /* Tenta usar a largura total da viewport de impressão */
                height: 100vh !important; /* Tenta usar a altura total da viewport de impressão */
                object-fit: contain; /* Redimensiona o canvas para caber na página sem cortar */
            }
        }
    </style>
</head>
<body>
    <h1>Gerador de Orçamento</h1>
    <div class="container">
        <div class="form-section">
            <h2>Dados do Orçamento</h2>

            <label for="numeroOrcamento">Nº Orçamento:</label>
            <div class="orcamento-numero-group">
                <input type="text" id="numeroOrcamento" placeholder="Ex: 2894" />
                <button onclick="incrementOrcamento()">+</button>
            </div>

            <label for="dataOrcamento">Data:</label>
            <input type="date" id="dataOrcamento" />

            <h3>Dados do Cliente</h3>
            <label for="nomeCliente">Nome:</label>
            <input type="text" id="nomeCliente" placeholder="Ex: João da Silva ou Empresa XYZ" />

            <label for="cpfCnpjCliente">CPF/CNPJ:</label>
            <input type="text" id="cpfCnpjCliente" placeholder="Ex: 123.456.789-00 ou 12.345.678/0001-90" />

            <label for="enderecoCliente">Endereço:</label>
            <input type="text" id="enderecoCliente" placeholder="Ex: Rua Exemplo, 123 - Centro" />

            <label for="cidadeCliente">Cidade:</label>
            <input type="text" id="cidadeCliente" placeholder="Ex: Curitiba" />

            <label for="ufCliente">UF:</label>
            <input type="text" id="ufCliente" maxlength="2" placeholder="Ex: PR" />

            <label for="emailCliente">E-mail:</label>
            <input type="email" id="emailCliente" placeholder="Ex: cliente@email.com" />

            <label for="telCliente">Telefone:</label>
            <input type="text" id="telCliente" placeholder="Ex: (42) 99999-9999" />

            <h3>Dados do Veículo</h3>
            <label for="tipoVeiculo">Caminhão / Caminhonete:</label>
            <input type="text" id="tipoVeiculo" placeholder="Ex: Scania P360 ou Ford Ranger" />

            <label for="corVeiculo">Cor:</label>
            <input type="text" id="corVeiculo" placeholder="Ex: Branco ou Preto" />

            <label for="placaVeiculo">Placa:</label>
            <input type="text" id="placaVeiculo" placeholder="Ex: XYZ9E87" />

            <label for="cidadeVeiculo">Cidade Veículo:</label>
            <input type="text" id="cidadeVeiculo" placeholder="Ex: São Paulo" />

       <label for="QUEM FEZ "> QUEM FEZ:</label>
            <input type="text" id="QUEM FEZ" placeholder="Ex:QUEM FEZ" />
            E
            <h3>Peças</h3>
            <div class="add-item-fields">
                <input type="number" id="newPecaQuant" value="1" min="0.1" step="0.1" placeholder="Quant. (Ex: 1)" />
                <input type="text" id="newPecaUnid" value="UNID." placeholder="Unid. (Ex: UNID., MT, KG)" />
                <input type="text" id="newPecaProduto" class="desc-input" placeholder="Descrição da Peça (Ex: Mola Parabólica)" />
                <input type="number" id="newPecaPrecoUnit" value="0.00" min="0" step="0.01" placeholder="Preço Unit. (Ex: 150.00)" />
            </div>
            <div id="pecasContainer" class="item-list-container">
            </div>
            <button onclick="addPeca()">Adicionar Peça</button>

            <h3>Serviços</h3>
            <div class="add-item-fields">
                <input type="number" id="newServicoQuant" value="1" min="0.1" step="0.1" placeholder="Quant. (Ex: 1)" />
                <input type="text" id="newServicoProduto" class="desc-input" placeholder="Descrição do Serviço (Ex: Troca de Amortecedores)" />
                <input type="number" id="newServicoPreco" value="0.00" min="0" step="0.01" placeholder="Preço Total (Ex: 300.00)" />
            </div>
            <div id="servicosContainer" class="item-list-container">
            </div>
            <button onclick="addServico()">Adicionar Serviço</button>

            <h3>Desconto</h3>
            <label for="descontoValor">Valor do Desconto:</label>
            <input type="number" id="descontoValor" value="0.00" min="0" step="0.01" placeholder="Ex: 50.00" />

            <button id="savePdfButton" onclick="saveCanvasAsPdf()">Salvar/Imprimir PDF</button>
        </div>

        <div class="canvas-preview" id="canvasPreviewContainer">
            </div>
    </div>

    <script>
        const canvasPreviewContainer = document.getElementById('canvasPreviewContainer');
        const pecasContainer = document.getElementById('pecasContainer');
        const servicosContainer = document.getElementById('servicosContainer');

        // Referências para os campos de entrada de peças
        const newPecaQuantInput = document.getElementById('newPecaQuant');
        const newPecaUnidInput = document.getElementById('newPecaUnid');
        const newPecaProdutoInput = document.getElementById('newPecaProduto');
        const newPecaPrecoUnitInput = document.getElementById('newPecaPrecoUnit');

        // Referências para os campos de entrada de serviços
        const newServicoQuantInput = document.getElementById('newServicoQuant');
        const newServicoProdutoInput = document.getElementById('newServicoProduto');
        const newServicoPrecoInput = document.getElementById('newServicoPreco');

        // Referência para o campo de desconto
        const descontoValorInput = document.getElementById('descontoValor');


        // Arrays para armazenar as peças e serviços
        const initialPecas = [];
        const initialServicos = [];

        // Dimensões do canvas para A4 (aproximadamente 210mm x 297mm a 300dpi)
        const CANVAS_WIDTH = 1000;
        const CANVAS_HEIGHT = 1400; // Altura de uma página A4 em pixels (aprox. 300dpi)

        // Margens internas do conteúdo
        const MARGIN_X = 60; // REDUZIDO
        const MARGIN_TOP_INITIAL = 60; // REDUZIDO
        const MARGIN_BOTTOM_PAGE = 60; // REDUZIDO
        const MAX_CONTENT_HEIGHT_PER_PAGE = CANVAS_HEIGHT - MARGIN_TOP_INITIAL - MARGIN_BOTTOM_PAGE;

        // Altura de texto e espaçamento base
        const BASE_FONT_SIZE = 18; // REDUZIDO
        const BASE_LINE_HEIGHT = 28; // REDUZIDO
        const SMALL_LINE_HEIGHT = BASE_LINE_HEIGHT - 3; // REDUZIDO para itens de lista


        let currentPageCtx = null; // Contexto do canvas da página atual
        let currentPageY = MARGIN_TOP_INITIAL; // Posição Y atual no canvas da página atual

        // Armazena todos os canvases criados
        let canvases = [];

        function formatCurrency(value) {
            return parseFloat(value).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });
        }

        // Função para iniciar uma nova página no canvas
        function startNewPage() {
            const canvasDiv = document.createElement('div');
            canvasDiv.className = 'canvas-container';
            const newCanvas = document.createElement('canvas');
            newCanvas.width = CANVAS_WIDTH;
            newCanvas.height = CANVAS_HEIGHT;
            canvasDiv.appendChild(newCanvas);
            canvasPreviewContainer.appendChild(canvasDiv);

            currentPageCtx = newCanvas.getContext('2d');
            currentPageCtx.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
            currentPageCtx.fillStyle = '#fcf9e7';
            currentPageCtx.fillRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
            currentPageCtx.fillStyle = '#333';
            currentPageCtx.strokeStyle = '#555';
            currentPageCtx.lineWidth = 1;

            canvases.push(newCanvas);
            currentPageY = MARGIN_TOP_INITIAL; // Reinicia Y para o topo da nova página
        }

        // Função para quebrar texto em várias linhas e desenhá-lo
        function drawWrappedText(ctx, text, x, y, maxWidth, lineHeight) {
            let words = text.split(' ');
            let line = '';
            let currentYForLines = y;
            let linesDrawn = 0;

            for (let n = 0; n < words.length; n++) {
                let testLine = line + words[n] + ' ';
                let metrics = ctx.measureText(testLine);
                let testWidth = metrics.width;

                if (testWidth > maxWidth && n > 0) {
                    ctx.fillText(line.trim(), x, currentYForLines);
                    currentYForLines += lineHeight;
                    linesDrawn++;
                    line = words[n] + ' ';
                } else {
                    line = testLine;
                }
            }
            if (line.trim() !== '') {
                ctx.fillText(line.trim(), x, currentYForLines);
                currentYForLines += lineHeight;
                linesDrawn++;
            }
            return linesDrawn * lineHeight; // Retorna a altura total ocupada
        }

        // Função para calcular a altura que um texto ocuparia
        function measureWrappedTextHeight(ctx, text, maxWidth, lineHeight) {
            let words = text.split(' ');
            let line = '';
            let lines = 0;
            if (text.trim() === '') return 0; // Handle empty text

            for (let n = 0; n < words.length; n++) {
                let testLine = line + words[n] + ' ';
                let metrics = ctx.measureText(testLine);
                let testWidth = metrics.width;
                if (testWidth > maxWidth && n > 0) {
                    lines++;
                    line = words[n] + ' ';
                } else {
                    line = testLine;
                }
            }
            lines++; // For the last line
            return lines * lineHeight;
        }

        function renderPecas() {
            pecasContainer.innerHTML = '';
            initialPecas.forEach((item, index) => {
                const total = item.quant * item.precoUnit;
                const row = document.createElement('div');
                row.className = 'item-display-row';
                row.innerHTML = `
                    <span>${item.produto} - ${formatCurrency(total)}</span>
                    <button class="remove-button" onclick="removePeca(${index})">X</button>
                `;
                pecasContainer.appendChild(row);
            });
            drawAllCanvases();
        }

        function addPeca() {
            const quant = parseFloat(newPecaQuantInput.value);
            const unid = newPecaUnidInput.value.trim();
            const produto = newPecaProdutoInput.value.trim();
            const precoUnit = parseFloat(newPecaPrecoUnitInput.value);

            // CORREÇÃO: Preço Unitário deve ser >= 0
            if (isNaN(quant) || quant <= 0 || !unid || !produto || isNaN(precoUnit) || precoUnit < 0) {
                alert("Por favor, preencha todos os campos da peça corretamente (Quantidade > 0, Preço Unitário >= 0).");
                return;
            }

            initialPecas.push({ quant: quant, unid: unid, produto: produto, precoUnit: precoUnit });
            renderPecas();

            newPecaQuantInput.value = "1";
            newPecaUnidInput.value = "UNID.";
            newPecaProdutoInput.value = "";
            newPecaPrecoUnitInput.value = "0.00";
        }

        function removePeca(index) {
            initialPecas.splice(index, 1);
            renderPecas();
        }

        function renderServicos() {
            servicosContainer.innerHTML = '';
            initialServicos.forEach((item, index) => {
                const total = item.quant * item.preco;
                const row = document.createElement('div');
                row.className = 'item-display-row';
                row.innerHTML = `
                    <span>${item.produto} - ${formatCurrency(total)}</span>
                    <button class="remove-button" onclick="removeServico(${index})">X</button>
                `;
                servicosContainer.appendChild(row);
            });
            drawAllCanvases();
        }

        function addServico() {
            const quant = parseFloat(newServicoQuantInput.value);
            const produto = newServicoProdutoInput.value.trim();
            const preco = parseFloat(newServicoPrecoInput.value);

            // CORREÇÃO: Preço Total deve ser >= 0
            if (isNaN(quant) || quant <= 0 || !produto || isNaN(preco) || preco < 0) {
                alert("Por favor, preencha todos os campos do serviço corretamente (Quantidade > 0, Preço >= 0).");
                return;
            }

            initialServicos.push({ quant: quant, produto: produto, preco: preco });
            renderServicos();

            newServicoQuantInput.value = "1";
            newServicoProdutoInput.value = "";
            newServicoPrecoInput.value = "0.00";
        }

        function removeServico(index) {
            initialServicos.splice(index, 1);
            renderServicos();
        }

        function incrementOrcamento() {
            const numeroOrcamentoInput = document.getElementById('numeroOrcamento');
            let currentNumber = parseInt(numeroOrcamentoInput.value, 10);
            if (!isNaN(currentNumber)) {
                numeroOrcamentoInput.value = currentNumber + 1;
            } else {
                numeroOrcamentoInput.value = "1";
            }
            drawAllCanvases();
        }

        function saveCanvasAsPdf() {
            drawAllCanvases();
            window.print();
        }

        document.querySelectorAll('#numeroOrcamento, #dataOrcamento, #nomeCliente, #cpfCnpjCliente, #enderecoCliente, #cidadeCliente, #ufCliente, #emailCliente, #telCliente, #tipoVeiculo, #corVeiculo, #placaVeiculo, #cidadeVeiculo, #descontoValor # QUEM FEZ').forEach(input => {
            input.addEventListener('input', drawAllCanvases);
        });

        document.addEventListener('DOMContentLoaded', () => {
            const today = new Date();
            const day = String(today.getDate()).padStart(2, '0');
            const month = String(today.getMonth() + 1).padStart(2, '0');
            const year = today.getFullYear();
            document.getElementById('dataOrcamento').value = `${year}-${month}-${day}`;

            renderPecas();
            renderServicos();
            drawAllCanvases();
        });

        // Função principal para desenhar todas as páginas
        function drawAllCanvases() {
            canvasPreviewContainer.innerHTML = ''; // Limpa canvases anteriores
            canvases = []; // Limpa a lista de canvases

            startNewPage(); // Inicia a primeira página

            // --- Cabeçalho da Empresa ---
            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 10}px Arial`; // REDUZIDO
            currentPageCtx.fillText('POSTO DE MOLAS SÃO BENTO', MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('ORÇAMENTIIIIIO', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 6}px Arial`; // REDUZIDO
            currentPageCtx.fillText('PEÇAS E SERVIÇOS', MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'right';
            const numeroOrcamento = document.getElementById('numeroOrcamento').value.trim();
            currentPageCtx.fillText(`Nº ${numeroOrcamento === '' ? 'Não informado' : numeroOrcamento}`, CANVAS_WIDTH - MARGIN_X, currentPageY); // CORREÇÃO: "Não informado"
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 20; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO
            currentPageCtx.fillText('Suspensão de Caminhão e Caminhonete', MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText('Alinhamento e Balanceamento - Suspensão a Ar', MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText('42 99934-3158 | 42 99946-5858', MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('CNPJ 50.076.502/0001-74', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText('postodemolassaobento@gmail.com - Av. Souza Naves, 4250 - CEP 84064-000 - Ponta Grossa / PR', MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 20; // REDUZIDO

            // --- Dados do Cliente e Veículo ---
            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 2}px Arial`; // REDUZIDO
            let clientVehicleSectionHeight = (BASE_LINE_HEIGHT + 10) + (SMALL_LINE_HEIGHT * 5) + (BASE_LINE_HEIGHT + 20); // Título + 5 linhas de dados + espaçamento final

            if (currentPageY + clientVehicleSectionHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            currentPageCtx.fillText('DADOS DO CLIENTE E VEÍCULO', MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO
            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO

            const nomeCliente = document.getElementById('nomeCliente').value.trim();
            const cpfCnpjCliente = document.getElementById('cpfCnpjCliente').value.trim();
            const enderecoCliente = document.getElementById('enderecoCliente').value.trim();
            const cidadeCliente = document.getElementById('cidadeCliente').value.trim();
            const ufCliente = document.getElementById('ufCliente').value.trim();
            const emailCliente = document.getElementById('emailCliente').value.trim();
            const telCliente = document.getElementById('telCliente').value.trim();
            const tipoVeiculo = document.getElementById('tipoVeiculo').value.trim();
            const corVeiculo = document.getElementById('corVeiculo').value.trim();
            const placaVeiculo = document.getElementById('placaVeiculo').value.trim();
            const cidadeVeiculo = document.getElementById('cidadeVeiculo').value.trim();
            const QUEM FEZ = document.getElementById('QUEM FEZ').value.trim();
            
            // CORREÇÃO: "Não informado" para campos vazios
            currentPageCtx.fillText(`Nome: ${nomeCliente === '' ? 'Não informado' : nomeCliente}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`CPF/CNPJ: ${cpfCnpjCliente === '' ? 'Não informado' : cpfCnpjCliente}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`Endereço: ${enderecoCliente === '' ? 'Não informado' : enderecoCliente}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Cidade/UF: ${cidadeCliente === '' ? 'Não informado' : cidadeCliente}/${ufCliente === '' ? 'Não informado' : ufCliente}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`E-mail: ${emailCliente === '' ? 'Não informado' : emailCliente}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Telefone: ${telCliente === '' ? 'Não informado' : telCliente}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`Veículo: ${tipoVeiculo === '' ? 'Não informado' : tipoVeiculo}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Cor: ${corVeiculo === '' ? 'Não informado' : corVeiculo}`, MARGIN_X + 400, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT; // REDUZIDO
            currentPageCtx.fillText(`Placa: ${placaVeiculo === '' ? 'Não informado' : placaVeiculo}`, MARGIN_X, currentPageY);
            currentPageCtx.fillText(`Cidade Veículo: ${cidadeVeiculo === '' ? 'Não informado' : cidadeVeiculo}`, MARGIN_X + 400, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 20; // REDUZIDO
            currentPageCtx.fillText(`QUEM FEZ ${QUEM FEZ === '' ? 'Não informado' : QUEM FEZ}`, MARGIN_X, currentPageY);
            // --- Seção de Peças ---
            let pecasSectionTitleHeight = BASE_LINE_HEIGHT + 6 + 10;
            let pecasTableHeaderHeight = (BASE_FONT_SIZE + 2 + 10) + (SMALL_LINE_HEIGHT + 5);

            if (currentPageY + pecasSectionTitleHeight + pecasTableHeaderHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'center';
            currentPageCtx.fillText('PEÇAS', CANVAS_WIDTH / 2, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
            currentPageCtx.fillText('UNID.', MARGIN_X + 100, currentPageY); // Ajustado X
            currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY); // Ajustado X
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY); // Ajustado X
            currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += 8; // REDUZIDO
            currentPageCtx.beginPath();
            currentPageCtx.moveTo(MARGIN_X, currentPageY);
            currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.stroke();
            currentPageY += SMALL_LINE_HEIGHT + 5; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO
            initialPecas.forEach(item => {
                const itemTotal = item.quant * item.precoUnit;

                const requiredHeight = measureWrappedTextHeight(currentPageCtx, item.produto, 350, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH

                if (currentPageY + requiredHeight + (SMALL_LINE_HEIGHT * 1) > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                    startNewPage();
                    // Redesenha cabeçalho de peças na nova página
                    currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`;
                    currentPageCtx.textAlign = 'center';
                    currentPageCtx.fillText('PEÇAS (continuação)', CANVAS_WIDTH / 2, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += BASE_LINE_HEIGHT + 10;

                    currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`;
                    currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
                    currentPageCtx.fillText('UNID.', MARGIN_X + 100, currentPageY);
                    currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY);
                    currentPageCtx.textAlign = 'right';
                    currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                    currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += 8;
                    currentPageCtx.beginPath();
                    currentPageCtx.moveTo(MARGIN_X, currentPageY);
                    currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.stroke();
                    currentPageY += SMALL_LINE_HEIGHT + 5;
                    currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`;
                }

                currentPageCtx.fillText(item.quant.toFixed(2), MARGIN_X, currentPageY);
                currentPageCtx.fillText(item.unid, MARGIN_X + 100, currentPageY);
                const actualHeightUsed = drawWrappedText(currentPageCtx, item.produto, MARGIN_X + 180, currentPageY, 350, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH
                currentPageCtx.textAlign = 'right';
                currentPageCtx.fillText(formatCurrency(item.precoUnit), CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                currentPageCtx.fillText(formatCurrency(itemTotal), CANVAS_WIDTH - MARGIN_X, currentPageY);
                currentPageCtx.textAlign = 'left';
                currentPageY += actualHeightUsed;
            });
            currentPageY += 30; // REDUZIDO

            // --- Seção de Serviços ---
            let servicosSectionTitleHeight = BASE_LINE_HEIGHT + 6 + 10;
            let servicosTableHeaderHeight = (BASE_FONT_SIZE + 2 + 10) + (SMALL_LINE_HEIGHT + 5);

            if (currentPageY + servicosSectionTitleHeight + servicosTableHeaderHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'center';
            currentPageCtx.fillText('SERVIÇOS', CANVAS_WIDTH / 2, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += BASE_LINE_HEIGHT + 10; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
            currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY); // Ajustado X
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY); // Ajustado X
            currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.textAlign = 'left';
            currentPageY += 8; // REDUZIDO
            currentPageCtx.beginPath();
            currentPageCtx.moveTo(MARGIN_X, currentPageY);
            currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageCtx.stroke();
            currentPageY += SMALL_LINE_HEIGHT + 5; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`; // REDUZIDO
            initialServicos.forEach(item => {
                const itemTotal = item.quant * item.preco;
                const requiredHeight = measureWrappedTextHeight(currentPageCtx, item.produto, 450, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH

                if (currentPageY + requiredHeight + (SMALL_LINE_HEIGHT * 1) > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                    startNewPage();
                    // Redesenha cabeçalho de serviços na nova página
                    currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`;
                    currentPageCtx.textAlign = 'center';
                    currentPageCtx.fillText('SERVIÇOS (continuação)', CANVAS_WIDTH / 2, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += BASE_LINE_HEIGHT + 10;

                    currentPageCtx.font = `bold ${BASE_FONT_SIZE}px Arial`;
                    currentPageCtx.fillText('QUANT.', MARGIN_X, currentPageY);
                    currentPageCtx.fillText('DESCRIÇÃO', MARGIN_X + 180, currentPageY);
                    currentPageCtx.textAlign = 'right';
                    currentPageCtx.fillText('VALOR UNIT.', CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                    currentPageCtx.fillText('TOTAL', CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.textAlign = 'left';
                    currentPageY += 8;
                    currentPageCtx.beginPath();
                    currentPageCtx.moveTo(MARGIN_X, currentPageY);
                    currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X, currentPageY);
                    currentPageCtx.stroke();
                    currentPageY += SMALL_LINE_HEIGHT + 5;
                    currentPageCtx.font = `${BASE_FONT_SIZE - 2}px Arial`;
                }

                currentPageCtx.fillText(item.quant.toFixed(2), MARGIN_X, currentPageY);
                const actualHeightUsed = drawWrappedText(currentPageCtx, item.produto, MARGIN_X + 180, currentPageY, 450, SMALL_LINE_HEIGHT); // REDUZIDO MAXWIDTH
                currentPageCtx.textAlign = 'right';
                currentPageCtx.fillText(formatCurrency(item.preco), CANVAS_WIDTH - MARGIN_X - 220, currentPageY);
                currentPageCtx.fillText(formatCurrency(itemTotal), CANVAS_WIDTH - MARGIN_X, currentPageY);
                currentPageCtx.textAlign = 'left';
                currentPageY += actualHeightUsed;
            });
            currentPageY += 40; // REDUZIDO

            // --- Totais e Rodapé ---
            let totalsFooterHeight = (SMALL_LINE_HEIGHT + 8) * 3 + (BASE_FONT_SIZE + 8 + 15) + (SMALL_LINE_HEIGHT + 8) + 80 + 25 + BASE_FONT_SIZE; // Ajustado os cálculos de altura para os novos tamanhos de fonte e linha

            if (currentPageY + totalsFooterHeight > (CANVAS_HEIGHT - MARGIN_BOTTOM_PAGE)) {
                startNewPage();
            }

            const totalPecas = initialPecas.reduce((sum, item) => sum + (item.quant * item.precoUnit), 0);
            const totalServicos = initialServicos.reduce((sum, item) => sum + (item.quant * item.preco), 0);
            const desconto = parseFloat(document.getElementById('descontoValor').value) || 0;
            const totalGeral = totalPecas + totalServicos - desconto;

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 4}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'right';
            currentPageCtx.fillText('TOTAL DE PEÇAS:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(totalPecas), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT + 8; // REDUZIDO

            currentPageCtx.fillText('TOTAL DE SERVIÇOS:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(totalServicos), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT + 8; // REDUZIDO

            currentPageCtx.fillText('DESCONTO:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(desconto), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += SMALL_LINE_HEIGHT + 8; // REDUZIDO

            currentPageCtx.font = `bold ${BASE_FONT_SIZE + 8}px Arial`; // REDUZIDO
            currentPageCtx.fillText('TOTAL GERAL:', CANVAS_WIDTH - MARGIN_X - 300, currentPageY);
            currentPageCtx.fillText(formatCurrency(totalGeral), CANVAS_WIDTH - MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 30; // REDUZIDO

            currentPageCtx.font = `${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'left';
            const dataOrcamento = document.getElementById('dataOrcamento').value;
            const dataFormatada = dataOrcamento ? new Date(dataOrcamento).toLocaleDateString('pt-BR', { day: 'numeric', month: 'long', year: 'numeric' }) : 'Não informado'; // CORREÇÃO: "Não informado"
            currentPageCtx.fillText(`Ponta Grossa, ${dataFormatada}`, MARGIN_X, currentPageY);
            currentPageY += BASE_LINE_HEIGHT + 60; // REDUZIDO

            currentPageCtx.beginPath();
            currentPageCtx.moveTo(MARGIN_X + 150, currentPageY); // Ajustado X
            currentPageCtx.lineTo(CANVAS_WIDTH - MARGIN_X - 150, currentPageY); // Ajustado X
            currentPageCtx.stroke();
            currentPageY += 20; // REDUZIDO
            currentPageCtx.font = `${BASE_FONT_SIZE}px Arial`; // REDUZIDO
            currentPageCtx.textAlign = 'center';
            currentPageCtx.fillText('Assinatura do Responsável', CANVAS_WIDTH / 2, currentPageY);
            currentPageCtx.textAlign = 'left';
        }
    </script>
</body>
</html>


      
    </div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/anchor-js/4.1.0/anchor.min.js" integrity="sha256-lZaRhKri35AyJSypXXs4o6OPFTbTmUoltBbDCbdzegg=" crossorigin="anonymous"></script>
    <script>anchors.add();</script>
  </body>
</html>
