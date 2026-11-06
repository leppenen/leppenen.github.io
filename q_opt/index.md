---
layout: default
title: Quantum Optics
---

[← Back to home]({{ '/' | relative_url }})

# ⚛️💡 Quantum Optics

<details markdown="1">
<summary><h2 style="display: inline;">📚 Useful Books</h2></summary>

I recommend starting with lecture notes and diving into research as soon as possible, rather than spending too much time working through classic textbooks. In my view, Scully and Zubairy is enough as a general textbook to keep on hand.

- [Lukin — Lecture notes (PDF)]({{ '/q_opt/books/Lukin_lectures.pdf' | relative_url }}) — Lecture notes by someone I consider one of the most influential scientists in the field.
- [Poddubny — Book draft (PDF)]({{ '/q_opt/books/Poddubny_book.pdf' | relative_url }}) — A draft of Professor Poddubny’s upcoming book.
- [Keeling — Lecture notes (PDF)]({{ '/q_opt/books/Keeling_lectures.pdf' | relative_url }}) — Includes a short introduction to collective quantum optics.
- [Novotny and Hecht (PDF)]({{ '/q_opt/books/Novotny_Hecht.pdf' | relative_url }}) — Useful for Green’s functions and spontaneous emission rates.
- <a href="{{ '/q_opt/books/Scully_Zubairy.djvu' | relative_url }}" download>Scully and Zubairy — Download (DjVu)</a> — A classic quantum optics textbook that is nice to have on hand.

</details>

<details markdown="1">
<summary><h2 style="display: inline;">🎥 Useful Lectures</h2></summary>

- [A crash course in quantum trajectories](https://www.youtube.com/watch?v=F4GHy1NcBFY&t=4017s)
- [An introduction to collective quantum optics by my PI, Ephraim Shahmoon](https://www.youtube.com/watch?v=IoGY1Dlmsuw)
- [Ana Maria Rey on the Dicke phase transition and entanglement generation](https://www.youtube.com/watch?v=wvZ1yRU_Cjg)
- [Norman Yao on time crystals](https://www.youtube.com/watch?v=_yy024F-d2s)

</details>

## 🐍💻 Python + HPC Tutorials for the Collective Quantum Optics Group

My tutorials on using a high-performance computing (HPC) cluster for quantum optics, with practical examples.

[GitHub repository: CQO_comp](https://github.com/leppenen/CQO_comp)

<div class="tutorial-links">
  <a href="https://github.com/leppenen/CQO_comp/blob/main/docs/tex_docs/lect1_slides.pdf">Tutorial 1: Introduction</a>
  <a href="https://github.com/leppenen/CQO_comp/blob/main/docs/tex_docs/lect2_slides.pdf">Tutorial 2: MCWF</a>
  <a href="https://github.com/leppenen/CQO_comp/blob/main/docs/tex_docs/bonus_GF.pdf">Bonus: Green’s Function with NumPy</a>
</div>

<style>
  .tutorial-links {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1em;
    margin: 1em 0;
  }

  @media (max-width: 600px) {
    .tutorial-links {
      grid-template-columns: 1fr;
    }
  }
</style>
