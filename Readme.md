Use kubectl to patch all matching items

# Usage

Change `terminationGracePeriodSeconds` of all deployment pods

```bash
kubectl patch-all deployment -A --type merge --patch '{"spec":{"template":{"spec":{"terminationGracePeriodSeconds":0}}}}'
```

# Install

## Option A: via `krew`

```bash
kubectl krew install --manifest-url https://raw.githubusercontent.com/grosser/kubectl-patch-all/main/krew.yaml
```

## Option B: copy into your /usr/local/bin folder

```bash
sudo wget https://raw.githubusercontent.com/grosser/kubectl-patch-all/main/kubectl-patch-all -O /usr/local/bin/kubectl-patch_all
sudo chmod +x /usr/local/bin/kubectl-patch_all
```

## Option C: use from checkout

```bash
git clone git@github.com:grosser/kubectl-patch-all.git
cd kubectl-patch-all && ./kubectl-patch-all
```

# Release

- tag new release
- push release
- `wget https://github.com/grosser/kubectl-patch-all/archive/refs/tags/<TAG>.zip`
- `sha256sum <TAG>.zip`
- update `krew.yaml` with new url and sha and push a new commit

# TODO

- covert to go
- get into krew
