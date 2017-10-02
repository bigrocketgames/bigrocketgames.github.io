---
layout: post
title:  "Dynamically Displaying Your Static Content in React"
date:   2017-10-02 01:13:31 +0000
---


When I started working on the client side of my final project, I knew I was going to want at least a couple of my navigation links to vary based on whether someone was logged in and if that user was an admin or not.  Doing this in a Rails application is fairly straight forward, just by writing the ruby code in your .erb file like this:

```
<% if current_user %>
  <li><%= link_to "Sign Out", destroy_user_session_path, method: "delete" %></li>
<% else %>
  <li><%= link_to "Sign In", new_user_session_path %></li>
<% end %>
```

It turns out that it is simple in React as well, but not quite as simple as that.  You can't just put it into your return of your component like this:

```
if (this.props.user.id) {
      pageHeader = <div>
          <h3 className="text-center">Your Favorite Teams</h3>
          <p className="text-center">Click a team name to see their schedule</p><hr/>
          <UserTeams />
          </div>
    } else {
      pageHeader = <div><h1 className="text-center">Team Schedules</h1><p className="text-center"><a href="/login">Login</a> or <a href="/signup">Signup</a> to find out when your favorite team plays</p><hr /></div>
    }
```

However, there is a simple solution to getting this code to work.  You could possibly turn this into a stateless component and pass it the user prop, but part of my problem was that I needed to know if there was a user, and if you try to pass a prop that doesn't exist, the application gets cranky.  So the simple solution I found is just to move this code to outside the return but still inside the render function and then call the variable inside of my return function.  This is how my entire render function ended up looking.

```
  render() {
    let pageHeader = null;
    if (this.props.user.id) {
      pageHeader = <div>
          <h3 className="text-center">Your Favorite Teams</h3>
          <p className="text-center">Click a team name to see their schedule</p><hr/>
          <UserTeams />
          </div>
    } else {
      pageHeader = <div><h1 className="text-center">Team Schedules</h1><p className="text-center"><a href="/login">Login</a> or <a href="/signup">Signup</a> to find out when your favorite team plays</p><hr /></div>
    }

    return (
      <div className="container">
        {pageHeader}
      </div>
    )
  }
}
```

This worked wonderfully in my application and for this particular instance where it rendered the welcome text on my application's home page based on whether or not a user is logged into the application.
