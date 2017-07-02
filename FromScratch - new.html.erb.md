<pre>
<p id="notice"><%= notice %></p>

<h1>Show Report</h1>
<p>
  <strong>Name:</strong>
  <%= @report.name %>
</p>

<p>
  <strong>Manager:</strong>
  <%= @report.manager %>
</p>

<p>
  <strong>From:</strong>
  <%= @report.from_date.strftime("%m") %>
</p>

<p>
  <strong>Date:</strong>
  <%= @report.date.strftime("%m") %>
</p>

<p>
  <strong>Notes:</strong>
  <%= @report.notes %>
</p>


<%= link_to 'Edit', edit_report_path(@report), class: 'btn btn-info btn-md' %><br>
<%= link_to 'Back', reports_path, class: 'btn btn-info btn-md' %>
</pre>
