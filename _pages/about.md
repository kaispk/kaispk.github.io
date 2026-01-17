---
permalink: /
title: ""
layout: home
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

# Kai Spiekermann

<div class="portrait-section">
<img src="/images/portrait.jpg" alt="Kai Spiekermann">
<div class="caption">Dr Kai Spiekermann, LSE</div>
</div>

I'm a Professor of Political Philosophy in the Department of
Government at the London School of Economics. I work in democratic
theory, the philosophy of the social sciences and topics relating to
politics, philosophy and economics (PPE) more generally. 

Among my research interests are group decisions, social epistemology
(and especially epistemic justifications of democracy), the ethics of
environmental change, and the methodology of political theory and
political science. More information is [here](/research).

<div style="clear: both;"></div>

<div class="contact-section">
<h3>Contact Information</h3>
<p><strong>Email:</strong> <a href="mailto:k.spiekermann@lse.ac.uk">k.spiekermann@lse.ac.uk</a></p>
<p><strong>Office hours:</strong> Please book on the LSE Student Hub app</p>
<p><strong>Affiliation:</strong> Department of Government, London School of Economics</p>
</div>

## Recent News

<div id="bluesky-feed"></div>

<script>
async function loadBlueskyPosts() {
  const handle = 'kaispiekermann.bsky.social'; // Your Bluesky handle
  const limit = 2; // Number of posts to show
  
  try {
    // Resolve handle to DID
    const didRes = await fetch(`https://bsky.social/xrpc/com.atproto.identity.resolveHandle?handle=${handle}`);
    const { did } = await didRes.json();
    
    // Fetch posts
    const postsRes = await fetch(`https://bsky.social/xrpc/app.bsky.feed.getAuthorFeed?actor=${did}&limit=${limit}`);
    const data = await postsRes.json();
    
    const feed = document.getElementById('bluesky-feed');
    feed.innerHTML = data.feed.map(item => {
      const post = item.post;
      const date = new Date(post.indexedAt).toLocaleDateString();
      return `
        <div class="bluesky-post">
          <p>${post.record.text}</p>
          <small><a href="https://bsky.app/profile/${handle}/post/${post.uri.split('/').pop()}" target="_blank">${date}</a></small>
        </div>
      `;
    }).join('');
  } catch (error) {
    console.error('Error loading Bluesky posts:', error);
  }
}

loadBlueskyPosts();
</script>


<div class="news-item">
<strong>PhD Supervision</strong>
If you are considering applying for a PhD and are thinking of me as your supervisor, please read <a href="https://kaispk.github.io/phd-supervision/">this guidance</a> first. The deadline for the 2026 entry is January 14.
</div>

<div class="news-item">
<strong>BIAPT 2026</strong>
I was at the BIAPT Conference in Edinburgh in January 2026, talking about social norms and climate change. 
</div>

<div class="news-item">
<strong>2024-06-30 - NSF RCN Conference</strong>
Research associate at the NSF RCN grant for "Augmenting Intelligence through Collective Learning", which was now sadly revoked. The final conference was in Vienna at the end of June.
</div>


<div class="news-item">
<strong>2024 - Open Society Foundation Grant</strong>
LSE won a <a href="https://www.lse.ac.uk/News/Latest-news-from-LSE/2024/a-January-2024/Envisioning-an-economy-that-works-for-all">transformational grant from the Open Society Foundation on Cohesive Capitalism</a>. I am working with <a href="https://personal.lse.ac.uk/voorhoev/">Alex Voorhoeve</a> and <a href="https://www.lse.ac.uk/cpnss/people/richard-bradley">Richard Bradley</a> and Suzanne Bloks <a href="https://suzannebloks.com/">Suzanne Bloks</a> on two projects, one on <a href="https://www.lse.ac.uk/cpnss/research/cohesion-and-deliberative-decision-making">cohesion and deliberation</a>, the other on protection against severe uncertainty.
</div>

<div class="news-item">
<strong>2024 - Handbook of Rationality Open Access</strong>
The <a href="https://direct.mit.edu/books/oa-edited-volume/5525/The-Handbook-of-Rationality">Handbook of Rationality</a> is now open access!
</div>



