# Spoticord Link

Spoticord Link is a Next.js application that enables users to connect their Spotify accounts to [Spoticord](https://github.com/SpoticordMusic/spoticord).

## Environment

|             Variable             | Description                                                                                                                                                           |
| :------------------------------: | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    DISCORD_TOKEN<sup>1</sup>     | Any Discord bot token (can be different from a Spoticord instance), for resolving user information                                                                    |
|     DATABASE_URL<sup>2</sup>     | A postgresql database URL, which must point to the same database as your Spoticord instance                                                                           |
|        SPOTIFY_CLIENT_ID         | Your Spotify app Client ID                                                                                                                                            |
|      SPOTIFY_CLIENT_SECRET       | Your spotify app Client Secret                                                                                                                                        |
| SPOTIFY_REDIRECT_URI<sup>3</sup> | The full URI to redirect to after (un)successful Spotify authentication (e.g. http://127.0.0.1:3000/authorize or https://&lt;auto-generated&gt;.vercel.app/authorize) |

### Important notes

- <sup>1</sup>: While not required, you may use a different Discord application than the one used for hosting the bot
- <sup>2</sup>: Make sure you use the same PostrgesDB database that you use for your Spoticord instance
- <sup>3</sup>: Insecure redirect URIs are no longer allowed in Spotify, this includes localhost. You are still allowed to use 127.0.0.1 without https.
