<script setup>
definePageMeta({
  layout: "landing",
});

const pricing = [
  {
    name: "SecretAI Basic",
    price: "Free",
    popular: false,
    features: [
      "Free until migration to Raydium",
      "Limited-access; throttling after extensive use",
      "Mental Health Prompt",
      "Lifelike Voice Chat",
      "Get help with any issue you face",
      "Empathetic AI with Emotional Intelligence",
    ],
    button: {
      text: "Get Started",
      link: "/",
    },
  },
  {
    name: "SecretAI Pro",
    price: {
      monthly: "$10",
      annual: "$16",
      discount: "10%",
      original: "$24",
    },
    popular: true,
    features: [
      "All the Pro Features of our AI Model",
      "Full-access; no throttling",
      "Spiritual Advisor Prompt",
      "Lifelike Voice Chat",
      "Attain Spiritual Enlightenment",
      "Explore your Faith",
    ],
    button: {
      text: "Get Started",
      link: "#",
    },
  },
  {
    name: "Build-Your-Own AI",
    price: "250",
    popular: false,
    features: [
      "Fully-Customizeable AI",
      "Choose your own prompt, like Mental Health Coach or Spiritual Advisor",
      "Hosting, setup and updates fully taken care of by our team",
      "60-minute Zoom meeting with the developer every month to take care of any updates you need",
      "Empathetic AI with Emotional Intelligence",
      "24/7 Phone Support",
    ],
    button: {
      text: "Contact us",
      link: "/contact",
    },
  },
];
</script>

<template>
  <LandingContainer>
    <LandingSectionhead>
      <template v-slot:title>Pricing</template>
      <template v-slot:desc
        >Simple & Predictable pricing. No Surprises.</template
      >
    </LandingSectionhead>

    <div class="grid md:grid-cols-3 gap-10 mx-auto max-w-screen-lg mt-12">
      <LandingPricing v-for="item of pricing" :plan="item" />
    </div>
  </LandingContainer>
</template>
