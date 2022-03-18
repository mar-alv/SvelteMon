<script lang="ts">
  type colorType = "gray" | "yellow" | "lightBlue";
  type positionType = "bottom" | "center" | "right";

  export let position: positionType = "bottom";
</script>

<div class={`modal modal--${position}`}>
  <div class="modal__content">
    <slot />
  </div>
</div>

<style lang="scss">
  .modal {
    width: 100%;
    height: 100%;
    display: flex;
    position: absolute;

    &.zi {
      z-index: 99;
      
    }

    &__content {
      border: 5px solid red;
    }

    &--bottom {
      align-items: flex-end;

      .modal__content {
        width: 100%;
      }
    }

    &--center {
      align-items: center;
      justify-content: center;
    }

    &--right {
      justify-content: flex-end;
    }
  }
</style>
