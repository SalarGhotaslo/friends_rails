<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <%= link_to "Acebook",  root_path, class:"navbar-brand" %>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
         <li class="nav-item">
          <%= link_to "Posts", posts_path, class:"nav-link"%>
        </li>
        <li class="nav-item">
          <%= link_to "Sign up", new_user_registration_path, class:"nav-link"%>
        </li>
         <li class="nav-item">
          <%= link_to "Sign in", new_user_session_path, class:"nav-link"%>
        </li>
         <li class="nav-item">
          <%= link_to "Sign out", destroy_user_session_path, class:"nav-link", method: :delete %>
        </li>

      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>

  </div>
</nav>