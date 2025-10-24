function loadVideo() {
    const url = document.getElementById("videoURL").value.trim();
    if (!url) return alert("Paste a YouTube URL!");

    let videoId;
    // Handle normal URL
    if (url.includes("v=")) {
        videoId = url.split("v=")[1].split("&")[0];
    }
    // Handle short URL youtu.be
    else if (url.includes("youtu.be/")) {
        videoId = url.split("youtu.be/")[1].split("?")[0];
    } else {
        return alert("Invalid YouTube URL!");
    }

    const embedUrl = `https://www.youtube.com/embed/${videoId}?rel=0&modestbranding=1`;

    document.getElementById("player").innerHTML = `
        <iframe src="${embedUrl}" frameborder="0" allowfullscreen></iframe>
    `;
}
