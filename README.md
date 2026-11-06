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
