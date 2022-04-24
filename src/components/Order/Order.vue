<template>
  <div class="card">
    <header class="card-header" />
    <article class="card-content">
      <div class="card-content-title">Order Summary</div>
      <div class="card-content-text">
        You can now listen to millions of songs, audiobooks, and podcasts on any
        device anywhere you like!
      </div>
      <div class="card-plan">
        <div class="card-plan-details">
          <img :src="musicIcon" />
          <div class="card-plan-content">
            <span class="annual-plan">Annual Plan</span>
            <span class="price">$59.99/year</span>
          </div>
        </div>
        <a href="#" class="card-change">Change</a>
      </div>
      <button class="btn-payment">Proceed to Payment</button>
      <button class="btn-cancel">Cancel Order</button>
    </article>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import musicIcon from "../../assets/images/icon-music.svg";

export default defineComponent({
  name: "Order",
  data() {
    return {
      musicIcon,
    };
  },
  setup() {},
});
</script>

<style lang="scss" scoped>
@import "../../assets/main.scss";
.card {
  width: 450px;
  height: 697px;
  border-radius: 20px;
  background: white;
  box-shadow: 1px 24px 34px -5px rgba(0, 0, 0, 0.27);
  -webkit-box-shadow: 1px 24px 34px -5px rgba(0, 0, 0, 0.27);
  -moz-box-shadow: 1px 24px 34px -5px rgba(0, 0, 0, 0.27);
  @media screen and (max-width: 500px) {
    width: 327px;
    height: 567px;
  }
}
header {
  background: url("../../assets/images/illustration-hero.svg");
  background-repeat: no-repeat;

  width: 100%;
  height: 220px;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  @media screen and (max-width: 500px) {
    width: 100%;
    height: 160px;
    background-size: contain;
  }
}
.card-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .card-content-title {
    font-size: 28px;
    color: $dark-blue;
    font-weight: 900;
    text-align: center;
    margin-top: 1.2em;
    margin-bottom: 1em;
  }
  .card-content-text {
    font-size: 16px;
    font-weight: 500;
    color: $grey;
    text-align: center;
    width: 354px;
    margin-bottom: 20px;
    @media screen and (max-width: 500px) {
      width: 263px;
    }
  }
  .card-plan {
    border-radius: 11px;
    width: 354px;
    height: 98px;
    background: #f7f9ff;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 2.5em;
    @media screen and (max-width: 500px) {
      width: 85%;
      height: 81px;
      margin-bottom: 1.5em;
    }
    a {
      margin: 0 20px;
      color: $bright-blue;
      font-size: 14px;
      font-weight: bold;
      &:hover {
        color: $pale-purple;
        transition: all ease 0.3s;
      }
      @media screen and (max-width: 500px) {
        font-size: 13px;
      }
    }
    .card-plan-details {
      display: flex;
      margin: 0 20px;

      img {
        width: 48px;
        height: 48px;
        margin-right: 20px;
      }
      .card-plan-content {
        display: flex;
        flex-direction: column;
        .annual-plan {
          font-size: 16px;
          font-weight: bold;
          color: $dark-blue;
          margin-bottom: 4px;
          @media screen and (max-width: 500px) {
            font-size: 14px;
          }
        }
        .price {
          font-size: 16px;
          color: $grey;
          @media screen and (max-width: 500px) {
            font-size: 14px;
          }
        }
      }
    }
  }
  .btn-payment {
    width: 354px;
    height: 50px;
    background: #382ae1;
    color: #fff;
    border-radius: 11px;
    outline: none;
    border: none;
    font-size: 15px;
    font-weight: bold;
    margin-bottom: 30px;
    cursor: pointer;
    box-shadow: -2px 14px 31px -5px rgba(56, 42, 225, 0.35);
    -webkit-box-shadow: -2px 14px 31px -5px rgba(56, 42, 225, 0.35);
    -moz-box-shadow: -2px 14px 31px -5px rgba(56, 42, 225, 0.35);
    &:hover {
      background: $pale-purple;
      transition: all ease 0.3s;
    }
    @media screen and (max-width: 500px) {
      width: 85%;
      margin-bottom: 1em;
    }
  }
  .btn-cancel {
    border: none;
    background: transparent;
    outline: none;
    color: $grey;
    font-size: 15px;
    font-weight: 900;
    cursor: pointer;
    &:hover {
      color: $dark-blue;
      transition: all ease 0.3s;
    }
  }
}
</style>
