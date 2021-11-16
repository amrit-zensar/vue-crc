<template>
  <div class="page">
    <div class="header">
      <a style="text-decoration: none; color: #fff; " href="#">
        <h4> <svg role="img" style="fill: rgb(255, 255, 255); transition: fill .35s; width: 14px; height: 14px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25 22">
            <title>button</title>
            <desc>Arrow left</desc>
            <path d="M7.2 13.2l6.5 6.7-2.5 2.5L0 11.2 11.1 0l2.6 2.6-6.5 6.6h17.9v4z"></path>
          </svg> SERVICES</h4>
      </a>
      <br>
      <h1 v-html="wcrc" style="font-size:65px;"></h1>
      <br>
      <p>{{ wcrcMsg}}</p>
    </div>

    <div class="middle">
      <h1 v-html="midHead" style="font-size:45px;"></h1>
      <p v-html="midMsg"></p>

      <div class="inputMsg">
        <label v-html="visitors"></label>
        <br>
        <input type="text" v-model="message">
      </div>

      <div class="inputMsg">
        <label v-html="conversion"></label>
        <br>
        <input type="text" v-model="message">
      </div>

      <div class="inputMsg">
        <label v-html="transaction"></label>
        <br>
        <input type="text" v-model="message">
      </div>

      <div class="inputMsg">
        <label v-html="rateConversion"></label>
        <br>
        <br>
        <input type="range" v-model="message">
      </div>
      <br>
      <button @click="handleClick" type="submit">CALCULATE <svg role="img"
          style="fill: rgb(255, 255, 255); transition: fill .35s; width: 12px; height: 12px;"
          xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25 22">
          <title>Submit</title>
          <desc>Submit form to Foolproof</desc>
          <path d="M17.9 9.3l-6.5-6.8L13.9 0l11.2 11.2L14 22.4l-2.6-2.5 6.5-6.7H0v-4z"></path>
        </svg></button>
    </div>

    <!-- Conversion Table Start -->

    <div>
      <form data-vv-scope="form-scope-new-business" enctype="multipart/form-data" autocomplete="off"
        novalidate="novalidate" class="form-base is-theme-beta">
        <div class="form-base__loader">
          <div class="form-loader form-loader--theme-beta">
            <div class="form-loader__icon"></div>
          </div>
        </div>
        <div class="form-base__content">

          <div class="form-base__elements">
            <fieldset class="form-fieldset">

              <div class="form-fieldset__content">
                <div class="form-input form-input--size-default is-theme-beta">
                  <label for="id-numberofvisitors" class="form-input__label">
                    What is your average number of
                    visitors?
                    <span class="form-input__required">*</span>
                    <span class="form-input__required label--desc">(per
                      month or per year)</span>
                  </label>
                  <input id="id-numberofvisitors" name="numberofvisitors" type="text" value="0" autocomplete="off"
                    v-model="" class="form-input__input form-input__input--none pristine untouched" aria-required="true"
                    aria-invalid="false">
                  <div class="form-input__msg form-input__msg--">
                    <div class="form-message form-message--theme-delta">
                      <p class="form-message__text">
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </fieldset>
            <fieldset class="form-fieldset">

              <div class="form-fieldset__content">
                <div class="form-input form-input--size-default is-theme-beta">
                  <label for="id-avgwebsite" class="form-input__label">
                    What is your average website
                    conversion rate?
                    <span class="form-input__required">*</span>
                  </label>
                  <input id="id-avgwebsite" name="avgwebsite" type="text" value="0" autocomplete="off" v-model=""
                    class="form-input__input form-input__input--none pristine untouched" aria-required="true"
                    aria-invalid="false">
                  <span class="form-input__required label--unit">%</span>
                  <div class="form-input__msg form-input__msg--">
                    <div class="form-message form-message--theme-delta">
                      <p class="form-message__text">
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </fieldset>
            <fieldset class="form-fieldset">

              <div class="form-fieldset__content">
                <div class="form-input form-input--size-default is-theme-beta">
                  <label for="id-avgtransaction" class="form-input__label">
                    What is your average transaction
                    value?
                    <span class="form-input__required">*</span>
                    <span class="form-input__required label--desc">(average
                      checkout, basket, or sales
                      value)</span>
                  </label>
                  <span class="form-input__required label--unit pos-aln--left">£</span>
                  <input id="id-avgtransaction" name="avgtransaction" type="text" value="0" autocomplete="off"
                    v-model="" class="form-input__input form-input__input--none pristine untouched pad-lft--15"
                    aria-required="true" aria-invalid="false">
                  <div class="form-input__msg form-input__msg--">
                    <div class="form-message form-message--theme-delta">
                      <p class="form-message__text">
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </fieldset>
            <fieldset class="form-fieldset">
              <div class="form-fieldset__content">
                <div class="form-input form-input--size-default is-theme-beta">
                  <label for="id-convrate" class="form-input__label">
                    What increase in conversion rate
                    do you want?
                    <span class="form-input__required">*</span>
                  </label>
                  <input id="id-convrate" name="convrate" type="range" min="0" max="250" value="0" v-model=""
                    class="customslider" aria-required="true" aria-invalid="false">
                  <span id="id-convratevalue" class="form-input__required label--desc">0
                    %</span>
                  <div class="form-input__msg form-input__msg--">
                    <div class="form-message form-message--theme-delta">
                      <p class="form-message__text">
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </fieldset>
            <div class="form-base__button">
              <div>
                <button type="button" onclick="webConversionResults()"
                  class="button-action button-action--theme-beta button-action--size-default button-action--states-default button-action--disabled-false button-action--icon-nudge">
                  <span class="button-action__title">Calculate</span>
                  <span class="button-action__right">
                    <span aria-label="Submit" class="icon">
                      <svg role="img"
                        style="fill: rgb(255, 255, 255); transition: fill .35s; width: 12px; height: 12px;"
                        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25 22">
                        <title>Submit</title>
                        <desc>Submit form to
                          Foolproof</desc>
                        <path d="M17.9 9.3l-6.5-6.8L13.9 0l11.2 11.2L14 22.4l-2.6-2.5 6.5-6.7H0v-4z">
                        </path>
                      </svg>
                    </span>
                  </span>
                </button>
              </div>
            </div>
          </div>
        </div>
      </form>
    </div>


    <div id="web_conversion_results">
      <div class="form-base__content">
        <div class="html-block html-block--theme-beta is-theme-beta">
          <div>
            <p>Incremental profit and revenue gains from new
              conversion rate:</p>
          </div>
        </div>
      </div>
      <div class="table-responsive">
        <table id="web_conversion_table" class="table table-bordered">
          <thead>
            <tr>
              <th></th>
              <th>Old Website</th>
              <th>Optimized Website</th>
              <th
                style="background-color: rgb(236, 255, 236); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0); border-top-width: 1px; border-top-style: solid; border-top-color: rgb(0, 153, 0);">
                Incremental Benefit</th>
            </tr>
          </thead>
          <tbody>
            <tr class="output-row" style="background-color: rgb(249, 249, 251);">
              <td>Your visitors</td>
              <td>0</td>
              <td>0</td>
              <td
                style="background-color: rgb(230, 249, 232); color: rgb(0, 153, 0); font-weight: bold; border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0);">
              </td>
            </tr>
            <tr class="output-row">
              <td>Website Conversions</td>
              <td>0%</td>
              <td>0%</td>
              <td
                style="background-color: rgb(236, 255, 236); color: rgb(0, 153, 0); font-weight: bold; border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0);">
                0%</td>
            </tr>
            <tr class="output-row" style="background-color: rgb(249, 249, 251);">
              <td>Number of sales</td>
              <td>0</td>
              <td>0</td>
              <td
                style="background-color: rgb(230, 249, 232); color: rgb(0, 153, 0); font-weight: bold; border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0);">
                0</td>
            </tr>
            <tr class="output-row">
              <td>Revenue</td>
              <td>£ 0</td>
              <td>£ 0</td>
              <td
                style="background-color: rgb(236, 255, 236); color: rgb(0, 153, 0); font-weight: bold; border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0);">
                £ 0</td>
            </tr>
            <tr class="output-row" style="background-color: rgb(249, 249, 251);">
              <td>Revenue per visitor</td>
              <td>£ 0</td>
              <td>£ 0</td>
              <td
                style="background-color: rgb(230, 249, 232); color: rgb(0, 153, 0); font-weight: bold; border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0);">
                £ 0</td>
            </tr>
            <tr class="output-row">
              <td>Visitors per transaction</td>
              <td>0</td>
              <td>0</td>
              <td id="bottom_rounder_corner"
                style="background-color: rgb(236, 255, 236); color: rgb(0, 153, 0); font-weight: bold; border-left-width: 1px; border-left-style: solid; border-left-color: rgb(0, 153, 0); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(0, 153, 0); border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(0, 153, 0);">
                0</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="clear-both">
        <div id="result-details">
          <span id="score_title"></span> <br>
          <span id="score_desc"></span>
        </div>
      </div>
    </div>


    <!-- Conversion Table End -->

    <div class="footer">
      <a href="/Home"><span>Home</span></a>
      <a href="/About"><span>About</span></a>
      <a href="/Services"><span>Services</span></a>
      <a href="/Journal"><span>Journal</span></a>
      <a href="/People"><span>People</span></a>
      <a href="/Contact"><span>Contact</span></a>

      <div class="foolproof">
        <a href="#"><svg role="img" style="fill: rgb(255, 255, 255); transition: fill .35s; width: 238px; height: 66px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 771 214">
            <g fill-rule="nonzero">
              <path
                d="M268.21 35.1v14.58h-38.66v24.6h30.98v14.06h-30.98V127H211.2V35.1h57.01zM323.09 61.55c5.34 2.82 9.54 6.89 12.6 12.23 3.06 5.34 4.6 11.61 4.6 18.81 0 7.2-1.53 13.45-4.6 18.75-3.06 5.3-7.26 9.38-12.6 12.23-5.34 2.86-11.36 4.28-18.07 4.28-6.71 0-12.73-1.43-18.07-4.28-5.34-2.86-9.54-6.93-12.61-12.23-3.06-5.3-4.59-11.55-4.59-18.75 0-7.2 1.53-13.47 4.59-18.81 3.06-5.34 7.27-9.42 12.61-12.23 5.34-2.81 11.36-4.22 18.07-4.22 6.71 0 12.73 1.41 18.07 4.22zM292.6 77.63c-3.4 3.44-5.09 8.42-5.09 14.96 0 6.54 1.69 11.53 5.09 14.96 3.4 3.43 7.53 5.15 12.42 5.15 4.88 0 9.02-1.72 12.42-5.15 3.4-3.43 5.09-8.42 5.09-14.96 0-6.54-1.7-11.53-5.09-14.96-3.4-3.43-7.53-5.15-12.42-5.15-4.88 0-9.02 1.72-12.42 5.15zM400.76 61.55c5.34 2.82 9.54 6.89 12.6 12.23 3.06 5.34 4.6 11.61 4.6 18.81 0 7.2-1.53 13.45-4.6 18.75-3.06 5.3-7.26 9.38-12.6 12.23-5.34 2.86-11.36 4.28-18.07 4.28-6.71 0-12.73-1.43-18.07-4.28-5.34-2.86-9.54-6.93-12.61-12.23-3.06-5.3-4.59-11.55-4.59-18.75 0-7.2 1.53-13.47 4.59-18.81 3.06-5.34 7.27-9.42 12.61-12.23 5.34-2.81 11.36-4.22 18.07-4.22 6.71 0 12.73 1.41 18.07 4.22zm-30.49 16.08c-3.4 3.44-5.09 8.42-5.09 14.96 0 6.54 1.69 11.53 5.09 14.96 3.4 3.43 7.53 5.15 12.42 5.15 4.88 0 9.02-1.72 12.42-5.15 3.4-3.43 5.09-8.42 5.09-14.96 0-6.54-1.7-11.53-5.09-14.96-3.4-3.43-7.53-5.15-12.42-5.15-4.88 0-9.02 1.72-12.42 5.15zM443.6 35.1V127h-17.51V35.1zM509.47 61.55c4.64 2.82 8.26 6.89 10.87 12.23 2.61 5.34 3.91 11.61 3.91 18.81 0 7.2-1.3 13.47-3.91 18.81-2.61 5.34-6.23 9.42-10.87 12.23-4.64 2.82-9.85 4.22-15.64 4.22-5.8 0-10.74-1.38-14.84-4.16-4.1-2.77-7.02-6.48-8.75-11.11v47.19h-17.51V58.19h17.51v14.28c1.74-4.64 4.65-8.32 8.75-11.05 4.1-2.73 9.05-4.1 14.84-4.1 5.79.01 11 1.42 15.64 4.23zm-34.21 16.46c-3.44 3.6-5.15 8.47-5.15 14.59 0 6.04 1.72 10.87 5.15 14.47 3.43 3.6 7.8 5.4 13.1 5.4 5.46 0 9.85-1.76 13.16-5.28 3.31-3.52 4.97-8.38 4.97-14.59 0-6.21-1.66-11.09-4.97-14.65-3.31-3.56-7.7-5.34-13.16-5.34-5.3-.01-9.67 1.79-13.1 5.4zM560.06 60.99c4.22-2.53 8.94-3.79 14.16-3.79v18.75h-5.09c-12.83 0-19.25 5.96-19.25 17.88v33.16h-17.51v-68.8h17.51v13.16c2.57-4.38 5.96-7.83 10.18-10.36zM631.96 61.55c5.34 2.82 9.54 6.89 12.6 12.23 3.06 5.34 4.6 11.61 4.6 18.81 0 7.2-1.53 13.45-4.6 18.75-3.06 5.3-7.26 9.38-12.6 12.23-5.34 2.86-11.36 4.28-18.07 4.28-6.71 0-12.73-1.43-18.07-4.28-5.34-2.86-9.54-6.93-12.61-12.23-3.06-5.3-4.59-11.55-4.59-18.75 0-7.2 1.53-13.47 4.59-18.81 3.06-5.34 7.27-9.42 12.61-12.23 5.34-2.81 11.36-4.22 18.07-4.22 6.71 0 12.73 1.41 18.07 4.22zm-30.49 16.08c-3.4 3.44-5.09 8.42-5.09 14.96 0 6.54 1.69 11.53 5.09 14.96 3.4 3.43 7.53 5.15 12.42 5.15 4.88 0 9.02-1.72 12.42-5.15 3.4-3.43 5.09-8.42 5.09-14.96 0-6.54-1.7-11.53-5.09-14.96-3.4-3.43-7.53-5.15-12.42-5.15-4.88 0-9.02 1.72-12.42 5.15zM709.63 61.55c5.34 2.82 9.54 6.89 12.6 12.23 3.06 5.34 4.6 11.61 4.6 18.81 0 7.2-1.53 13.45-4.6 18.75-3.06 5.3-7.26 9.38-12.6 12.23-5.34 2.86-11.36 4.28-18.07 4.28-6.71 0-12.73-1.43-18.07-4.28-5.34-2.86-9.54-6.93-12.61-12.23-3.06-5.3-4.59-11.55-4.59-18.75 0-7.2 1.53-13.47 4.59-18.81 3.06-5.34 7.27-9.42 12.61-12.23 5.34-2.81 11.36-4.22 18.07-4.22 6.71 0 12.73 1.41 18.07 4.22zm-30.49 16.08c-3.4 3.44-5.09 8.42-5.09 14.96 0 6.54 1.69 11.53 5.09 14.96 3.4 3.43 7.53 5.15 12.42 5.15 4.88 0 9.02-1.72 12.42-5.15 3.4-3.43 5.09-8.42 5.09-14.96 0-6.54-1.7-11.53-5.09-14.96-3.4-3.43-7.53-5.15-12.42-5.15s-9.02 1.72-12.42 5.15zM759.99 48.51c-2.07 1.82-3.11 5.01-3.11 9.56v.12h13.91v14.78h-13.91v54.02h-17.51V72.97h-8.82V58.19h8.82v-1.61c0-8.2 2.34-14.51 7.01-18.94 4.68-4.43 11.61-6.65 20.8-6.65 1.57 0 2.78.04 3.6.12v15.15c-5.12-.31-8.72.43-10.79 2.25z">
              </path>
              <g>
                <path
                  d="M230.75 205.77h-13.59l-2.58 7.14h-4.29l11.44-30.33h4.52l11.4 30.33h-4.29l-2.61-7.14zm-1.14-3.11l-5.65-15.6-5.66 15.6h11.31zM275.29 209.63h15.56v3.29h-20.03v-3.15l15.3-24.46h-14.9v-3.29h19.37v3.15zM308.82 185.26v10.56h11.75v3.07h-11.75v10.78h13.06v3.24h-17.05v-30.9h17.05v3.24h-13.06zM360.02 212.92h-3.99l-16.04-24.41v24.41H336v-30.9h3.99l16.04 24.46v-24.46h3.99zM393.9 208.97c-.7 1.26-1.77 2.28-3.2 3.07-1.43.79-3.2 1.18-5.3 1.18-2.04 0-3.86-.37-5.45-1.12-1.6-.74-2.87-1.77-3.82-3.07-.95-1.3-1.5-2.78-1.64-4.45h4.25c.09.88.39 1.73.9 2.56.51.83 1.24 1.52 2.19 2.06s2.1.81 3.44.81c1.75 0 3.1-.47 4.03-1.4.93-.94 1.4-2.13 1.4-3.6 0-1.26-.33-2.28-.98-3.07a6.985 6.985 0 00-2.43-1.86c-.97-.45-2.28-.94-3.95-1.47-1.96-.64-3.53-1.25-4.72-1.82-1.18-.57-2.19-1.42-3.02-2.56-.83-1.14-1.25-2.64-1.25-4.52 0-1.61.39-3.02 1.16-4.25.77-1.23 1.88-2.18 3.33-2.85 1.45-.67 3.15-1.01 5.11-1.01 3.04 0 5.45.74 7.23 2.21 1.78 1.47 2.82 3.35 3.11 5.63H390c-.24-1.23-.86-2.31-1.89-3.24-1.02-.93-2.41-1.4-4.16-1.4-1.61 0-2.9.42-3.86 1.25-.96.83-1.44 2.01-1.44 3.53 0 1.2.31 2.17.94 2.91a6.61 6.61 0 002.34 1.75c.93.42 2.22.9 3.86 1.43 1.99.64 3.59 1.26 4.8 1.84 1.21.58 2.24 1.47 3.09 2.65.85 1.18 1.27 2.75 1.27 4.71 0 1.49-.35 2.85-1.05 4.1zM427.38 205.77h-13.59l-2.59 7.14h-4.29l11.44-30.33h4.52l11.39 30.33h-4.29l-2.59-7.14zm-1.14-3.11l-5.66-15.6-5.65 15.6h11.31zM463.67 212.92l-8.07-12.62h-4.34v12.62h-3.99v-30.9h10.17c3.51 0 6.14.84 7.89 2.52 1.75 1.68 2.63 3.91 2.63 6.68 0 2.51-.7 4.54-2.1 6.07-1.4 1.53-3.43 2.49-6.09 2.87l8.42 12.76h-4.52zm-12.4-15.52h5.83c4.53 0 6.8-1.99 6.8-5.96 0-3.97-2.27-5.96-6.8-5.96h-5.83v11.92z">
                </path>
                <g>
                  <path
                    d="M526.45 184.49c2.45 1.86 4.15 4.39 5.09 7.6h-4.21c-.79-2.04-2.06-3.67-3.81-4.89-1.75-1.22-3.9-1.82-6.45-1.82-2.01 0-3.82.49-5.41 1.47-1.59.98-2.85 2.38-3.77 4.21-.92 1.83-1.38 3.97-1.38 6.42 0 2.43.46 4.54 1.38 6.36.92 1.81 2.18 3.21 3.77 4.19 1.59.98 3.4 1.47 5.41 1.47 2.55 0 4.69-.61 6.45-1.82 1.75-1.21 3.02-2.84 3.81-4.89h4.21c-.93 3.21-2.63 5.75-5.09 7.6-2.45 1.86-5.56 2.78-9.33 2.78-2.89 0-5.45-.66-7.67-1.99-2.22-1.33-3.95-3.18-5.19-5.57-1.24-2.38-1.86-5.09-1.86-8.13 0-3.07.62-5.8 1.86-8.19 1.24-2.4 2.97-4.26 5.19-5.59s4.78-1.99 7.67-1.99c3.76 0 6.87.93 9.33 2.78zM567.76 183.64c2.29 1.34 4.09 3.22 5.41 5.63 1.32 2.41 1.97 5.14 1.97 8.18s-.66 5.76-1.97 8.17c-1.32 2.41-3.12 4.29-5.41 5.63-2.3 1.34-4.87 2.02-7.74 2.02-2.86 0-5.46-.67-7.78-2.02-2.33-1.34-4.14-3.22-5.46-5.63-1.32-2.41-1.98-5.13-1.98-8.17s.66-5.76 1.98-8.18c1.31-2.41 3.13-4.29 5.46-5.63 2.32-1.34 4.92-2.02 7.78-2.02 2.87 0 5.44.67 7.74 2.02zm-13.46 3.18c-1.68.98-3 2.38-3.94 4.21-.95 1.83-1.42 3.97-1.42 6.42 0 2.43.47 4.56 1.42 6.4.95 1.84 2.27 3.25 3.94 4.23 1.68.98 3.58 1.47 5.72 1.47 2.1 0 3.99-.5 5.68-1.49 1.68-.99 3-2.4 3.95-4.23.95-1.82 1.42-3.95 1.42-6.38 0-2.46-.47-4.6-1.42-6.42-.95-1.82-2.27-3.23-3.95-4.21-1.68-.98-3.57-1.47-5.68-1.47-2.13 0-4.04.49-5.72 1.47zM620.46 182.54v30.37h-3.99v-24.24l-9.68 24.24h-3.55l-9.73-24.15v24.15h-3.99v-30.37h4.78l10.78 25.51 10.61-25.51zM641.64 200.47v12.45h-3.99v-30.9h9.82c3.54 0 6.18.83 7.93 2.48s2.63 3.91 2.63 6.77c0 2.89-.91 5.15-2.72 6.77-1.81 1.62-4.43 2.43-7.85 2.43h-5.82zm10.72-4.87c1.07-1.02 1.6-2.47 1.6-4.34 0-1.93-.53-3.4-1.6-4.4-1.06-1.01-2.81-1.51-5.24-1.51h-5.48v11.79h5.48c2.43 0 4.17-.51 5.24-1.54zM687.96 205.77h-13.59l-2.59 7.14h-4.29l11.44-30.33h4.52l11.4 30.33h-4.29l-2.6-7.14zm-1.14-3.11l-5.65-15.6-5.66 15.6h11.31zM731.88 212.92h-3.99l-16.04-24.41v24.41h-3.99v-30.9h3.99l16.04 24.46v-24.46h3.99zM769.22 182.02l-10.12 19.2v11.7h-4.03v-11.7l-10.17-19.2h4.64l7.58 14.95 7.54-14.95z">
                  </path>
                </g>
              </g>
              <g>
                <path
                  d="M1.55 177.14c-1.24 0-1.54.72-.66 1.6l32.57 32.57c.88.88 2.61 1.6 3.86 1.6h31.25a2.27 2.27 0 002.26-2.26v-67.02a2.27 2.27 0 012.26-2.26h67.02a2.27 2.27 0 002.26-2.26v-31.25c0-1.24-.72-2.98-1.6-3.86L108.2 71.43c-.88-.88-1.6-.58-1.6.66v31.25a2.27 2.27 0 01-2.26 2.26H37.32a2.27 2.27 0 00-2.26 2.26v67.02a2.27 2.27 0 01-2.26 2.26H1.55z">
                </path>
                <path
                  d="M35.06 68.85a2.27 2.27 0 002.26 2.26h102.79a2.27 2.27 0 002.26-2.26V37.6c0-1.24-.72-2.98-1.6-3.86L108.2 1.17c-.88-.88-1.6-.58-1.6.66v31.25a2.27 2.27 0 01-2.26 2.26H37.32a2.27 2.27 0 00-2.26 2.26v31.25z">
                </path>
              </g>
            </g>
          </svg></a>
      </div>

      <div class="icons">
        <!-- Twitter -->
        <a href="/Twitter"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 21 17">
            <title>twitter</title>
            <desc>Directs user to our twitter page</desc>
            <path class="icon-twitter" fill-rule="evenodd"
              d="M20.782 2.118a8.569 8.569 0 0 1-2.449.67A4.27 4.27 0 0 0 20.21.437a8.574 8.574 0 0 1-2.708 1.03A4.267 4.267 0 0 0 14.389.126a4.256 4.256 0 0 0-4.154 5.215A12.117 12.117 0 0 1 1.447.904a4.24 4.24 0 0 0 1.32 5.67 4.26 4.26 0 0 1-1.932-.53v.054a4.254 4.254 0 0 0 3.419 4.164 4.21 4.21 0 0 1-1.924.074 4.263 4.263 0 0 0 3.981 2.95 8.563 8.563 0 0 1-5.294 1.817A8.83 8.83 0 0 1 0 15.045a12.104 12.104 0 0 0 6.536 1.908c7.842 0 12.131-6.474 12.131-12.086 0-.185-.004-.368-.013-.55a8.618 8.618 0 0 0 2.128-2.199">
            </path>
          </svg></a>

        <!-- Instagram -->
        <a href="/Insta"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 22 22">
            <title>instagram</title>
            <desc>Directs user to our instagram page</desc>
            <g class="icon-instagram" fill-rule="evenodd">
              <path
                d="M6.894 1.545c-2.479 0-4.497 2.011-4.497 4.482v9.046c0 2.47 2.018 4.481 4.497 4.481h8.508c2.48 0 4.498-2.01 4.498-4.481V6.027c0-2.47-2.019-4.482-4.498-4.482H6.894zm8.508 19.553H6.894c-3.335 0-6.048-2.702-6.048-6.025V6.027C.846 2.703 3.559 0 6.894 0h8.508c3.335 0 6.049 2.703 6.049 6.027v9.046c0 3.323-2.714 6.025-6.049 6.025z">
              </path>
              <path
                d="M11.018 6.801c-.91 0-1.777.355-2.45 1.007a3.794 3.794 0 0 0-1.149 2.713 3.728 3.728 0 0 0 3.73 3.716c2.045 0 3.684-1.642 3.73-3.738.023-1.056-.283-1.953-.883-2.591-.645-.687-1.64-1.07-2.875-1.105-.034-.002-.07-.002-.103-.002m.131 9.324c-3.103 0-5.626-2.514-5.626-5.604 0-1.525.628-3.008 1.725-4.07a5.393 5.393 0 0 1 3.927-1.537c1.752.052 3.206.641 4.205 1.702.946 1.007 1.428 2.365 1.395 3.925a5.74 5.74 0 0 1-1.668 3.94 5.548 5.548 0 0 1-3.958 1.644M18.223 4.757a1.31 1.31 0 0 1-1.313 1.307 1.31 1.31 0 0 1-1.312-1.307 1.31 1.31 0 0 1 1.312-1.308 1.31 1.31 0 0 1 1.313 1.308">
              </path>
            </g>
          </svg></a>

        <!-- LinkedIn -->
        <a href="/LinkedIn"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 22 21">
            <title>linkedin</title>
            <desc>Directs user to our linkedin page</desc>
            <g class="icon-linkedin" fill-rule="evenodd">
              <path
                d="M12.107 8.68v.044c-.019-.013-.008-.03 0-.044V6.79H7.653c.057 1.25 0 13.35 0 13.35h4.454v-7.456c0-.401.03-.796.146-1.082.324-.796 1.058-1.625 2.286-1.625 1.614 0 2.26 1.227 2.26 3.02v7.144h4.453v-7.655c0-4.102-2.2-6.01-5.13-6.01-2.363 0-3.422 1.293-4.015 2.204zM.733 20.141H5.19V6.79H.733zM2.99.35C1.467.35.47 1.348.47 2.659c0 1.28.966 2.307 2.46 2.307h.03c1.553 0 2.52-1.028 2.52-2.307C5.452 1.348 4.514.349 2.99.349">
              </path>
            </g>
          </svg></a>

        <!-- Facebook -->
        <a href="/Facebook"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 11 21">
            <title>facebook</title>
            <desc>Directs user to our facebook page</desc>
            <path class="icon-facebook" fill-rule="evenodd"
              d="M10.64 6.742H7.35v-2.15c0-.806.538-.995.916-.995h2.32V.05L7.388.037c-3.547 0-4.354 2.647-4.354 4.34v2.365H.982v3.655h2.053v10.346H7.35V10.397h2.912l.378-3.655z">
            </path>
          </svg></a>

        <!-- YouTube -->
        <a href="/YouTube"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 35">
            <title>youtube</title>
            <desc>Directs user to our youtube page</desc>
            <g fill="none" fill-rule="evenodd">
              <path fill="#ffffff"
                d="M48.955 5.5a6.282 6.282 0 0 0-4.42-4.448C40.635 0 25 0 25 0S9.364 0 5.465 1.052A6.282 6.282 0 0 0 1.045 5.5C0 9.425 0 17.614 0 17.614s0 8.188 1.045 12.113a6.283 6.283 0 0 0 4.42 4.449C9.365 35.227 25 35.227 25 35.227s15.636 0 19.535-1.051a6.283 6.283 0 0 0 4.42-4.45C50 25.803 50 17.615 50 17.615S50 9.425 48.955 5.5">
              </path>
              <path fill="#2e2e2e" d="M19.886 25.048l13.069-7.434-13.069-7.435v14.869"></path>
            </g>
          </svg></a>

        <!-- CodePen -->
        <a href="/CodePen"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 21 22">
            <title>codepen</title>
            <desc>Directs user to our codepen page</desc>
            <path class="icon-codepen" fill-rule="evenodd"
              d="M18.917 12.633l-2.214-1.477 2.214-1.475v2.952zm-7.646 6.257v-4.114l3.838-2.557 3.099 2.064-6.937 4.607zm-.885-5.646l-3.131-2.088 3.131-2.086 3.132 2.086-3.132 2.088zm-.885 5.646l-6.938-4.607 3.1-2.064L9.5 14.776v4.114zM1.854 9.681l2.215 1.475-2.215 1.477V9.681zm7.647-6.258v4.114l-3.839 2.56L2.563 8.03l6.938-4.607zm1.77 0l6.937 4.607-3.099 2.067-3.838-2.56V3.423zm9.409 4.492l-.007-.04a.746.746 0 0 0-.03-.116c-.006-.022-.014-.042-.022-.063l-.02-.044c-.01-.02-.019-.039-.03-.058-.008-.014-.016-.029-.025-.042a.78.78 0 0 0-.038-.053l-.03-.039-.044-.046c-.011-.012-.023-.025-.035-.035l-.05-.043-.04-.03c-.006-.003-.011-.007-.015-.011L10.877 1.04a.89.89 0 0 0-.982 0L.48 7.295l-.016.011-.039.03a.874.874 0 0 0-.05.043c-.013.01-.025.023-.037.035l-.043.046-.03.04a.78.78 0 0 0-.039.052l-.024.042-.031.058-.019.044a.528.528 0 0 0-.023.063.549.549 0 0 0-.014.043l-.015.074-.007.039a.844.844 0 0 0-.008.115v6.254c0 .04.002.078.008.116l.007.038c.004.025.01.05.015.074l.014.043c.007.02.014.043.023.065l.019.042.03.058c.01.015.018.028.025.042l.038.053a.797.797 0 0 0 .074.085c.012.012.024.025.037.035a.874.874 0 0 0 .05.043c.012.009.025.02.04.03.004.002.01.008.015.01l9.416 6.256a.888.888 0 0 0 .982 0l9.417-6.256.014-.01.04-.03.051-.043c.012-.01.024-.023.035-.035.016-.014.029-.03.044-.048a.421.421 0 0 0 .03-.037l.038-.053a.694.694 0 0 0 .025-.042c.011-.019.02-.038.03-.058l.02-.042c.008-.022.016-.044.022-.065a.55.55 0 0 0 .03-.117l.007-.038a.844.844 0 0 0 .008-.116V8.03a.844.844 0 0 0-.008-.115z">
            </path>
          </svg></a>

        <!-- Dribble -->
        <a href="/Dribble"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 22 22">
            <title>dribbble</title>
            <desc>Directs user to our dribbble page</desc>
            <path class="icon-dibbble" fill-rule="evenodd"
              d="M15.846 18.578c-.088-.533-.564-3.128-1.725-6.315 2.864-.456 5.345.326 5.528.386a8.831 8.831 0 0 1-3.803 5.929m-4.956 1.509c-2.15 0-4.118-.761-5.653-2.026.117.094.198.154.198.154s1.702-3.697 6.964-5.523a.437.437 0 0 1 .058-.018c1.249 3.233 1.766 5.939 1.895 6.713a8.843 8.843 0 0 1-3.462.7m-8.874-8.843c0-.093.004-.186.006-.278.159.002 4.543.102 9.11-1.26.254.495.498 1 .721 1.503a7.83 7.83 0 0 0-.35.105c-4.79 1.541-7.217 5.835-7.217 5.835l.003.004a8.788 8.788 0 0 1-2.273-5.909M7.102 3.25a52.97 52.97 0 0 1 3.295 5.095c-4.26 1.127-7.958 1.083-8.191 1.08a8.857 8.857 0 0 1 4.896-6.175m1.662-.589l-.003.003-.026.005.029-.008m7.985 1.95c-.022.034-1.286 1.95-4.634 3.202a45.06 45.06 0 0 0-3.316-5.158c.67-.163 1.37-.25 2.09-.25a8.85 8.85 0 0 1 5.86 2.206m3.012 6.547c-.13-.028-3.133-.671-6.183-.29a24.946 24.946 0 0 0-.782-1.74c3.507-1.422 4.93-3.472 4.945-3.498a8.799 8.799 0 0 1 2.02 5.528m1.307-1.995a10.125 10.125 0 0 0-.607-1.947 10.121 10.121 0 0 0-.957-1.758 10.473 10.473 0 0 0-2.806-2.796 10.415 10.415 0 0 0-1.765-.955 10.436 10.436 0 0 0-6.137-.603c-.666.136-1.324.34-1.953.603-.614.26-1.21.581-1.766.955-.548.37-1.065.795-1.537 1.265a10.401 10.401 0 0 0-2.225 3.29 10.334 10.334 0 0 0-.816 4.029c0 .702.07 1.404.21 2.085a10.2 10.2 0 0 0 1.565 3.705c.37.548.797 1.063 1.266 1.531.472.469.99.893 1.537 1.263.556.374 1.152.695 1.766.954.63.265 1.287.467 1.953.604a10.494 10.494 0 0 0 4.184 0 10.345 10.345 0 0 0 3.718-1.558 10.342 10.342 0 0 0 2.806-2.794 10.18 10.18 0 0 0 .957-1.76 10.271 10.271 0 0 0 .607-6.113">
            </path>
          </svg></a>

        <!-- Medium -->
        <a href="/Medium"><svg role="img"
            style="fill: rgb(255, 255, 255); transition: fill .35s; width: 22px; height: 22px;"
            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 26 20">
            <title>medium</title>
            <desc>Directs user to our medium page</desc>
            <path
              d="M2.999,4.08 C3.03012356,3.77027286 2.91117466,3.46435116 2.679,3.257 L0.32,0.423 L0.32,0 L7.652,0 L13.317,12.382 L18.299,0 L25.286,0 L25.286,0.423 L23.268,2.353 C23.0949663,2.48520391 23.0091638,2.70221099 23.045,2.917 L23.045,17.085 C23.0092307,17.30007 23.0949834,17.5173358 23.268,17.65 L25.24,19.578 L25.24,20.002 L15.323,20.002 L15.323,19.578 L17.366,17.602 C17.567,17.403 17.567,17.345 17.567,17.038 L17.567,5.585 L11.889,19.955 L11.121,19.955 L4.51,5.585 L4.51,15.216 C4.455,15.62 4.59,16.027 4.876,16.321 L7.532,19.531 L7.532,19.955 L0,19.955 L0,19.531 L2.656,16.321 C2.941,16.027 3.068,15.617 2.999,15.216 L2.999,4.08 Z">
            </path>
          </svg></a>
      </div>

      <div class="others">
        <a href="#"><span>Tailored Services</span></a>
        <a href="#"><span>Cookies & Privacy</span></a>
        <a href="#"><span>Accessbility</span></a>
        <a href="#"><span>Device Lab</span></a>
      </div>
      <div class="others2">
        <a href="#"><span>Site Map</span></a>
        <a href="#"><span>Carriers</span></a>
        <a href="#"><span>Infinity CRO</span></a>
      </div>

    </div>

  </div>
</template>

<script>
  export default {
    name: 'CRC',
    data() {
      return {
        name: "Hello CRC",
        message: '',
        wcrc: 'Website Conversion <br> Rate Calculator',
        wcrcMsg: 'Find out what a small increse in conversion is worth.',
        midHead: "Ensure you're getting the <br> most from your visitors.",
        midMsg: 'Enter your website statistics in to the fields below to discover how a small increase <br> in your website conversion rate can lead to a significant increase in revenue and <br> sales without increasing the number of visitors to your site .',
        visitors: 'WHAT IS YOUR AVAERAGE NUMBER <br>OF VISITORS? * <span>(PER MONTH OR PER <br> YEAR)</span>',
        conversion: '<span>WHAT IS YOUR AVERAGE WEBSITE <br>CONVERSION RATE ? * </span>',
        transaction: 'WHAT IS YOUR AVAERAGE NUMBER <br>TRANSACTION VALUE ? * <span>(AVERAGE <br> CHECKOUT, BASKET, OR SALES <br> VALUE)</span>',
        rateConversion: 'WHAT INCREASE IN CONVERSION <br> RATE DO YOU WANT? *',

      }
    },
    props: {
      msg: String,
    },
    methods: {
      /* handleClick: function() {
      alert('test')
     } */

      slider: document.getElementById('id-convrate'),
      output: document.getElementById("id-convratevalue"),


      /* output.innerHTML = slider.value + "%"; */

      querySelector: function querySelector(elementClassId) {
        return document.querySelector(elementClassId);
      },

      roundHundredth: function roundHundredth(a) {
        return Math.round(100 * a) / 100
      },

      displayErrorModal: function displayErrorModal(d, c, b) {},

      webConversion: function webConversionResults() {
        var r = parseFloat(querySelector("#id-numberofvisitors").value);
        var b = parseFloat(querySelector("#id-avgwebsite").value) / 100;
        var c = parseFloat(querySelector("#id-avgtransaction").value);
        var v = querySelector("#id-convrate").value / 100;
        var e = false;
        // if (isNaN(r)) {
        //    $("#ui_avg_visitors").addClass("error-input");
        //    e = true
        // } else {
        //    $("#ui_avg_visitors").removeClass("error-input")
        // }
        // if (isNaN(b)) {
        //    $("#ui_avg_conversion").addClass("error-input");
        //    e = true
        // } else {
        //    $("#ui_avg_conversion").removeClass("error-input")
        // }
        // if (isNaN(c)) {
        //    $("#ui_avg_transaction").addClass("error-input");
        //    e = true
        // } else {
        //    $("#ui_avg_transaction").removeClass("error-input")
        // }
        if (e) {
          return false
        }
        var q = "";
        var A = "";
        var n = 0;
        // if (r == 0 || r % 1 != 0) {
        //    q = "Invalid input for the first question";
        //    A = 'Only whole numbers apart from 0 are allowed for the first question: "What is your average number of visitors?"';
        //    n++
        // }
        // if (b <= 0 || b > 1) {
        //    q = "Invalid input for the second question";
        //    A = 'Values equal to 0 or over 100% are not allowed for the second question: "What is your average website conversion rate?"';
        //    n++
        // }
        // if (c == 0) {
        //    q = "Invalid input for the third question";
        //    A = 'The value 0 is not allowed for the third question: "What is your average transaction value?"';
        //    n++
        // }
        // if (n >= 2) {
        //    q = "Invalid inputs";
        //    A = "Only whole numbers apart from 0 are allowed for the first question.<br /><br />Values equal to 0 or over 100% are not allowed for the second question.<br /><br />The value 0 is not allowed for the third question.<br /><br />Fourth question: the conversion rate increase can't result in a conversion rate over 100%.";
        //    displayErrorModal(q, A);
        //    return false
        // } else {
        //    if (n == 1) {
        //          displayErrorModal(q, A);
        //          return false
        //    }
        // }
        var o = r;
        var u = b;
        var y = o * u;
        var l = y * c;
        var w = b * (1 + v);
        if (w > 1) {
          q = "Invalid input in your desired conversion rate increase";
          A =
            "A website conversion rate can't be superior to 100%, so we replace your input value by 100%. Please also consider that a 100% conversion rate is unlikely to happen.";
          displayErrorModal(q, A, true);
          w = 1;
          var k = 1;
          for (var x = 1, j = 0; x <= 250; x++) {
            if (j > 100) {
              k = x - 1;
              break
            }
            j = b * (1 + x)
          }
          k -= 100;
          $("#web_conversion_slider").slider("destroy");
          $("#web_conversion_slider").slider({
            create: function (i, C) {},
            value: k,
            min: 0,
            max: 250,
            slide: function (i, C) {
              $("#web_conversion_amt").text(C.value)
            },
            stop: function (i, C) {
              if ($("#web_conversion_results").css("visibility") != "hidden") {
                webConversionResults()
              }
            }
          });
          // $("#web_conversion_amt").text(k)
        }
        var d = o * w;
        var a = d * c;
        var s = w - u;
        var h = d - y;
        var g = a - l;
        var z = l / o;
        var m = o / y;
        var p = a / o;
        var f = o / d;
        var t = (p - z) / z;
        var B = (f - m) / m;
        var getAllElements = document.querySelectorAll(".output-row");
        for (var i = 0; i < getAllElements.length; i++) {
          var getAllChild = getAllElements[i].children;
          if (i == 0) {
            getAllChild[1].innerHTML = o;
            getAllChild[2].innerHTML = o;
          } else if (i == 1) {
            getAllChild[1].innerHTML = roundHundredth(u * 100) + "%";
            getAllChild[2].innerHTML = roundHundredth(w * 100) + "%";
            getAllChild[3].innerHTML = "+" + roundHundredth(s * 100) + "%";
          } else if (i == 2) {
            getAllChild[1].innerHTML = Math.round(y);
            getAllChild[2].innerHTML = Math.round(d);
            getAllChild[3].innerHTML = Math.round(h);
          } else if (i == 3) {
            getAllChild[1].innerHTML = "&pound; " + l;
            getAllChild[2].innerHTML = "&pound; " + roundHundredth(a);
            getAllChild[3].innerHTML = "&pound; " + roundHundredth(g);
          } else if (i == 4) {
            getAllChild[1].innerHTML = isNaN(roundHundredth(z)) ? "&pound; 0" : "&pound; " + roundHundredth(z);
            getAllChild[2].innerHTML = isNaN(roundHundredth(p)) ? "&pound; 0" : "&pound; " + roundHundredth(p);
            getAllChild[3].innerHTML = isNaN(roundHundredth(t * 100)) ? "+0%" : "+" + roundHundredth(t * 100) +
              "%";
          } else if (i == 5) {
            getAllChild[1].innerHTML = isNaN(roundHundredth(m)) ? 0 : roundHundredth(m);
            getAllChild[2].innerHTML = isNaN(roundHundredth(f)) ? 0 : roundHundredth(f);
            getAllChild[3].innerHTML = isNaN(roundHundredth(B * 100)) ? "0%" : roundHundredth(B * 100) + "%";
          }
        }
        querySelector("#web_conversion_results").style.display = "block";
        // if (w < 1) {
        //    $("html, body").animate({
        //          scrollTop: 500
        //    }, "slow", function () {})
        // }
        return false
      },



      


    }

  }
</script>


<style scoped>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .page {
    font-size: 18px;
  }

  .header {
    text-align: left;
    color: #fff;
    background-color: #c2395e;
    padding: 80px;
  }

  .middle {
    text-align: left;
    padding-top: 50px;
    padding-left: 80px;
  }

  .middle input {
    border: none;
    border-bottom: 2px solid #c3c3c3;
    width: 25%;
    margin: 0;
    padding: 0;
    line-height: 28px;
  }

  /* Input Slider */
  input[type="range"] {
    margin: auto;
    -webkit-appearance: none;
    position: relative;
    overflow: hidden;
    height: 30px;
    width: 25%;
    cursor: pointer;
    border-radius: 0;
  }

  ::-webkit-slider-runnable-track {
    background: #ddd;
  }

  ::-webkit-slider-thumb {
    -webkit-appearance: none;
    width: 40px;
    height: 40px;
    background: #d3d3d3;
    box-shadow: -100vw 0 0 100vw dodgerblue;
    border: 2px solid #999;
  }

  ::-moz-range-track {
    height: 45px;
    background: #ddd;
  }

  ::-moz-range-thumb {
    background: #fff;
    height: 60px;
    width: 20px;
    border: 3px solid #999;
    border-radius: 0 !important;
    box-shadow: -100vw 0 0 100vw dodgerblue;
    box-sizing: border-box;
  }

  ::-ms-fill-lower {
    background: dodgerblue;
  }

  ::-ms-thumb {
    background: #fff;
    border: 2px solid #999;
    height: 40px;
    width: 20px;
    box-sizing: border-box;
  }

  ::-ms-ticks-after {
    display: none;
  }

  ::-ms-ticks-before {
    display: none;
  }

  ::-ms-track {
    background: #ddd;
    color: transparent;
    height: 40px;
    border: none;
  }

  ::-ms-tooltip {
    display: none;
  }

  /* Input slider end */

  .inputMsg {
    margin-top: 50px;
  }

  button {
    background-color: #21a7ba;
    border: none;
    padding: 20px;
    border-radius: 5px;
    font-size: 20px;
    color: #fff;
  }

  .footer {
    background-color: #2e2e2e;
    margin-top: 25px;
    padding: 50px;
  }

  .footer span {
    margin: 0px 15px;
    float: left;
    color: #fff;
  }

  .foolproof {
    float: right;
  }

  .icons {
    margin-top: 60px;
    padding-right: 800px;
  }

  .icons a {
    /* float: left; */
    margin: 15px;
  }

  .others {
    padding-top: 80px;
  }

  .others2 {
    padding-top: 50px;
  }

  /*  Website Conversion CSS  */

  .label--desc {
    color: rgba(0, 0, 0, .3) !important;
    font-family: Poppins, Helvetica, Arial, sans-serif;
    font-size: 14px;
    font-weight: 700;
    line-height: 20px;
    letter-spacing: 1.6px;
    text-transform: uppercase;
    font-style: normal;
  }

  .label--unit {
    position: absolute;
    right: 0;
    bottom: 5px;
    padding: 0;
    font-family: Poppins, Helvetica, Arial, sans-serif;
    font-size: 14px;
    font-weight: 700;
    line-height: 20px;
    letter-spacing: 1.6px;
    text-transform: uppercase;
    font-style: normal;
  }

  .pos-aln--left {
    right: auto;
    left: 0;
  }

  .pad-lft--15 {
    padding-left: 15px;
  }

  .customslider {
    -webkit-appearance: none;
    width: 100%;
    height: 25px;
    background: #d3d3d3;
    outline: none;
    opacity: 0.7;
    -webkit-transition: .2s;
    transition: opacity .2s;
  }

  .customslider:hover {
    opacity: 1;
  }

  .customslider::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 25px;
    height: 25px;
    background: #4CAF50;
    cursor: pointer;
  }

  .customslider::-moz-range-thumb {
    width: 25px;
    height: 25px;
    background: #4CAF50;
    cursor: pointer;
  }

  #web_conversion_results {
    margin-top: 25px;
    display: none;
    position: relative;
  }

  .table-responsive {
    min-height: .01%;
    overflow-x: auto;
  }

  #web_conversion_results table#web_conversion_table {
    margin: 15px 0;
    padding: 0;
  }

  #web_conversion_results table {
    border-collapse: separate;
  }

  .table-bordered {
    border: 1px solid #ddd;
  }

  .table {
    width: 100%;
    max-width: 100%;
    margin-bottom: 20px;
  }

  table {
    background-color: transparent;
  }

  table {
    border-spacing: 0;
    border-collapse: collapse;
  }

  thead {
    display: table-header-group;
    vertical-align: middle;
    border-top-color: inherit;
    border-right-color: inherit;
    border-bottom-color: inherit;
    border-left-color: inherit;
  }

  tr {
    display: table-row;
    vertical-align: inherit;
    border-top-color: inherit;
    border-right-color: inherit;
    border-bottom-color: inherit;
    border-left-color: inherit;
  }

  #web_conversion_results table#web_conversion_table tr {
    padding: 0;
    margin: 0;
  }

  .table>caption+thead>tr:first-child>td,
  .table>caption+thead>tr:first-child>th,
  .table>colgroup+thead>tr:first-child>td,
  .table>colgroup+thead>tr:first-child>th,
  .table>thead:first-child>tr:first-child>td,
  .table>thead:first-child>tr:first-child>th {
    border-top: 0;
  }

  .table-bordered>thead>tr>td,
  .table-bordered>thead>tr>th {
    border-bottom-width: 2px;
  }

  .table-bordered>tbody>tr>td,
  .table-bordered>tbody>tr>th,
  .table-bordered>tfoot>tr>td,
  .table-bordered>tfoot>tr>th,
  .table-bordered>thead>tr>td,
  .table-bordered>thead>tr>th {
    border: 1px solid #ddd;
  }

  .table>thead>tr>th {
    vertical-align: bottom;
    border-bottom: 2px solid #ddd;
  }

  .table>tbody>tr>td,
  .table>tbody>tr>th,
  .table>tfoot>tr>td,
  .table>tfoot>tr>th,
  .table>thead>tr>td,
  .table>thead>tr>th {
    padding: 8px;
    line-height: 1.42857143;
    vertical-align: top;
    border-top: 1px solid #ddd;
  }

  #web_conversion_results table#web_conversion_table tr th {
    font-weight: bold;
    padding: 10px;
    text-align: center;
  }

  #web_conversion_table tr:nth-child(odd) {
    background-color: #F9F9FB;
  }

  #web_conversion_table tr th:nth-child(4) {
    background-color: #ECFFEC;
    border-left: 1px solid #009900;
    border-right: 1px solid #009900;
    border-top: 1px solid #009900;
  }

  #web_conversion_table tr td:nth-child(4) {
    color: #009900;
    font-weight: bold;
    background-color: #ECFFEC;
    border-left: 1px solid #009900;
    border-right: 1px solid #009900;
  }

  #web_conversion_table tr td:nth-child(even) {
    background-color: #E6F9E8;
  }

  #web_conversion_table tr:nth-child(6) td:nth-child(even) {
    border-bottom: 1px solid #009900;
  }

  /*  Website Conversion CSS end */
</style>