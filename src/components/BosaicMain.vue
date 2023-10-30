<template>
    <div class="header">
      <h1 class="logo">Webwork-Station</h1>
      <div class="navcontainer">
        <ul>
          <li>
  
            <div class="product" @mouseover="showPopup" @mouseleave="hidePopup">
              <a href="/home">Product</a>
              <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='20' height='20'><path d="M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z"></path></svg>
              <div class="popup" v-if="isHovered"> <!-- make sure you adjust popup postion to fall within mouseover distance of the linkdiv -->
                <div class="popupcontainer1content1" @mouseover="showsecondPopup" @mouseleave="hidesecondPopup" :class="{ 'popupcontainer1content1hover': isHovered2 }">
                  <h3 class="h3popupcontainer1content1">Bonsai Workflow</h3>
                  <p class="ppopupcontainer1content1">Look professional, win more clients and manage your business from &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  one place</p>
                  <div class="secondpopup" v-if="isHovered2" @mouseleave="hidesecondPopup">
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                              <div class="secondpopupcont" style="margin-bottom: 3.5rem;">
                                  <svg width="14" height="19" viewBox="0 0 14 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                  <path d="M12.2486 0H1.73654C0.821277 0 0.0763493 0.702774 0 1.5916C0 1.5916 0 6.81774 0 17.27C0 18.4378 0.714649 19 1.73654 19H12.2486C13.2142 19 14 18.2205 14 17.2622V1.73782C14 0.779453 13.2145 0 12.2486 0ZM13.1244 17.2619C13.1244 17.7409 12.7318 18.1307 12.2488 18.1307H1.73677C1.25385 18.1307 0.861192 17.7409 0.861192 17.2619V1.73759C0.861192 1.25841 1.25385 0.868796 1.73677 0.868796H12.2488C12.7318 0.868796 13.1244 1.25841 13.1244 1.73759V17.2619Z" fill="#4C4D5F"/>
                                  <path d="M11.2002 3.04004H2.80016C2.54243 3.04004 2.3335 3.2442 2.3335 3.49604C2.3335 3.74788 2.54243 3.95204 2.80016 3.95204H11.2002C11.4579 3.95204 11.6668 3.74788 11.6668 3.49604C11.6668 3.2442 11.4579 3.04004 11.2002 3.04004Z" fill="#4C4D5F"/>
                                  <path d="M7.31127 6.83984H2.80016C2.54243 6.83984 2.3335 7.044 2.3335 7.29584C2.3335 7.54769 2.54243 7.75184 2.80016 7.75184H7.31127C7.56901 7.75184 7.77794 7.54769 7.77794 7.29584C7.77794 7.044 7.56901 6.83984 7.31127 6.83984Z" fill="#4C4D5F"/>
                                  <path d="M11.2 15.96H7.46667C7.20893 15.96 7 16.1641 7 16.416C7 16.6678 7.20893 16.872 7.46667 16.872H11.2C11.4577 16.872 11.6667 16.6678 11.6667 16.416C11.6667 16.1641 11.4577 15.96 11.2 15.96Z" fill="#4C4D5F"/>
                                  <path d="M8.86683 9.12012H2.80016C2.54243 9.12012 2.3335 9.32428 2.3335 9.57612C2.3335 9.82796 2.54243 10.0321 2.80016 10.0321H8.86683C9.12456 10.0321 9.3335 9.82796 9.3335 9.57612C9.3335 9.32428 9.12456 9.12012 8.86683 9.12012Z" fill="#4C4D5F"/>
                                  <path d="M5.75572 11.3999H2.80016C2.54243 11.3999 2.3335 11.6041 2.3335 11.8559C2.3335 12.1077 2.54243 12.3119 2.80016 12.3119H5.75572C6.01345 12.3119 6.22238 12.1077 6.22238 11.8559C6.22238 11.6041 6.01345 11.3999 5.75572 11.3999Z" fill="#4C4D5F"/>
                                  </svg>
                                  <h3>Invoices</h3>
                                  <p>Get paid faster with automatic invoicing, online payments and more</p>
                              </div>
                          
                          </div>
                </div>
              </div>
            </div>
  
          </li>
  
          <li>
  
            <div class="templates" @mouseover="showtemplatepopup" @mouseleave="hidetemplatepopup">
              <a href="/about">Templates</a>
              <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='20' height='20'><path d="M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z"></path></svg>
              <div class="templatepopup" v-if="istemplateHovered"> <!-- make sure you adjust popup postion to fall within mouseover distance of the linkdiv -->
                      <div class="templatecontent1" @mouseover="showtemplatecontent1popup">
                          <h1>Legal self-representation</h1>
                          <div class="templatecontent1popup">this is </div>
                      </div>
                      <div class="templatecontent2" @mouseover="showtemplatecontent2popup" @mouseleave="hidetemplatecontent2popup">
                          <h1>Legal self-representation</h1>
                          <div class="templatecontent2popup" v-if="istemplatecontent2Hovered">and this is 2</div>
                      </div>
                      <div class="templatecontent3" @mouseover="showtemplatecontent3popup" @mouseleave="hidetemplatecontent3popup">
                          <h1>Legal self-representation</h1>
                          <div class="templatecontent3popup" v-if="istemplatecontent3Hovered">and this is 3</div>
                      </div>
                      
                  </div>
            </div>
            
          </li>
          <li class="pricing">
            <a href="/services">Pricing</a>
          </li>
          <li class="reviews">
            <a href="/contact">Reviews</a>
          </li>
        </ul>
      </div>
      
      <button class="login">LOGIN</button>
      <button class="startfree">START FREE</button>
    </div>
    <div class="bodycontainer">
  
      <div class="backgroundbox"></div>
      <img class="image" src="../assets/bonsai.png" alt="bon" >
      <div class="bodycontent1">
        <h1>Everything you need to run your business.</h1>
        <p>Bonsai's all-in-one product suite with smart automation lets you focus on your passion, not your paperwork.</p>
        <input type="text" placeholder="Enter your email">
        <button>START FREE</button>
                  
                  
      </div>
  
    </div>
  </template>
  
  <script>
  
  export default {
  data() {
  return {
  isHovered: false, // Initially, the popup is hidden
  isHovered2: false,
  istemplateHovered: false,
  istemplatecontent2Hovered: false,
  istemplatecontent3Hovered: false,
  };
  },
  methods: {
  showPopup() {
  this.isHovered = true; // Show the popup when hovering
  
  },
  hidePopup() {
  this.isHovered = false; // Hide the popup when not hovering
  
  },
  showsecondPopup() {
  this.isHovered2 = true; // Show the popup when hovering
  },
  hidesecondPopup() {
  this.isHovered2 = false; // Show the popup when hovering
  },
  showtemplatepopup() {
  this.istemplateHovered = true; // Show the popup when hovering
  
  },
  hidetemplatepopup() {
  this.istemplateHovered = false; // Hide the popup when not hovering
  
  },
  showtemplatecontent1popup() {
  this.istemplatecontent1Hovered = true; // Show the popup when hovering
  },
  hidetemplatecontent1popup() {
  this.istemplatecontent1Hovered = false; // Show the popup when hovering
  },
  showtemplatecontent2popup() {
  this.istemplatecontent2Hovered = true; // Show the popup when hovering
  },
  hidetemplatecontent2popup() {
  this.istemplatecontent2Hovered = false; // Show the popup when hovering
  },
  showtemplatecontent3popup() {
  this.istemplatecontent3Hovered = true; // Show the popup when hovering
  },
  hidetemplatecontent3popup() {
  this.istemplatecontent3Hovered = false; // Show the popup when hovering
  },
  },
  };
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style>
  @font-face {
  font-family: amerigobt;
  src: url(../assets/font/AmerigoBT.ttf);
  }
  
  @font-face {
  font-family: proximareg;
  src: url(../assets/font/proximanova-regular.otf);
  }
  
  @font-face {
  font-family: proximabold;
  src: url(../assets/font/proximanova-semibold.otf);
  }
  
  .header {
    position: fixed;
    top: 0rem;
    width: 100%;
    height: 5rem;
    background-color: rgb(255, 255, 255);
    display: flex;
    gap: 2rem;
    z-index: 100;
    
  }
  .logo {
    margin-right: 5.8rem;
    position: relative;
    left: 0.5rem;
    color: #00b289;
      font-family: amerigobt;
      letter-spacing: 1px;
  
  }
  .navcontainer {
    height: fit-content;
    
  
  }
  
  .navcontainer ul {
    list-style-type: none;
    display: flex;
    gap: 2.2rem;
    font-family: amerigotbt;
      font-size: 17px;
      letter-spacing: 1px;
      position: relative;
      top: 0.7rem;
      left: 0.3rem;
    /* margin: 0; */
  }
  .product {
    border-color: rgb(12, 12, 12);
    display: flex;
    gap: 0.1rem;
    
  }
  
  .product a {
    padding-bottom: 1.5rem;
    
  }
  .product a:hover {
      color: rgba(0, 0, 0, 0.959);
  }
  
  .product svg {
    position: relative;
    top: 0rem;
    fill: rgba(0, 0, 0, 0.669);
  }
  
  .popup {
      position: absolute;
      top: 2rem;
      left: -7.5rem;
      height: 33rem;
      width: 18rem;
      background-color: white;
      padding-right: 2rem;
      padding-left: 2rem;
      box-shadow: 20px 20px 40px rgba(0, 0, 0, 0.03),
                -20px -20px 40px rgba(0, 0, 0, 0.03),
                20px -20px 40px rgba(0, 0, 0, 0.03),
                -20px 20px 40px rgba(0, 0, 0, 0.03);
      display: flex;
      flex-direction: column;  
  }
  
  .popupcontainer1content1 {
      border-bottom-style: solid;
      padding-bottom: 2rem;
      border-width: 0.5px;
      border-color: silver;
      margin-top: 2rem;
      height: 8rem;
  
  }
  
  .popupcontainer1content1hover {
      border-bottom-style: solid;
      padding-bottom: 2rem;
      border-width: 0.5px;
      border-color: rgb(255, 255, 255);
      margin-top: 2rem;
      height: 8rem;
  }
  
  .h3popupcontainer1content1 {
      position: absolute;
      top: 2.5rem;
      font-family: amerigobt;
      font-size: 22px;
      color: rgba(0, 0, 0, 0.811);
      letter-spacing: 0.02em;
      font-weight: 200;
      margin-right: 2rem;
      margin-top: 1rem;
  }
  .ppopupcontainer1content1{
      position: absolute;
      top: 5rem;
      
      font-family: amerigotbt;
      font-size: 17px;
      width: 18rem;
      letter-spacing: 0.03em;
      color: rgba(0, 0, 0, 0.628);
  
  
  }
  .secondpopup{
      position: absolute;
      top: 0rem;
      bottom: 0rem;
      left: 20rem;
      height: 31rem;
      width: 38rem;
      background-color: white;
      padding-left: 3rem;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(3, 1fr);
  
      padding-top: 2rem;
      
      margin-bottom: 0rem;
  }
  .secondpopupcont {
  display:  flex;
  flex-direction: column;
  width: 17rem;
  height: 6rem;
  }
  
  .secondpopupcont:hover {
      background-color: rgba(0, 0, 0, 0.046);
  }
  
  .secondpopupcont svg {
      position: relative;
      top: 0.5rem;
  
  
  }
  
  .secondpopupcont h3 {
      position: relative;
      top: -1.8rem;
      left: 1.8rem;
      font-family: amerigotbt;
      font-size: 14px;
      color: rgba(0, 0, 0, 0.667);
      letter-spacing: 0.03em;
      margin-bottom: -2rem;
  
  
  
  }
  
  .secondpopupcont p {
      position: relative;
      left: 1.8rem;
      top: 0rem;
      bottom: -10rem;
      font-family: amerigotbt;
      font-size: 13.5px;
      letter-spacing: 0.03em;
      color: rgba(0, 0, 0, 0.628);
      width: 15rem;
  
  }
  
  .templates {
    border-color: rgb(5, 5, 5);
    display: flex;
    gap: 0.1rem;
  }
  
  .templates a {
    padding-bottom: 1.5rem;
  
  }
  .templates a:hover {
      color: rgba(0, 0, 0, 0.959);
  }
  
  
  .templates svg {
    position: relative;
    top: 0rem;
    fill: rgba(0, 0, 0, 0.669);
  
  
  }
  
  .templatepopup {
      position: absolute;
      top: 2.5rem;
      left: -16rem;
      height: 50rem;
      width: 26rem;
      background-color: white;
      padding-right: 2rem;
      padding-left: 3rem;
      box-shadow: 20px 20px 40px rgba(0, 0, 0, 0.03),
                -20px -20px 40px rgba(0, 0, 0, 0.03),
                20px -20px 40px rgba(0, 0, 0, 0.03),
                -20px 20px 40px rgba(0, 0, 0, 0.03);
      display: flex;
      flex-direction: column;  
  }
  .templatecontent1 {
  
  }
  
  .templatecontent1popup {
      position: absolute;
      top: 0rem;
      left: 30rem;
      height: 50rem;
      width: 40rem;
      background-color: white;
      display: flex;
      flex-direction: column;
      gap: 4rem;
      z-index: 0;
      transition: 10s;
      border-style: solid;
  }
  
  .templatecontent2popup {
      position: absolute;
      top: 0rem;
      left: 30rem;
      height: 50rem;
      width: 40rem;
      background-color: white;
      display: flex;
      flex-direction: column;
      gap: 4rem;
      z-index: 0;
      transition: 10s;
      border-style: solid;
  }
  
  .templatecontent3popup {
      position: absolute;
      top: 0rem;
      left: 30rem;
      height: 50rem;
      width: 40rem;
      background-color: white;
      display: flex;
      flex-direction: column;
      gap: 4rem;
      z-index: 0;
      transition: 10s;
      border-style: solid;
  }
  
  
  .pricing {
    position: relative;
    top: 2px;
  }
  .reviews {
    position: relative;
    top: 2px;
  }
  .navcontainer li {
    
  }
  .navcontainer a {
    text-decoration: none;
    color: rgba(0, 0, 0, 0.669);
  }
  
  .login {
  
  
  color: #00b289;
  background-color: white;
  border-style: solid;
  border-color: #00b289;
  border-width: 0.5px;
  font-family: amerigotbt;
  font-weight: 600;
  padding: 11px;
  width: 5.7rem;
  height: 2.4rem;
  border-radius: 4px;
  position: relative;
  top: 1.2rem;
  left: 4.8rem;
  
  }
  .login:hover {
    background-color: hsl(166, 100%, 36%);
    border-color: #00b289;
    color: white;
  }
  
  .startfree {
    color: white;
    background-color: #00b289;
    border-color: #00b289;
    border-style: solid;
    border-width: 0.5px;
    font-family: amerigotbt;
    font-weight: 600;
    padding: 11px;
    width: 8.4rem;
    height: 2.4rem;
    border-radius: 4px;
    position: relative;
    top: 1.2rem;
    left: 3.8rem;
  
  
  }
  .startfree:hover {
    background-color: hsl(166, 100%, 30%);
    border-color: #00b289;
  }
  
  
  .bodycontainer {
      height: 100rem;
      overflow: hidden;
  }
  .backgroundbox {
      position: relative;
      z-index: -1rem;
      left: 31rem;
      bottom: 23rem;
      width: 50rem;
      height: 50rem;
      background-color: rgb(230, 244, 253);
      rotate: -23deg;
      border-radius: 6rem;
      
  }
  
  .bodycontent1 {
    width: 30rem;
    position: absolute;
    left: 4rem;
    bottom: 4.5rem;
  
  }
  
  .bodycontent1 h1 {
    font-family: amerigobt;
    width: 28rem;
    font-size: 39px;
    letter-spacing: 2px;
    line-height: 3.5rem;
    color: rgb(76, 82, 90);;
    
  
  }
  
  .bodycontent1 p {
    font-family: amerigobt;
    width: 28rem;
    font-size: 21px;
    font-weight: 600;
    margin-bottom: 2.5rem;
    color: rgb(76, 82, 90);;
  
    
  
  }
  
  .bodycontent1 input {
    height: 4rem;
    width: 18rem;
    border-style: solid;
    border-color: #00b289;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
  
    
  
  }
  
  .bodycontent1 input :placeholder {
    height: 4rem;
    width: 18rem;
    border-style: solid;
    border-color: #00b289;
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
  
    
  
  }
  
  .bodycontent1 button {
    height: 4.38rem;
    width: 10rem;
    color: white;
    background-color: #00b289;
    border-color: #00b289;
    border-style: solid;
    border-width: 0.5px;
    font-family: amerigotbt;
    font-weight: 600;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    
  
  }
  
  .bodycontent1 button:hover {
    background-color: hsl(166, 100%, 36%);
    border-color: #00b289;
    color: white;
  }
  
  
  .image {
      width: 42rem;
      height: auto;
      position: relative;
      bottom: 36.5rem;
      left: 41.3rem;
  }
  
  
  
  
 
  </style>
  