<div class="musta_ylapalkki">
  <div class="linkkijalogo">
    <a class="abstract link" href="#"
      ><img src="logo-text.png" alt="da" width="140px" /></a
    >
    <a class="helpcenter link" href="#">Help Center</a>
  </div>

  <div class="napit">
    <a class="btn1 btn" href="#">Submit a request</a>
    <a class="btn2 btn" href="#">Sign in</a>
  </div>
</div>

<style>
  .musta_ylapalkki {
    background-color: var(--väri-toka);
    height: 88px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 13%;
    box-sizing: border-box;
  }

  .linkkijalogo {
    display: flex;
  }

  a {
    text-decoration: none;
    color: var(--väri-eka);
    padding: 7px 15px;
    font-weight: 600;
    font-size: 24px;
  }

  .abstract {
    border-right: 2px solid #fff;
  }

  .helpcenter:hover {
    text-decoration: underline;
  }

  .napit {
    display: flex;
    gap: 15px;
  }

  .btn {
    padding: 7px 20px;
    border-radius: 8px;
    color: white;
    text-decoration: none;
    font-weight: 500;
  }

  .btn1 {
    background-color: rgb(34, 32, 32);
    border: 1px solid var(--väri-eka);
    color: white;
    text-decoration: none;
  }

  .btn2 {
    background-color: var(--väri-kolmas);
    color: white;
    text-decoration: none;
  }

  @media (max-width: 375px) {
    .musta_ylapalkki {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      padding: 0 8%;
    }

    .linkkijalogo {
      display: flex;
      flex-direction: row;
      align-items: center;
    }

    .link {
      font-size: 0.9rem;
      font-weight: normal;
    }

    .napit .btn {
      padding: 8px 6px;
      font-size: 0.6rem;
    }

    .abstract img {
      width: 80px;
    }
  }

  @media (max-width: 768px) {
    .musta_ylapalkki {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      padding: 0 8%;
    }

    .link {
      font-weight: normal;
    }

    .btn {
      padding: 10px 10px;
      font-size: 1rem;
    }

    .abstract img {
      width: 120px;
    }
  }

  @media (max-width: 390px) {
    .musta_ylapalkki {
      height: auto;
      flex-direction: column;
      align-items: center;
      padding: 20px 15px;
      gap: 20px;
    }

    .linkkijalogo {
      width: auto;
      display: flex;
      align-items: center;
      gap: 15px;
    }

    .abstract,
    .helpcenter {
      padding-top: 0;
      padding-bottom: 0;
    }

    .abstract {
      border-right: none;
      padding-right: 0;
      padding-left: 0;
      line-height: 1;
    }

    .abstract img {
      width: 100px;
      vertical-align: middle;
    }

    .helpcenter {
      font-size: 1rem;
      padding-left: 0;
    }

    .napit {
      display: flex;
      width: 100%;
      justify-content: space-around;
      gap: 10px;
    }

    .btn {
      padding: 10px 15px;
      font-size: 0.9rem;
      flex-grow: 1;
      text-align: center;
    }
  }
</style>
