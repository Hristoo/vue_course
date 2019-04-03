<template>
    <div class="main">
      
        <div id="list-complete" class="demo" style="margin-top: 20px; margin-bottom: 20px; padding: 10px; background-color: #e4e4e4;">
          
          <button class="btn" v-on:click="filter('all')">Всички</button>
          <button class="btn" v-on:click="filter('tag1')">Български</button>
          <button class="btn" v-on:click="filter('tag2')">Английски</button>
          <transition-group name="list-complete"
            class="list-complete"      tag="section">
            <div
              v-for="item in filteredItems"
              v-bind:key="item.id"
              class="list-complete-item"
            >
              <img class="list-complete-img" :src="item.img" alt="" />
            </div>
          </transition-group>
        </div>



  </div>  
</template>

<script>
export default {
  computed: {
          showAlert() {
            return this.name.length > 4 ? true : false
          }
        },
    data(){
        return {
            title: 'Проекти разработени от мен',
            items: [
            { id: 1, tags: ['all', 'tag3'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/02/ili1-1.jpg'},
            { id: 2, tags: ['all', 'tag2'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/02/Jonas.jpg'},
            { id: 3, tags: ['all', 'tag1'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/02/parking.jpg' },
            { id: 4, tags: ['all', 'tag1'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/06/rabotavanglia1.jpg' },
            { id: 5, tags: ['all', 'tag2'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/02/joansremovalsbethnalgreen.jpg' },
            { id: 6, tags: ['all', 'tag2'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/05/cleaningcompanycanarywharf.co_.uk_.jpg' },
            { id: 7, tags: ['all', 'tag1'], img: 'https://scontent-sof1-1.xx.fbcdn.net/v/t1.0-9/33525792_198087317672251_7691889413244059648_o.png?_nc_cat=100&_nc_ht=scontent-sof1-1.xx&oh=f514e00a34749e7d5bdf7069a15930f0&oe=5D0C0C13' },
            { id: 8, tags: ['all', 'tag2'], img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/02/Jonas.jpg' },
            ],
            currentTag: 'all'
        }
    },
        computed: {
          filteredItems: function() {
            var filter = this.currentTag;
            return this.items.filter(function(item) {
                return item.tags.indexOf(filter) !== -1;
            });
          }
        },
        methods: {
          shuffle: function () {
            this.items = _.shuffle(this.items)
          },
          filter: function(tag) {
            this.currentTag = tag;
          }
        }
}
</script>

<style scoped>
.list-complete {
  display: flex;
  width: 100%;
  flex-direction: row;
  flex-wrap: wrap;

}
.list-complete-item {
  transition: transform 1s;
  flex: 1 1 25%;
  height: 200px;
  max-width: 25%;
  padding: 10px;
/*   display: inline-block;
  margin-right: 10px; */
}
.list-complete-img {
  object-fit: cover;
  height: 100%;
  width: 100%;
}
.list-complete-enter, .list-complete-leave-to
/* .list-complete-leave-active for <2.1.8 */ {
  opacity: 0;
  transform: translateY(30px);
}
.list-complete-leave-active {
  position: absolute;
}
.main{
  padding-top: 60px;
}
</style>
