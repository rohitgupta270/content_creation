# Content Creation Workspace

**What is this?** A tool that helps you create professional LinkedIn posts automatically with AI. Instead of writing posts from scratch, Claude (an AI assistant) helps you generate ready-to-publish content with pictures, in your unique voice.

**Who should use this?** Product managers, entrepreneurs, thought leaders, and content creators who want to build their personal brand on LinkedIn without spending hours writing.

---

## How It Works (Simple Explanation)

Think of this like having a smart writing assistant:

1. **You tell Claude about yourself** — your experience, your voice, what you care about
2. **Claude generates LinkedIn posts** — based on what's trending, proven content formats, and your expertise
3. **Posts include pictures** — either AI-generated infographics or your personal photos
4. **Everything is saved in folders** — organized and ready to publish whenever you want

The whole process runs automatically once you set it up.

---

## Getting Started (Step by Step)

### Step 1: Clone This Project

```bash
git clone https://github.com/YOUR-USERNAME/content_creation.git
cd content_creation
```

### Step 2: Get API Keys (Required)

You need API keys from two services to generate images. Don't worry — they're free or cheap.

**Sign up for these:**
1. **Apify** (for scraping social media data)
   - Go to [apify.com](https://apify.com)
   - Sign up (free)
   - Get your API key from Settings
   
2. **Kie.ai** (for AI image generation)
   - Go to [kie.ai](https://kie.ai)
   - Sign up (free tier available)
   - Get your API key

### Step 3: Add Your API Keys

Create a file called `.env` in the project folder and add your keys:

```
APIFY_API_KEY=your_apify_key_here
KIE_AI_API_KEY=your_kie_ai_key_here
```

**⚠️ Important:** Never share this `.env` file. It contains secret keys.

### Step 4: Install Python Libraries

You need Python installed. Then run:

```bash
pip install Pillow requests
```

### Step 5: Tell Claude About You

This is the important part. Edit these files to describe yourself:

**`context/profile.md`** — Who are you?
- Your name, LinkedIn URL, experience level
- What industries you've worked in
- What you're known for

**`context/strategy.md`** — What do you want to achieve?
- What topics do you want to talk about? (e.g., AI, payments, leadership)
- Who is your audience? (e.g., product managers, founders)
- What's your goal? (build audience, get consulting inquiries, get hired, etc.)

**`context/business.md`** — What do you do?
- Describe your business/role in simple terms
- What problems do you solve?

### Step 6: Add Your Photos

Create a folder `context/images/` and add:
- 5-10 photos of yourself (casual, at desk, outdoors, professional photos)
- Name them clearly: `at-desk.jpg`, `casual-smile.jpg`, etc.

Claude will use these in your posts.

### Step 7: Create Your First Posts

Open Claude Code and run:

```
/prime
```

This tells Claude to read everything about you. Then run:

```
/create-10-posts
```

Claude will generate **10 LinkedIn posts** with:
- Your unique voice
- Real company examples and data
- Professional images
- Ready to copy and paste into LinkedIn

---

## What You Get

After running `/create-10-posts`, you'll find:

- **10 posts** in the `posts/` folder
- **Each post has:**
  - A text file with the post copy
  - An image (photo or AI infographic)
  - A folder with everything organized
- **Dashboard** at `outputs/dashboard.html` — see all your posts in one place

---

## How to Use Your Posts

1. Go to `posts/` folder
2. Pick any post you like
3. Read the text in `post.md`
4. Copy the text to LinkedIn
5. Upload the image
6. Click "Post"

That's it! No hours of writing. Just publish.

---

## Folder Guide (What Everything Does)

| Folder | What It's For |
|--------|---------------|
| `context/` | **All about YOU** — your profile, strategy, photos |
| `posts/` | **Finished posts** — ready to publish on LinkedIn |
| `outputs/` | **Dashboard** — see all your posts in one place |
| `reference/` | **Style guides** — examples of good writing, colors, layouts |
| `scripts/` | **Behind the scenes** — tools that build your dashboard |
| `plans/` | **Planning** — save your content plans here |

---

## Customizing for Your Brand

### Change Your Colors

If you don't like the green and cream colors:

1. Open `scripts/generate-carousel.py`
2. Find the color codes (they look like `#C8E64A`)
3. Change them to your brand colors
4. Save and run `/create-10-posts` again

### Change Your Writing Style

Claude uses your personal voice and style guide by default. If you want to adjust it:

1. Edit `reference/rohit-voice-guide.md` to describe your writing style
2. Add examples of your best posts
3. Update your tone preferences (humor, formality, technical depth, etc.)
4. Run `/prime` then `/create-10-posts`

---

## Scheduling Daily Posts (Advanced)

If you have GitHub, you can set up **automatic daily posts**:

1. Push this repo to GitHub
2. Run `/schedule` to create a daily routine
3. Every morning, Claude generates 5 new posts automatically
4. Pull them to your computer when ready

(Instructions for this are in CLAUDE.md)

---

## Troubleshooting

**Q: "API key not found" error**
- Make sure you created `.env` file
- Make sure you added your actual API keys
- Make sure the file name is exactly `.env` (not `.env.txt`)

**Q: Claude says "I don't know you"**
- Edit `context/profile.md` and `context/strategy.md`
- Run `/prime` to reload context

**Q: Posts don't have images**
- Check that `context/images/` has photos
- Or check that your Kie.ai API key is correct

**Q: I don't like the posts Claude generated**
- Edit your `context/strategy.md` to be more specific
- Tell Claude what you DON'T want
- Try again

---

## Tips for Best Results

1. **Be specific about yourself** — vague descriptions = vague posts
2. **Add real data** — "31% growth" beats "good results"
3. **Include recent photos** — professional and casual both work
4. **Tell Claude your goals** — "attract recruiters" vs "build audience" gets different posts
5. **Review before posting** — Claude is smart but you know your brand better

---

## Next Steps

1. Fill in your `context/` files
2. Add your photos
3. Run `/prime` then `/create-10-posts`
4. Pick your favorites and publish
5. Come back tomorrow and create more posts

---

## Questions?

- Read `CLAUDE.md` — the full instructions are there
- Read `QUICK-START.md` — quick reference guide
- Read `PROJECT-SUMMARY.md` — deeper details about how everything works

---

**Made with ❤️ for content creators who want to build their personal brand.**
