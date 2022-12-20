# ruApps

```console
git clone https://github.com/fakelog/android_vendor_ruapps.git vendor/ruapps
```

in BoardConfig.mk add

```make
WITH_RUAPPS := true
```

in device.mk add

```make
# RuApps
ifneq ($(WITH_RUAPPS),true)
$(call inherit-product, vendor/ruapps/arm64/arm64-vendor.mk)
endif
```
