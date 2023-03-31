<script>
  let total = 0;
  let console = "";
  let state = null;

  function resolveState() {
    switch (state) {
      case "add":
        total += parseFloat(console);
        console = "0";
        break;
      case "substract":
        total -= parseFloat(console);
        console = "0";
        break;
      case "multiply":
        total *= parseFloat(console);
        console = "0";
        break;
      case "divide":
        total /= parseFloat(console);
        console = "0";
        break;
      default:
        total = parseFloat(console);
        console = "0";
        break;
    }
  }

  function setOperation(operation) {
    resolveState();
    state = operation;
  }

  function setValue(value) {
    if (console.toString() == "0" || state == "equal") {
      console = "";
    }
    if (state == "equal") {
      state = null;
    }
    if (value == "C") {
      total = 0;
      state = null;
      console = "";
      return;
    }
    console = console + value;
  }

  function equal() {
    resolveState();
    console = total;
    state = "equal";
  }
</script>

<div class="calculator">
  <div class="calculator__screen">
    <input type="text" bind:value={console} readonly="true" />
  </div>
  <div class="calculator__buttons">
    <div class="calculator__operations">
      <button
        on:click={() => {
          setOperation("add");
        }}
      >
        +
      </button>
      <button
        on:click={() => {
          setOperation("substract");
        }}
      >
        -
      </button>
      <button
        on:click={() => {
          setOperation("multiply");
        }}
      >
        &times;
      </button>
      <button
        on:click={() => {
          setOperation("divide");
        }}
      >
        &divide;
      </button>
    </div>
    <div class="calculator__numbers">
      <div>
        <button
          on:click={() => {
            setValue(7);
          }}
        >
          7
        </button>
        <button
          on:click={() => {
            setValue(8);
          }}
        >
          8
        </button>
        <button
          on:click={() => {
            setValue(9);
          }}
        >
          9
        </button>
      </div>
      <div>
        <button
          on:click={() => {
            setValue(4);
          }}
        >
          4
        </button>
        <button
          on:click={() => {
            setValue(5);
          }}
        >
          5
        </button>
        <button
          on:click={() => {
            setValue(6);
          }}
        >
          6
        </button>
      </div>
      <div>
        <button
          on:click={() => {
            setValue(1);
          }}
        >
          1
        </button>
        <button
          on:click={() => {
            setValue(2);
          }}
        >
          2
        </button>
        <button
          on:click={() => {
            setValue(3);
          }}
        >
          3
        </button>
      </div>
      <div>
        <button
          on:click={() => {
            setValue(0);
          }}
        >
          0
        </button>
        <button
          on:click={() => {
            setValue(".");
          }}
        >
          .
        </button>
        <button
          on:click={() => {
            setValue("C");
          }}
        >
          C
        </button>
      </div>
    </div>
    <div class="calculator__equal">
      <button on:click={equal}> = </button>
    </div>
  </div>
</div>

<style lang="scss">
  .calculator {
    width: 465px;
    height: 450px;
    border: 1px solid #eee;
    border-radius: 10px;
    box-shadow: 2px 2px 2px #eee;
    padding: 10px;
    margin: 50px auto;

    button {
      outline: none;
      cursor: pointer;
    }

    &__screen {
      input {
        width: 100%;
        padding: 20px;
        outline: none;
        text-align: right;
        font-size: 25px;
      }
    }

    &__buttons {
      display: flex;
      flex-wrap: wrap;
    }

    &__operations {
      display: flex;
      justify-content: space-between;
      width: 100%;

      button {
        width: 30%;
        height: 60px;
        font-size: 2rem;
        background-color: $primary;
        color: $white;
      }
    }

    &__numbers {
      width: 75%;

      div {
        display: flex;
        justify-content: space-between;

        button {
          width: 40%;
          height: 75px;
          background-color: $primary;
          color: $white;
          font-size: 2rem;
        }
      }
    }

    &__equal {
      flex: 1;

      button {
        font-size: 2rem;
        margin-left: 5%;
        width: 95%;
        height: 100%;
        background-color: $secondary;
        color: #eee;
      }
    }
  }
</style>
