Use kubectl to patch all matching items

# Usage

Change `terminationGracePeriodSeconds` of all deployment pods

```bash
kubectl patch-all deployment -A --type merge --patch '{"spec":{"template":{"spec":{"terminationGracePeriodSeconds":0}}}}'
```

# Install

## Option A: via `krew`

```bash
krew install --manifest-url https://raw.githubusercontent.com/grosser/kubectl-patch-all/main/krew.yaml
```

## Option B: copy into your /usr/local/bin folder

```bash
wget TODO
chmod +x /usr/local/bin/kubectl-patch-all
```

## Option C: use from checkout

```bash
git clone git@github.com:grosser/kubectl-patch-all.git
PATH=$PATH:$PWD/kubectl-patch-all
```

# TODO
- covert to go
- get into krew
