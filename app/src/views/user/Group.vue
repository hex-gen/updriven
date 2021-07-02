<template>
  <TopNav />

  <div class="app-container">

    <div class="left-container">
      <div class="wrapper" data-simplebar>
        <LeftNav @on-click="(tab) => onClickTab(tab)" />
      </div>
    </div>
    
    <div class="right-container" data-aos="fade-up" data-aos-delay="150">
      <div class="wrapper" data-simplebar>
        <div>
          <SectionSponsored />
        </div>
        <div class="mt-6">
          <SectionLive />
        </div>
      </div>
    </div>

    <div class="middle-container scroll-group">

        <div class ="group-container bshadow">
            <ShowGroup01/>
        </div>

        <div class ="group-container bshadow">
            <ShowGroup02/>
        </div>

        <div class ="right-container">
          <div class="search-container" style="width: 61%">
            <form action="/" method="GET">
              <FormGroup 
                placeholder="Search Group" wrapperClass="append" 
                icon="search.png"
              />
            </form>
          </div>
          <div class="search-container">
          <SectionSearchGroup/>
          </div>
        
        </div>

    </div>

  </div>
</template>

<script>
import TopNav from '../../components/TopNav';
import LeftNav from '../../components/LeftNav';
import PostNew from '../../components/PostNew';
import PostMultiple from '../../components/PostMultiple';
import SectionSponsored from '../../components/SectionSponsored';
import SectionLive from '../../components/SectionLive';
import ShowGroup01 from '../../components/ShowGroup01';
import ShowGroup02 from '../../components/ShowGroup02';
import SectionSearchGroup from '../../components/SectionSearchGroup';

export default {
  name: 'UserGroupPage',
  components: {
    TopNav,
    LeftNav,
    PostNew,
    PostMultiple,
    SectionSponsored,
    SectionLive,
    ShowGroup01,
    ShowGroup02,
    SectionSearchGroup
  },
  
  mounted() {
    AOS.init({ easing: 'ease-in-out-cubic', duration: 750, once: true, offset: 10 });
  },
  methods: {
    createPost(post) {
      this.$refs['posts'].createPost(post);
    },
    onClickTab(tab) {
      if(tab.link=='javascript:'){
        this.$refs['posts'].updateCategory(tab);
      }else{
        window.location.href = tab.link;
      }
    }
  }
  
}
</script>
