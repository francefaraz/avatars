# Free Fire-style avatar additions

Added 20 October 2026. Four original battle royale portraits generated with the built-in image generation tool. Existing avatar files and purchases stay unchanged.

The new image files live in `C:/munexa/avatars`, published through the `francefaraz/avatars` repository. The app references their raw GitHub URLs; the new PNGs are not bundled in Flutter assets. Unlock prices were approved by the user. No new Google Play product is needed for diamond unlocks.

| Preview | Avatar | Diamonds | Raw image URL |
| --- | --- | ---: | --- |
| ![Shadow Viper](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_shadow_viper.png) | Shadow Viper | 75 | [ff_shadow_viper.png](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_shadow_viper.png) |
| ![Crimson Rebel](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_crimson_rebel.png) | Crimson Rebel | 75 | [ff_crimson_rebel.png](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_crimson_rebel.png) |
| ![Arctic Wolf](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_arctic_wolf.png) | Arctic Wolf | 100 | [ff_arctic_wolf.png](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_arctic_wolf.png) |
| ![Desert Falcon](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_desert_falcon.png) | Desert Falcon | 100 | [ff_desert_falcon.png](https://raw.githubusercontent.com/francefaraz/avatars/main/ff_desert_falcon.png) |

## Integration

`lib/models/avatar_item.dart` adds four catalog entries with remoteImageUrl. `AvatarArtwork` renders existing bundled portraits and new network portraits, with a loading indicator and image-error fallback. Collection, preview and profile use it for remote additions. Equip writes the same remote URL into the player profile, so existing room-host and leaderboard renderers can reuse it. Normal diamond debit, ownership checks and activity history apply.

Zip Game reference: `C:/munexa/zipgame/avatar.md` and `app/src/main/java/far/munexa/zipgame/utils/FirebaseManager.kt` use `https://cdn.jsdelivr.net/gh/francefaraz/avatars/{avatarId}.png`. Brain Battle currently uses `https://cdn.jsdelivr.net/gh/alohe/avatars/png/`; its source was inspected as a reference and not modified.

## Generation prompts

Mode: built-in image_gen; new images, no reference inputs or CLI fallback. Final files: `C:/munexa/avatars/<id>.png`.

### Shadow Viper

Use case: stylized-concept. Asset type: square gaming profile avatar for a Free Fire-style battle royale room app. Create original premium game character portrait: an adult masked tactical scout, charcoal hood, emerald visor and subtle green armor trims, poised and confident. Head and shoulders, centered, face and silhouette comfortably inside a circular crop, dark navy studio background, vivid cinematic rim lighting, polished detailed 3D game key art matching a premium avatar shop. Single character, no scene props, no weapons, no text, no letters, no logos, no watermark. Original character design.

### Crimson Rebel

Use case: stylized-concept. Asset type: square gaming profile avatar for a Free Fire-style battle royale room app. Create original premium game character portrait: an adult woman with warm brown skin, short asymmetric dark hair with a red streak, crimson tactical street jacket, confident focused expression. Head and shoulders, centered, face and silhouette comfortably inside a circular crop, dark navy studio background, vivid cinematic rim lighting, polished detailed 3D game key art matching a premium avatar shop. Single character, no scene props, no weapons, no text, no letters, no logos, no watermark. Original character design.

### Arctic Wolf

Use case: stylized-concept. Asset type: square gaming profile avatar for a Free Fire-style battle royale room app. Create original premium game character portrait: an adult male battle royale ranger, silver hair, icy blue eyes, white and navy winter tactical collar with subtle wolf-inspired angular detailing. Head and shoulders, centered, face and silhouette comfortably inside a circular crop, dark navy studio background, vivid cinematic rim lighting, polished detailed 3D game key art matching a premium avatar shop. Single character, no scene props, no weapons, no text, no letters, no logos, no watermark. Original character design.

### Desert Falcon

Use case: stylized-concept. Asset type: square gaming profile avatar for a Free Fire-style battle royale room app. Create original premium game character portrait: an adult woman with medium brown skin, amber goggles pushed onto her forehead, sand-colored scarf, bronze tactical armor, determined friendly expression. Head and shoulders, centered, face and silhouette comfortably inside a circular crop, dark navy studio background, vivid cinematic rim lighting, polished detailed 3D game key art matching a premium avatar shop. Single character, no scene props, no weapons, no text, no letters, no logos, no watermark. Original character design.

