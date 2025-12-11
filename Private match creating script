fetch("https://na.suprem.io/matchmake/create/private", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Origin": "https://suprem.io",
    "Referer": "https://suprem.io/"
  },
  body: JSON.stringify({
    code: "mycode",        // ← change this to your custom code
    username: "MyUser",
    ability: 1,
    cosmeticHead: "fedora"
  })
})
  .then(res => res.json())
  .then(data => {
    console.log("Created:", data);

    // Redirect current page to the private match
    const code = data.room.code;
    location.href = `https://suprem.io/#${code}`;
  })
  .catch(err => console.error(err));
