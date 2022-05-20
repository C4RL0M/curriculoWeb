<template>
  <Menu>
    <div class="Content">
      <Title title="name" subTitle="profession" />
      <Card>
        <p class="Content-text">
          {{ $t("age") }}
          <br />
          {{ $t("contact") }}: carlosmiguelnowatzki@outlook.com
          <br />
          {{ $t("location") }}: São Leopoldo - Rio Grande do Sul
          <br />
          {{ $t("myself") }}
          <br />
          {{ $t("goOut") }}
        </p>
      </Card>
      <div class="Content-footer">
        <SocialNetwork
          icon="linkedin"
          link="https://www.linkedin.com/in/carlos-nowatzki-8b75b51b5/"
        />
        <SocialNetwork
          icon="github"
          link="https://github.com/C4RL0M"
        />
        <SocialNetwork
          icon="twitter"
          link="https://twitter.com/carlos_m1guel"
        />
      </div>
    </div>
  </Menu>
</template>

<script>
import Card from "~/components/Card";
import Title from "~/components/Title";
import SocialNetwork from "~/components/SocialNetwork";

export default {
  name: "Home",
  metaInfo: {
    title: "Sobre",
  },
  components: {
    Card,
    Title,
    SocialNetwork,
  },
};
</script>

<style lang="scss" scoped>
.Content {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
  flex-direction: column;
  padding: 0 $paddingLeftRightScreen $paddingLarge;

  @media (max-width: $largeViewports) {
    padding: 0 100px;
  }

  @media (max-width: $smallViewports) {
    padding: 0 40px;
  }

  &-text {
    color: $lynch;
    line-height: 2.4;

    @media (max-width: $largeViewports) {
      font-size: 0.9rem;
    }
  }

  &-footer {
    width: 100%;
    display: flex;
    margin-top: 30px;

    > div {
      &:not(:last-child) {
        margin-right: 5px;
      }
    }
  }
}
</style>
