# What
- Play Asset Delivery Using Addressable for Unity


# How To Install Package

Add the lines below to `Packages/manifest.json`

for version 1.0.0
```csharp
"com.pancake.play-asset-delivery": "https://github.com/pancake-llc/play-asset-delivery-addressable.git#1.0.0",
```


# Usages

- Step 1: If you have not created a setting for addressable, create it by going to menu `Window` > `Asset Management` > `Addressables` > `Groups` > `Create Addressables Settings`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_1.jpg" width="600"  alt=""/></p>

- Step 2: Create `PlayAssetDeliveryInitializationSettings`. Access the create menu via right click > `Create` > `Addressables` > `Initialization` > `PlayAssetDeliveryInitializationSettings`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_2.jpg" width="600"  alt=""/></p>

- Step 3: Create `BuildScriptPlayAssetDelivery`. Go to menu `Create` > `Addressables` > `Custom Build` > `Play Asset Delivery`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_3.jpg" width="600"  alt=""/></p>

- Step 4: Create `AssetPacksContent`. Truly go to menu `Create` > `Addressables` > `Group Tempaltes` > `Blank Group Template` > Rename to AssetPackContent


- Step 5: Add Schema Content Packing Loading for AssetPackContent

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_4.jpg" width="600"  alt=""/></p>

- Step 6: In Content Packing & Loading
	- change `BuildPath` to `Local.BuildPath`
	- change `LoadPath` to `Local.LoadPath`
	- change `Asset Provider` to `Assets from Bundles Provider`
	- change `Asset Bundle Provider` to `AssetBundle Provider`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_5.jpg" width="600"  alt=""/></p>

- Step 7: Add Schema Play Asset Delivery and change Asset Pack to InstallTimeContent (InstallTime).

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_6.jpg" width="600"  alt=""/></p>

- Step 8: Open `AddressableAssetSettings`
	- In Build and Play Mode Scripts add `BuildScriptPlayAssetDelivery`
	- In Asset Group Templates add `AssetPackContent`
	- In Initializatio Objects add `PlayAssetDeliveryInitializationSettings`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_7.jpg" width="600"  alt=""/></p>

- Step 9: Move `AssetPackContent`, `BuildScriptPlayAssetDelivery`, `PlayAssetDeliveryInitializationSettings` to folder `PlayAssetDelivery/Data`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_8.jpg" width="600"  alt=""/></p>


- Step 10: In the Addressables window, instead of using the menu `Build` > `New Build` > `Build Default Script`, we now use the menu `Build` > `New Build` > `Play Asset Delivery`

<p style="text-align: center;"><img src="https://cdn.jsdelivr.net/npm/yenmoc-assets@1.0.62/img/pad_9.jpg" width="600"  alt=""/></p>