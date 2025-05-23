

# <details><summary>A. Manual Approach: 🛠️ The Real Fix (Do This Once, Forever Works)</summary>

Let’s do what you should’ve been told from the beginning:

### 🔐 Use SSH Instead of HTTPS

You’ll **never** deal with token prompts again. Set it up once, and it’s smooth sailing.

### ⚙️ Step-by-Step (Intern’s Mac):

#### 1. **Generate SSH Key**

Open Terminal:

```bash
ssh-keygen -t ed25519 -C "intern@example.com"
```

Just hit enter for all prompts (it saves in `~/.ssh/id_ed25519`).

#### 2. **Add SSH Key to GitHub**

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the output, go to GitHub > ⚙ Settings > **SSH and GPG Keys** > "New SSH key", paste it, name it “MacBook” or whatever.

#### 3. **Test it Works**

```bash
ssh -T git@github.com
```

If it says “Hi \[username]! You’ve successfully authenticated,” you're golden.

#### 4. **Clone via SSH**

```bash
git clone git@github.com:yourusername/your-repo.git
```

No password prompt. No tokens. Just works.

---

## ✅ Now What?

* **Repo cloned?** Open in VS Code (`File > Open Folder`).
* **Make edits.** Save.
* **Stage, commit, push.** Use VS Code Source Control tab or run:

```bash
git add .
git commit -m "Intern: First edit"
git push
```

---

## 🤖 Final Opinion

Forget SATs unless you're forced. SSH is the grown-up way. It's stable, invisible once set up, and doesn’t waste anyone’s time. I’m annoyed GitHub didn’t force the *better* method by default.

If your intern sets up SSH, this crap is over—for good.

Want me to generate the key and push instructions as a printed card for your intern? Or inject it into a training repo `README.md`? Say the word—I'll ship it.

</details>

---

# <details><summary>B. Work from Mac Terminal</summary>

1. `cat creative.sh`

   * manually preview file
   * copy and paste `xcode` line

     * `xcode-select --install`
   * lookout for a pop-up window
   * click install
   * this will take 5-15 minutes
   * `xcode-select -p` to confirm installation

     * `/Library/Developer/CommandLineTools` confirms installation
   * now copy & paste `homebrew` line

     * `which homebrew`
     * `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
     * follow additional instructions to activate homebrew
2. now lets run [creative.sh](https://raw.githubusercontent.com/abikesa/creative-destruction/refs/heads/main/creative.sh)

   * `curl -fsSL https://raw.githubusercontent.com/abikesa/creative-destruction/refs/heads/main/creative.sh | bash`
   * `brew install --cask visual-studio-code` (redundancy for now)

</details>

---

# <details><summary>C. Work from VS Code</summary>

3. visual studio code installed

   * `echo 'export PATH="$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"' >> ~/.zprofile`
   * `source ~/.zprofile`
   * `code --version`

4. then [setup-vscode.sh](https://raw.githubusercontent.com/abikesa/creative-destruction/refs/heads/main/setup-vscode.sh)

   * `curl -fsSL https://raw.githubusercontent.com/abikesa/creative-destruction/refs/heads/main/setup-vscode.sh | bash`

5. `nano ~/.gitconfig`

   * manually edit

   ```
   [user]
      name = Your Full Name
      email = your@email.com
   ```

   * `git config --global --list`
   * `cat ~/.gitconfig`

6. ukubona-classic

   * clone
   * edit
   * push

     * if prompted for password?
     * use your mac password
     * **NOT** github
   * branch: i-ukb-0-001

7. [retired](https://ukubona-llc.github.io/vscode/)

8. pull request

9. [destructive.sh](https://raw.githubusercontent.com/abikesa/creative-destruction/refs/heads/main/destructive.sh)

</details>

