<script>
export default {
  data() {
    return {
      boxLeft: 0,
      boxTop: 0,
    }
  },
  methods: {
    getSpotInfo(e){ 
      console.dir(e)
      this.boxLeft = e.clientX;
      this.boxTop = e.clientY; 
    },
    
  },
  mounted() {
    
  }
}
</script>

<template>
  <div class="header">
    <div class="header__left">
      <div class="logo-area">
        <img src="https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png" alt="">
        <h3>MyApp</h3>
      </div>
    </div>
    <div class="header__right">
      <div class="header__right__search">
        <div class="search_box">
          <i class="fas fa-search"></i>
          <input type="text" class="input__box">
        </div>
      </div>
      <div class="header__user_area">
        <div class="user__area">
          <div class="user__icon">
            <i class="fas fa-user"></i>
            <p>{{ name }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="main_ground">
    <div class="sidebar__nav">
      <div class="icon__only">
        <ul>
          <li>
            <a href=""><i class="fas fa-vector-square"></i></a>
          </li>
          <li class="active">
            <a href=""><i class="fas fa-folder-open"></i></a>
          </li>
          <li>
            <a href=""><i class="fas fa-calendar-alt"></i></a>
          </li>
          <li>
            <a href=""><i class="fas fa-users"></i></a>
          </li>
          <li>
            <a href=""><i class="fas fa-window-restore"></i></a>
          </li>
          <li>
            <a href=""><i class="fas fa-cog"></i></a>
          </li>
        </ul>
      </div>
      <div class="child_of_icon_manu">
          <div class="loaded_items">
            <div class="title-of-parent">
              <h3><i class="fas fa-chevron-left"></i> Task Board</h3> 
            </div>
            <ul>
                <li><a href="">All Items</a></li>
                <li class="active"><a href="">Assigned Task</a>
                  <ul>
                    <li><a href="">Task one</a></li>
                    <li><a href="">Task two</a></li>
                    <li><a href="">Task three</a></li>
                    <li><a href="">Task four</a></li>
                    <li><a href="">Task five</a></li>
                  </ul>
                </li>
                <li><a href="">Created by me</a></li>
                <li><a href="">History</a>
                  <ul>
                    <li><a href="">History one</a></li>
                    <li><a href="">History two</a></li>
                    <li><a href="">History three</a></li>
                    <li><a href="">History four</a></li>
                    <li><a href="">History five</a></li>
                  </ul>
                </li>
                <li><a href="">Latest Activity</a></li> 
            </ul>
          </div>
      </div>
    </div>
    <div class="content__area">
      <div class="fixedBox" :style="{ left: boxLeft + 'px', top: boxTop + 'px' }">
        FixedBox
      </div>
      <h3 @click="getSpotInfo" style="margin-left: 134px; margin-top: 156px;">Spot One</h3>
      <h3 @click="getSpotInfo" style="margin-left: 350px; margin-top: 200px;">Spot Two</h3>
    </div>
  </div>
</template>
