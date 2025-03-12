<div class="alapalkki">
  <div class="lista_yksi lista">
    <h3>Abstract</h3>
    <ul>
      <li><a href="#">Start Trial</a></li>
      <li><a href="#">Pricing</a></li>
      <li><a href="#">Download</a></li>
    </ul>
  </div>

  <div class="lista_kaksi lista">
    <h3>Resources</h3>
    <ul>
      <li><a href="#">Blog</a></li>
      <li><a href="#">Help Center</a></li>
      <li><a href="#">Release Notes</a></li>
      <li><a href="#">Status</a></li>
    </ul>
  </div>

  <div class="lista_kolme lista">
    <h3>Community</h3>
    <ul>
      <li><a href="#">Twitter</a></li>
      <li><a href="#">LinkedIn</a></li>
      <li><a href="#">Facebook</a></li>
      <li><a href="#">Dribbble</a></li>
      <li><a href="#">Podcast</a></li>
    </ul>
  </div>

  <div class="listat_yhdessä">
    <div class="lista_nelja lista">
      <h3>Company</h3>
      <ul>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Careers</a></li>
        <li><a href="#">Legal</a></li>
      </ul>
    </div>
    <div class="lista_viisi lista">
      <h3>Contact Us</h3>
      <ul>
        <li><a href="#">info@abstract.com</a></li>
      </ul>
    </div>
  </div>

  <div class="copyright">
    &copy; Copyright 2025 Abstract Studio Design, Inc. All rights reserved
  </div>
</div>

<style>
  .listat_yhdessä {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .lista {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }
  h3 {
    color: var(--väri-eka);
    text-transform: capitalize;
    font-size: 1.5rem;
  }
  a:any-link {
    color: var(--väri-eka);
    text-decoration: none;
  }

  a:hover {
    color: var(--väri-eka);
    text-decoration: underline;
  }
  .alapalkki {
    display: flex;
    flex-direction: row;
    padding-left: 15vw;
    gap: 10vw;
    padding-top: 4vh;
    padding-bottom: 4vh;
    height: auto;
    background-color: var(--väri-toka);
  }

  .lista_viisi h3 {
    font-size: 1rem;
  }
  .lista_viisi {
    display: flex;
    flex-direction: column;
    gap: 3px;
  }

  .copyright {
    color: var(--väri-eka);
    max-width: 8vw;
    font-weight: 600;
    font-size: 1.1rem;
  }

  @media (max-width: 375px) {
    .alapalkki {
      width: 126.2vw;
      flex-direction: column;
      padding-left: 5vw;
      padding-top: 2vh;
      padding-bottom: 8vh;
      gap: 20px;
    }

    .lista_yksi,
    .lista_kaksi,
    .lista_kolme,
    .lista_nelja,
    .lista_viisi {
      max-width: 40vw;
      min-width: 10px;
    }

    h3 {
      font-size: 1rem;
      text-align: left;
    }

    ul li a {
      font-size: 0.8rem;
    }

    .listat_yhdessä {
      flex-direction: column;
      gap: 15px;
    }

    .copyright {
      font-size: 0.7rem;
      margin-top: 20px;
      text-align: center;
    }
  }

  @media (max-width: 1200px) {
    .lista_yksi,
    .lista_kaksi,
    .lista_kolme,
    .lista_nelja,
    .lista_viisi {
      max-width: 40vw;
      min-width: 10px;
    }

    .alapalkki {
      flex-direction: row;
      padding-left: 5vw;
      padding-right: 5vw;
      padding-top: 2vh;
      padding-bottom: 8vh;
      justify-content: space-between;
    }
  }

  @media (max-width: 768px) {
    .lista_yksi,
    .lista_kaksi,
    .lista_kolme,
    .lista_nelja,
    .lista_viisi {
      max-width: 40vw;
      min-width: 10px;
    }

    .alapalkki {
      flex-direction: row;
      padding-left: 5vw;
      padding-right: 5vw;
      padding-top: 2vh;
      padding-bottom: 8vh;
      justify-content: space-between;
    }
  }
</style>
