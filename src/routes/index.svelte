<script>
  import COVIDAlertLevel from "../components/COVIDAlertLevel.svelte";
</script>

<style>
  .page {
    min-height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  h1 {
    font-size: 3.5vw;
    text-align: center;
  }
  .r-value {
    font-size: 500%;
  }
  h1 small {
    opacity: 0.5;
    font-size: 60%;
  }

  h2 {
    font-size: 3.5vw;
  }

  article {
    padding: 5%;
  }

  article .content {
    font-size: 1.5vw;
    padding-left: 10px;
    border-left: 6px solid black;
    max-width: 600px;
  }

  footer {
    text-align: center;
    padding: 2vw;
    font-size: 2vw;
    color: #999999;
  }
  footer a {
    transition: 0.3s;
    color: #999999;
  }
  footer a:hover {
    color: #000;
  }

  .mean-for-me {
    text-align: center;
    font-size: 1.5vw;
    color: #000;
    text-decoration: none;
    opacity: 0.5;
    transition: 0.3s;
    margin-bottom: 0;
  }
  .mean-for-me img {
    height: 3vw;
  }
  .mean-for-me:hover {
    opacity: 1;
  }

  .email-input {
    text-align: center;
  }
  .email-input label h4 {
    text-align: center;
    font-size: 1.5vw;
    color: #000;
    text-decoration: none;
    opacity: 0.5;
  }

  .input-cont {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  .email-input input {
    font-size: 2vw;
    padding: 0.5vw;
    background: none;
    border: 3px solid #ddd;
    border-right: 0;
  }
  .email-input button {
    border: 0;
    background: #ea5043;
    border-bottom: 3px solid rgb(155, 52, 43);
    color: white;
    cursor: pointer;
    width: 4vw;
  }
  .email-input button img {
    height: 70%;
  }
  .probably {
    color: #999;
    font-size: 80%;
  }

  ul {
    padding-left: 2vw;
  }
  @media (max-width: 1000px) {
    ul {
      padding-left: 4vw;
    }
    .email-input button {
      width: 8vw;
    }
    .email-input input {
      font-size: 4vw;
      padding: 1vw;
    }
    h1,
    h2 {
      font-size: 7vw;
    }
    article .content,
    .mean-for-me,
    .email-input label h4 {
      font-size: 3vw;
    }
    footer {
      font-size: 4vw;
      padding: 4vw;
    }
    .mean-for-me img {
      height: 6vw;
    }
  }
</style>

<svelte:head>
  <!-- Primary Meta Tags -->
  <title>The R value in the UK is...</title>
  <meta name="title" content="The R value in the UK is..." />
  <meta
    name="description"
    content="What is R? When will lockdown end? Get frequent updates about the
    COVID pandemic" />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://whatisr.uk" />
  <meta property="og:title" content="The R value in the UK is..." />
  <meta
    property="og:description"
    content="What is R? When will lockdown end? Get frequent updates about the
    COVID pandemic" />
  <meta property="og:image" content="/banner.png" />

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content="https://whatisr.uk" />
  <meta property="twitter:title" content="The R value in the UK is..." />
  <meta
    property="twitter:description"
    content="What is R? When will lockdown end? Get frequent updates about the
    COVID pandemic" />
  <meta property="twitter:image" content="/banner.png" />
</svelte:head>
<div class="page" id="home">
  <div />
  <h1>
    <strong>R</strong>
    in the UK is at most
    <br />
    <strong class="r-value">0.9</strong>
    <br />
    <small>
      <a href="#data" class="probably">(probably)</a>
    </small>
  </h1>
  <div>
    <form
      class="email-input"
      action="https://whatisr.us18.list-manage.com/subscribe/post?u=9984954bc9514001bfc4cb7a0&amp;id=ab153d836a"
      method="post">
      <div style="position: absolute; left: -5000px;" aria-hidden="true">
        <input
          type="text"
          name="b_9984954bc9514001bfc4cb7a0_ab153d836a"
          tabindex="-1"
          value="" />
      </div>
      <label for="email">
        <h4>Email me updates</h4>
      </label>
      <div class="input-cont">
        <input
          type="email"
          placeholder="rich@teabiscuits.uk"
          id="email"
          name="EMAIL"
          required />
        <button>
          <img src="save-icon.svg" alt="Save Icon" />
        </button>
      </div>
    </form>
    <br />
    <a href="#alert-level" class="mean-for-me">
      <h4>
        What does this mean for me?
        <br />
        <img src="down-arrow.svg" alt="Down Arrow" />
      </h4>
    </a>
  </div>
</div>

<article id="alert-level">
  <h2>
    The UK
    <strong>
      <a href="https://www.bbc.co.uk/news/uk-52602635">COVID Alert Level</a>
    </strong>
    is
  </h2>
  <COVIDAlertLevel level={4} />
</article>

<article id="help">
  <h2>What can I do to help?</h2>
  <div class="content">
    <ul>
      <li>Follow the government guidelines</li>
      <li>Enoucrage others to follow the guidelines</li>
      <li>Help vulnerable people in your community</li>
    </ul>
  </div>
</article>

<article id="lockdown">
  <h2>When will lockdown end?</h2>
  <div class="content">
    <ul>
      <li>
        If criteria are met, at the earliest June 1st, phased reopening of shops
        and some primary school students.
      </li>
      <li>
        If criteria are met, at the earliest July 1st, reopen some restaurants
        and public places.
      </li>
    </ul>
  </div>
</article>

<article id="data">
  <h2>
    How do we know "
    <b>R</b>
    "?
  </h2>
  <div class="content">
    <p>
      We don't know for sure, but we can make educated guesses based on various
      data.
      <br />
      We list our sources
      <a
        href="https://docs.google.com/spreadsheets/d/1A3joelHjrIyPzNwWEzraprj3aDfc7dAe9JUakeA98Fo/edit#gid=0">
        here
      </a>
      <br />
    </p>
  </div>
</article>

<footer>
  <span>
    <a href="https://twitter.com/nathanpmyoung" target="_blank">
      @nathanpmyoung
    </a>
    |
    <a href="https://twitter.com/isnit0" target="_blank">@isnit0</a>
    |
    <a href="https://twitter.com/nwspk" target="_blank">@nwspk</a>
  </span>
</footer>
