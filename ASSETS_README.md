# Assets Folder Structure

Place the following files in `./assets/` alongside the `.mdx` file:

| Asset filename                   | Source file (from this upload)                      | Description                              |
|----------------------------------|-----------------------------------------------------|------------------------------------------|
| `00_video_chaos_theory.gif`      | `00_video_chaos_theory.mp4` (convert to GIF)        | Animated Lorenz Attractor — 200 frames   |
| `04_lorenz_attractor.png`        | `04_Screenshot_2026-03-10_at_11_58_54_AM.png`       | Lorenz 3D phase portrait, 80,000 pts     |
| `05_butterfly_effect.png`        | `05_Screenshot_2026-03-10_at_11_59_56_AM.png`       | Butterfly effect — 3 time windows        |
| `08_mandelbrot_set.png`          | `08_Screenshot_2026-03-10_at_12_02_31_PM.png`       | Mandelbrot set — 3 zoom levels           |
| `10_julia_set_gallery.png`       | `10_Screenshot_2026-03-10_at_12_03_27_PM.png`       | Julia set gallery — 8 constants          |
| `12_lyapunov_fractal.png`        | `12_Screenshot_2026-03-10_at_12_06_15_PM.png`       | Lyapunov fractal — order/chaos boundary  |
| `15_poincare_sections.png`       | `15_Screenshot_2026-03-10_at_12_15_07_PM.png`       | Poincaré sections — return map           |

## Convert MP4 to GIF (optional)

```bash
# Using ffmpeg
ffmpeg -i 00_video_chaos_theory.mp4 -vf "fps=25,scale=800:-1:flags=lanczos" assets/00_video_chaos_theory.gif

# Or keep as MP4 and update the MDX img tag to a <video> tag:
# <video src="./assets/00_video_chaos_theory.mp4" autoplay loop muted playsinline />
```

## GitHub Rendering Notes

- GitHub renders `.md` files natively. For `.mdx`, use with a framework like **Next.js**, **Gatsby**, or **Astro**.
- LaTeX math (`$$ ... $$`) renders on GitHub with the new math support (available since 2022).
- For a pure GitHub markdown file, rename to `the-art-of-chaos.md` — everything will render correctly except JSX components (none used here).
