# Release

List of steps to create new release.

1. Install extras packages:

   ```bash
   pip install '.[release]'
   ```

2. Ensure `dist/` directory is clean:

   ```bash
   rm -fv dist/*
   ```

3. Create sdist and wheel:

   ```bash
   python -m build --sdist --wheel
   ```

4. Upload to testing PyPI:

   ```bash
   python3 -m twine upload --repository testpypi dist/*
   ```

5. Tag a release - replace X.Y.Z with actual version:

   ```bash
   git tag vX.Y.Z
   ```

6. Clean `dist/` directory again:

   ```bash
   rm -fv dist/*
   ```

7. Upload to production PyPI:

   ```bash
   python3 -m twine upload dist/*
   ```
