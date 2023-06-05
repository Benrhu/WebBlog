<script lang="ts">
export default {
  name: "PricingPerUser",
  data() {
    return {
      numEmployees: 0,
      basicPrice: 0,
      premiumPrice: 0,
      enterprisePrice: 0,
      showPlans: true,
    };
  },
  methods: {
    calculatePrice(): void {
      const basicPlan = 4;
      const premiumPlan = 8;
      const enterprisePlan = 12;

      this.basicPrice = this.numEmployees * basicPlan;
      this.premiumPrice = this.numEmployees * premiumPlan;
      this.enterprisePrice = this.numEmployees * enterprisePlan;

      if (this.numEmployees >= 500) {
        this.showPlans = false;
      } else {
        this.showPlans = true;
      }
    },
    updatePrice() {
      this.calculatePrice();
    },
    updateSlider(event: Event) {
      const target = event.target as HTMLInputElement;
      this.numEmployees = parseInt(target.value, 10);
      this.calculatePrice();
    },
  },
};
</script>

<template>
  <div class="pricing dark:bg-elucidator-900">
    <div class="pricing__slider">
      <input
        type="range"
        min="10"
        max="500"
        v-model="numEmployees"
        @input="updateSlider"
        class="slider__input"
      />
      <div class="slider__labels">
        <span class="slider__label">0</span>
        <span class="slider__label">250</span>
        <span class="slider__label">500</span>
      </div>
    </div>
    <div class="pricing__details mb-24">
      <div class="details__employees">
        <h2 class="text-elucidator-700 dark:text-dark-repulser-400">Empleados:</h2>
        <input
          type="number"
          v-model.number="numEmployees"
          @input="updatePrice"
          class="employees__count w-1/2"
          min="0"
        />
      </div>
    </div>
    <div class="pricing-plans dark:text-white">
      <template v-if="showPlans">
        
        <div class="pricing__plan">
          <h2 class="plan__title">Básico</h2>
          <div class="plan__price">
            <span class="price__amount">{{ basicPrice }}€</span>
            <span class="price__period">/mes</span>
          </div>
          <ul class="plan__features">
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>5 allowed behaviors
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>10 allowed rules
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Tokens management
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>User roles
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Basic analytics
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Basic support
            </li>
          </ul>
          <button class="plan__button">Hire</button>
        </div>

        <div class="pricing__plan">
          <h2 class="plan__title">Premium</h2>
          <div class="plan__price">
            <span class="price__amount">{{ premiumPrice }}€</span>
            <span class="price__period">/monthly</span>
          </div>
          <ul class="plan__features">
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>10 allowed behaviors
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>10 allowed rules
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Tokens management
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>User roles
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Advanced analytics
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Priority support
            </li>
          </ul>
          <button class="plan__button">Hire</button>
        </div>

        <div class="pricing__plan">
          <h2 class="plan__title">Enterprise</h2>
          <div class="plan__price">
            <span class="price__amount">{{ enterprisePrice }}€</span>
            <span class="price__period">/monthly</span>
          </div>
          <ul class="plan__features">
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Unlimited behaviors
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Unlimited rules
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Tokens management
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>User roles
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>Advanced analytics
            </li>
            <li class="feature flex">
              <i class="gg-check-o mr-2"></i>24/7 support
            </li>
          </ul>
          <button class="plan__button">Hire</button>
        </div>
      </template>
      <template v-else>
        <div class="hablemos">
          <h2 class="plan__title">Hablemos</h2>
          <div class="plan__price">
            <span class="price__period text-center"
              >Nuestro equipo puede ayudarte a encontrar la mejor solución para
              tus necesidades</span
            >
          </div>
          <button class="plan__button">Hire</button>
        </div>
      </template>
    </div>
  </div>
</template>

<style>
.pricing {
  display: flex;
  margin-bottom: auto;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.pricing__title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 20px;
  text-align: center;
  color: black;
}

.pricing__slider {
  width: 300px;
  position: relative;
}

.slider__input {
  width: 100%;
  -webkit-appearance: none;
  background-image: linear-gradient(to right, white, blue);
  height: 8px;
  border-radius: 4px;
  outline: none;
  opacity: 0.7;
  transition: opacity 0.2s;
}

.slider__input:hover {
  opacity: 1;
}

.slider__input::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 16px;
  height: 16px;
  background-color: blue;
  border-radius: 50%;
  cursor: pointer;
}

.slider__labels {
  display: flex;
  justify-content: space-between;
  margin-top: 8px;
  color: blue;
  font-size: 12px;
}

.pricing__details {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}

.details__employees,
.details__price {
  display: flex;
  flex-direction: wrap;
  align-items: center;
  margin: 0 20px;
  color: blue;
  font-size: 14px;
}

.employees__count {
  width: 100px;
  height: 40px;
  font-size: 24px;
  font-weight: bold;
  color: #6b7280;
  border-radius: 50px 50px 50px;
  text-align: center;
}

.employees__label,
.price__label {
  margin-top: 4px;
}

.price__amount {
  font-size: 24px;
  font-weight: bold;
  color: #6b7280;
}

.pricing-plans {
  display: flex;
  justify-content: center;
  flex-wrap: nowrap;
  gap: 40px;
  width: 100%;
}

.pricing__plan {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  width: 380px;
  background-color: #0093e9;
  background-image: linear-gradient(160deg, #0093e9 0%, #80d0c7 100%);
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.pricing__plan:hover {
  transform: scale(1.05);
}

.plan__title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 4px;
  margin-right: 20px;
  color: white;
}

.plan__price {
  display: flex;
  align-items: baseline;
  margin-bottom: 20px;
}

.price__currency {
  font-size: 16px;
  font-weight: bold;
  margin-right: 2px;
  color: white;
}

.price__amount {
  font-size: 36px;
  font-weight: bold;
  margin-right: 2px;
  color: white;
}

.price__period {
  font-size: 16px;
  color: white;
}

.plan__features {
  list-style: none;
  padding: 0;
  margin-bottom: 20px;
  width: 300px;
}

.feature {
  margin-bottom: 8px;
  color: white;
}

.plan__button {
  padding: 12px 24px;
  background-color: white;
  color: black;
  font-size: 16px;
  font-weight: bold;
  border: none;
  border-radius: 50px 50px 50px;
  cursor: pointer;
}

.plan__button:hover {
  background-color: skyblue;
}

.hablemos {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  width: 800px;
  height: 200px;
  background-color: #0093e9;
  background-image: linear-gradient(160deg, #0093e9 0%, #80d0c7 100%);
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}
</style>
