<template>

<li class="casino-game-list-item" v-for="{id, image, bonus_text, description, detail_link, money_bonus, reviews_quantity, reviews_link, mark, visit_link } in casinoGames" :key="id">
  <img :src="image" alt="game-logo" class="game-logo-img">
  <div class="promo-content">
    <h5 class="bonus-text">{{bonus_text}}</h5>
    <div class="description-content">
      <p class="description">{{description}}</p>
      <a :href="detail_link" class="more-link">More</a>
    </div>
  </div>
  <p class="price">£{{money_bonus}}</p>
  <div class="rate-container">
    <p class="rate-signature">Rate it! ({{reviews_quantity}})</p>
    <ul class="list-inline rating-list">
      <li><i class="fa fa-star" title="Rate 5"></i></li>
      <li><i class="fa fa-star" title="Rate 4"></i></li>
      <li><i class="fa fa-star" title="Rate 3"></i></li>
      <li><i class="fa fa-star" title="Rate 2"></i></li>
      <li><i class="fa fa-star" title="Rate 1"></i></li>
    </ul>
    <a class="read-review-link" :href="reviews_link" >Read Review</a>
  </div>
  <p class="mark">{{mark}}</p>
  <a :href="visit_link" class="visit-site-btn">VISIT SITE</a>
</li>

</template>

<script>
export default {
  props: ['casinoGames']
}

</script>

<style>

.game-logo-img {
  width: 276px;
  border-radius: 4px;
  margin: 0 auto 30px;
}

.rating-list li {
  float: right;
  color: #ddd;
  padding: 10px 5px;
}

.rating-list li:hover,
.rating-list li:hover ~ li {
  color: red;
}

.rating-list {
  display: inline-block;
  list-style: none;
}
.bonus-text {
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: 28px;
  letter-spacing: 0em;
  text-align: center;
  color: var(--main-color);
  max-width: 44%;
  margin: 0 auto  10px;
}
.description {
  color: var(--main-color);
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  width: 100%;
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: 14px;
  letter-spacing: 0em;
  text-align: center;
}
.more-link{
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: 14px;
  letter-spacing: 0em;
  text-align: center;
  color: var(--main-color);
  text-decoration: underline;
}
.description-content {
  display: flex;
  align-items: flex-end;
}
.promo-content {
  margin-bottom: 30px;
}
.price {
  color: var(--main-color);
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  line-height: 28px;
  letter-spacing: 0em;
  text-align: center;
  margin-bottom: 30px;
}
.rate-container{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.rate-signature {
  color: var(--main-color);
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 19px;
  letter-spacing: 0em;
  text-align: center;
  margin-bottom: 8px;
  width: 100%;
}
.read-review-link {
  width: 100%;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 23px;
  letter-spacing: 0em;
  text-align: center;
  text-decoration: underline;
  color: var(--main-color);
}
.mark {
  font-size: 64px;
  font-style: normal;
  font-weight: 500;
  line-height: 75px;
  letter-spacing: 0em;
  text-align: left;
  color: var(--main-color);
  margin: 30px auto;
  text-align: center;
}
.visit-site-btn {
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 21px;
  letter-spacing: 0em;
  text-align: center;
  color: white;
  width: 184px;
  height: 48px;
  background-color: #ED1C49;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 4px;
  margin: 0 auto;
}
.casino-game-list-item {
  padding: 40px 0px;
}
.casino-game-list-item {
  border-bottom: 1px solid #D1D1D1;
  margin: 0 20px
}
.casino-game-list-item:last-child {
  border-bottom: none;
}
@media screen and (min-width: 768px) {
  .description-content {
    max-width: 227px;
    margin: 0 auto;
  }
  .bonus-text {
    font-size: 24px;
  }
}
@media screen and (min-width: 1024px) {
.casino-game-list-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
  .casino-game-list-item:after {
    display: none;
  }
  .bonus-text {
    max-width: 100%;
  }

}
@media screen and (min-width: 1440px) {
  .casino-game-list-item {
    padding: 80px 0px;
  }
  .casino-game-list-item {
    border-bottom: 1px solid #D1D1D1;
    margin: 0 35px
  }
  .casino-game-list-item:last-child {
    border-bottom: none;
  }
  .casino-game-list-item .game-logo-img {
    margin: 0 30px 0 0;
  }
  .bonus-text {
    max-width: 60%;
  }
  .rate-container {
    max-width: 145px;
    margin-right: 30px;
  }
  .mark{
    margin: 0 30px 0 auto;
  }
  .description-content {
    max-width: 211px;
  }
  .promo-content {
    margin-bottom: 0px;
    margin-right: 30px;
  }
  .price {
    margin-bottom: 0;
    margin-right: 30px;
  }


}
</style>
