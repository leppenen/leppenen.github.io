# Nikita Leppenen

Welcome to my personal website!  

Feel free to explore my work and reach out!

## Updating conferences

Add an entry to `_data/conferences.yml`, then commit and push as usual:

```yaml
- name: Conference name
  location: City, Country
  year: 2027
  title: "My presentation title"
  type: oral
  region: Europe
```

Use `oral` or `poster` for `type`. Add `online: true` for online participation.
Use the host city's region even for online events. Use `Middle East` for Israel. Use `North America` or
`South America` where applicable. Quote text containing a colon followed by a space.

The Conferences page groups entries by year and recalculates both pie charts
automatically. Each entry counts as one presentation; two presentations at the
same conference count twice. No chart values need to be edited manually.

## Updating publications

Add one paper to `_data/publications.yml`, then commit and push as usual:

```yaml
- title: "My paper title"
  authors: [N. Leppenen, A. Collaborator]
  journal: Phys. Rev. A
  citation: "114, 013720"
  year: 2026
  doi: 10.1103/cy7b-hsl3
  field: Collective quantum optics
```

The publication list and all three charts update automatically. Author counts
come from the `authors` list, including all authors. Keep journal names consistent
and assign one primary `field` per paper. Current fields are:

- Collective quantum optics (superradiance and subradiance)
- Quantum-dot spins and spin–photon interfaces (including Zeno effects)
- Photogalvanics in topological materials (topological insulators and Weyl semimetals)
- Excitons in 2D materials (oscillator strength and Sommerfeld enhancement)

New journal names, author counts, and fields appear in the charts automatically.
