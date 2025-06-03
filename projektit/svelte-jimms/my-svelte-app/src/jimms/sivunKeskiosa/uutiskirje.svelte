<div class="uutiskirje">
  <div class="teksti">
    <h2 class="otsikko">Tilaa uutiskirje</h2>
    <div>
      Tilaa Jimm'sin uutiskirje ja saat ensimmäisten joukossa tietoa
      tarjouksista, tapahtumista ja uusista tuotteista.
    </div>
  </div>
  <div class="nappi">
    <a class="uutiskirje_nappi" href="#">tilaa uutiskirje</a>
  </div>
</div>

<style>
  .uutiskirje {
    display: flex;
    flex-direction: column;
    gap: 20px;
    max-width: 20vw;
    color: var(--väri-teksti);
  }

  .teksti {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .teksti div {
    line-height: 1.5;
    white-space: normal;
    word-wrap: break-word;
  }

  .otsikko {
    font-size: 18px;
    text-transform: uppercase;
    color: #fff;
  }

  .nappi {
    width: 100%;
    display: flex;
    justify-content: flex-start;
  }

  .uutiskirje_nappi {
    padding: 8px 8px;
    border-radius: 3px;
    background-color: var(--väri-linkki-tausta-hover);
  }

  a:any-link {
    color: var(--väri-otsikot);
    text-decoration: none;
    text-transform: uppercase;
    font-weight: bold;
  }

  @media screen and (max-width: 680px) {
    .uutiskirje {
      width: 100%;
      max-width: none;
      gap: 15px;
    }

    .teksti {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .teksti div {
      line-height: 1.5;
      white-space: normal;
      word-wrap: break-word;
      font-size: 14px;
    }

    .nappi {
      width: 100%;
      display: flex;
      justify-content: flex-start;
    }

    .uutiskirje_nappi {
      display: inline-block;
      padding: 10px 30px;
      border-radius: 4px;
      background-color: var(--väri-linkki-tausta-hover);
      text-align: center;
      transition: background-color 0.2s ease;
      min-width: 160px;
    }

    .uutiskirje_nappi:hover {
      background-color: #ff6b00;
    }

    a:any-link {
      color: #fff;
      text-decoration: none;
      text-transform: uppercase;
      font-weight: 600;
      font-size: 14px;
    }
  }

  @media screen and (max-width: 390px) {
    .uutiskirje {
      gap: 12px;
    }

    .teksti div {
      font-size: 14px;
    }

    .uutiskirje_nappi {
      min-width: 140px;
      padding: 8px 20px;
    }
  }
</style>
