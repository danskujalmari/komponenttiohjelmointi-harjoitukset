<div class="wrapper">
  <div class="ekat_kaksi blokwrapperit">
    <div class="using_abstract blokki">
      <img src="abstract.png" alt="abs" width="70px" height="70px" />
      <div class="blokinsisalto">
        <h5>Using Abstract</h5>
        <p>
          Abstract lets you manage, version, and document your designs in one
          place.
        </p>
        <a href="#">Learn more &rarr;</a>
      </div>
    </div>
    <div class="manage_account blokki">
      <img src="account.png" alt="" width="70px" height="70px" />
      <div class="blokinsisalto">
        <h5>Manage your account</h5>
        <p>
          Configure your account settings, such as your email, profile details,
          and password.
        </p>
        <a href="#">Learn more &rarr;</a>
      </div>
    </div>
  </div>

  <div class="tokat_kaksi blokwrapperit">
    <div class="manage_projects blokki">
      <img src="puzzle.png" alt="" width="70px" height="70px" />
      <div class="blokinsisalto">
        <h5>Manage organizations, teams, and projects</h5>
        <p>
          Use Abstract organizations, teams, and projects to organize your
          people and your work.
        </p>
        <a href="#">Learn more &rarr;</a>
      </div>
    </div>
    <div class="manage_billing blokki">
      <img src="money.png" alt="" width="70px" height="70px" />
      <div class="blokinsisalto">
        <h5>Manage billing</h5>
        <p>Change subscriptions and payment details.</p>
        <a href="#">Learn more &rarr;</a>
      </div>
    </div>
  </div>

  <div class="kolmannet_kaksi blokwrapperit">
    <div class="authenticate_abstract blokki">
      <img src="key.png" alt="" width="70px" height="70px" />
      <div class="blokinsisalto">
        <h5>Authenticate to Abstract</h5>
        <p>Set up and configure SSO, SCIM, and Just-in-Time provisioning.</p>
        <a href="#">Learn more &rarr;</a>
      </div>
    </div>
    <div class="support blokki">
      <img src="message.png" alt="" width="70px" height="70px" />
      <div class="blokinsisalto">
        <h5>Abstract support</h5>
        <p>Get in touch with a human.</p>
        <a href="#">Learn more &rarr;</a>
      </div>
    </div>
  </div>
</div>

<style>
  .wrapper {
    display: flex;
    flex-direction: column;
    gap: 6vh;
    padding: 10vh 0;
  }

  .blokwrapperit {
    display: flex;
    justify-content: center;
    gap: 10vw;
    flex-wrap: wrap;
  }

  .blokki {
    max-width: 30%;
    min-width: 30%;
    flex: 1;
    padding: 10px;
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
    gap: 30px;
  }

  h5 {
    text-transform: capitalize;
    font-size: 1.4rem;
  }

  a:any-link {
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  @media (max-width: 375px) {
    .wrapper {
      padding: 5vh 0;
      gap: 1vh;
    }

    .blokwrapperit {
      width: 100%;
      display: block;
      text-align: justify;
      gap: 5vh;
    }

    .blokki {
      max-width: 90%;
      min-width: 90%;
      padding: 15px;
    }

    h5 {
      font-size: 1.2rem;
    }

    p {
      font-size: 1rem;
      line-height: 1.5;
    }

    img {
      width: 50px;
      height: 50px;
    }
  }
</style>
