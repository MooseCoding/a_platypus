<script>
    import Contact from '$lib/pages/contact_page.json';

    let name = Contact.Contact.Name;
    let username = Contact.Contact.Username;
    let title = Contact.Contact.Title;
    let email = Contact.Contact.Email;
    let phone = Contact.Contact.Phone;
    let linkedin = Contact.Contact.LinkedIn;
    let youtube = Contact.Contact.YouTube;
    let twitter = Contact.Contact.Twitter;
    let insta = Contact.Contact.Instagram;
    let website = Contact.Contact.Website;
    let linktree = Contact.Contact.LinkTree; 
  </script>
  
  <div class="p-6 rounded-lg shadow-lg max-w-xs mx-auto text-center space-y-4" style="background-color: {Contact.Contact.BackgroundColor}">
    <h2 class="text-2xl font-bold" style="color: {Contact.Contact.TextColor}">{name}</h2>
    <h3 class="text-xl font-semibold" style="color: {Contact.Contact.TextColor}">{username}</h3>
    <p style="color: {Contact.Contact.TextColor}">{title}</p>
  
    <div class="flex flex-col items-center space-y-2">
      <a href={`mailto:${email}`} class="hover:text-blue-500" style="color: {Contact.Contact.EmailColor}">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-5 h-5 inline mr-2" viewBox="0 0 24 24">
          <path d="M12 13.065l-11-7.065h22l-11 7.065zm11-8.065h-22v16h22v-16z"/>
        </svg>
        {email}
      </a>
  
      <a href={`tel:${phone}`} class="hover:text-green-500" style="color: {Contact.Contact.PhoneColor}">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-5 h-5 inline mr-2" viewBox="0 0 24 24">
          <path d="M17.707 16.293l-2.121 2.121c-.293.293-.678.439-1.061.439s-.768-.146-1.061-.439l-1.414-1.414c-1.171-.195-2.343-.488-3.486-1.03s-2.091-1.397-3.071-2.377-1.751-2.006-2.377-3.071c-.543-1.144-.835-2.315-1.03-3.486l-1.414-1.414c-.293-.293-.439-.678-.439-1.061s.146-.768.439-1.061l2.121-2.121c.586-.586 1.535-.586 2.121 0l2.121 2.121c.586.586.586 1.535 0 2.121l-1.414 1.414c.151.806.383 1.603.707 2.378s.812 1.518 1.374 2.08 1.314 1.046 2.08 1.374c.775.324 1.572.556 2.378.707l1.414-1.414c.586-.586 1.535-.586 2.121 0l2.121 2.121c.586.586.586 1.535 0 2.121z"/>
        </svg>
        {phone}
      </a>
    </div>

    <div class="flex justify-center space-x-4">
      {#if insta}
        <a href={insta} target="_blank" rel="noopener noreferrer" class="text-red-600 hover:text-red-800">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-6 h-6" viewBox="0 0 24 24">
            <path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.9 3.9 0 0 0-1.417.923A3.9 3.9 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.9 3.9 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.9 3.9 0 0 0-.923-1.417A3.9 3.9 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599s.453.546.598.92c.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.5 2.5 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.5 2.5 0 0 1-.92-.598 2.5 2.5 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233s.008-2.388.046-3.231c.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92s.546-.453.92-.598c.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92m-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217m0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334"/>
          </svg>
        </a>
      {/if}
      
      {#if linkedin}
        <a href={linkedin} target="_blank" rel="noopener noreferrer" class="text-blue-700 hover:text-blue-900">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-6 h-6" viewBox="0 0 24 24">
            <path d="M19 3h-14c-1.104 0-2 .896-2 2v14c0 1.104.896 2 2 2h14c1.104 0 2-.896 2-2v-14c0-1.104-.896-2-2-2zm-11 14h-2v-8h2v8zm-1-9c-.553 0-1-.447-1-1s.447-1 1-1 1 .447 1 1-.447 1-1 1zm10 9h-2v-4c0-1.105-.895-2-2-2s-2 .895-2 2v4h-2v-8h2v1.025c.586-.769 1.445-1.025 2.5-1.025 2.207 0 3.5 1.343 3.5 3v5z"/>
          </svg>
        </a>
      {/if}

    {#if twitter}
      <a href={youtube} target="_blank" rel="noopener noreferrer" class="text-red-600 hover:text-red-800">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-6 h-6" viewBox="0 0 24 24">
          <path d="M12.6.75h2.454l-5.36 6.142L16 15.25h-4.937l-3.867-5.07-4.425 5.07H.316l5.733-6.57L0 .75h5.063l3.495 4.633L12.601.75Zm-.86 13.028h1.36L4.323 2.145H2.865z"/>
        </svg>
      </a>
    {/if}
  
    {#if youtube}
      <a href={youtube} target="_blank" rel="noopener noreferrer" class="text-red-600 hover:text-red-800">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-6 h-6" viewBox="0 0 24 24">
          <path d="M23.498 6.186c-.336-1.25-1.317-2.207-2.538-2.436-2.054-.338-10.254-.338-10.254-.338s-8.196 0-10.254.338c-1.221.229-2.202 1.186-2.538 2.436C.002 7.472 0 12 0 12s.002 4.528.707 5.814c.336 1.25 1.317 2.207 2.538 2.436 2.054.338 10.254.338 10.254.338s8.2 0 10.254-.338c1.221-.229 2.202-1.186 2.538-2.436C24 16.528 24 12 24 12s-.002-4.528-.502-5.814zm-14.831 7.166v-6.386l6.182 3.193-6.182 3.193z"/>
        </svg>
      </a>
    {/if}
  
      {#if website}
        <a href={website} target="_blank" rel="noopener noreferrer" class="text-gray-700 hover:text-gray-900">
          <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-6 h-6" viewBox="0 0 24 24">
            <path d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm0 22c-5.514 0-10-4.486-10-10s4.486-10 10-10 10 4.486 10 10-4.486 10-10 10zm0-18c-4.411 0-8 3.589-8 8 0 4.411 3.589 8 8 8s8-3.589 8-8c0-4.411-3.589-8-8-8zm1 13h-2v-6h2v6zm0-8h-2v-2h2v2z"/>
          </svg>
        </a>
      {/if}
    </div>
  </div>