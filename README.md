# lineage-priv_keys

# Usage

```bash
croot && git clone https://github.com/KernelBuilding/vendor_lineage-priv_keys vendor/lineage-priv/keys
```

```bash
cd vendor/lineage-priv/keys
```

```
./keys.sh
```

# Testing

Included `check_keys.py` script checks whether all apk/apex/capex files in the build out are signed with keys within its directory. Be aware that some targets are **expected** to be signed with vendor key, for example `com.android.apex.cts.shim.v1_prebuilt`.

```
$ ./check_keys.py ~/lineage/out/target/product/P661N
/home/hoshino/lineage/out/target/product/P661N/obj/ETC/com.android.apex.cts.shim.v1_prebuilt_intermediates/com.android.apex.cts.shim.apex is signed with an unknown key!
```
