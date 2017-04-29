# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
<nav class="navbar navbar-default" role="navigation">
  <div class="container-fluid">
      <!-- Brand and toggle get grouped for better mobile display -->
      <div class="navbar-header">
          <a class="navbar-brand" href="/">Rural Teacher Project </a>
      </div>

      <!-- Collect the nav links, forms, and other content for toggling -->
      <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
          <ul class="nav navbar-nav navbar-right">
              <% if !current_user %>
                <li><%= link_to("注册", new_user_registration_path) %> </li>
                <li><%= link_to("登入", new_user_session_path) %></li>
              <% else %>
                <li class="dropdown">
                  <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                      Hi!, <%= current_user.email %>
                      <b class="caret"></b>
                  </a>
                  <ul class="dropdown-menu">
                      <li> <%= link_to("Admin Panel", admin_jobs_path) %> </li>
                      <li> <%= link_to("登出", destroy_user_session_path, method: :delete) %> </li>
                  </ul>
                </li>
              <% end %>
          </ul>
      </div>
      <!-- /.navbar-collapse -->
  </div>
  <!-- /.container-fluid -->
</nav>
