using Steamworks;

        #region Friend List overlay
        void OnFriendsLoad()
        {

            InvokeRepeating("UpdateState", 0, 2);

            int friendCount = SteamFriends.GetFriendCount(EFriendFlags.k_EFriendFlagImmediate);
            for (int i = 0; i < friendCount; ++i)
            {
                CSteamID friendSteamId = SteamFriends.GetFriendByIndex(i, EFriendFlags.k_EFriendFlagImmediate);
                string friendName = SteamFriends.GetFriendPersonaName(friendSteamId);
                int friendAvatar = SteamFriends.GetLargeFriendAvatar(friendSteamId);
                EPersonaState friendState = SteamFriends.GetFriendPersonaState(friendSteamId);
                if (friendState == EPersonaState.k_EPersonaStateOnline)
                {
                    Debug.Log(friendName);
                }


                FriendGameInfo_t info;
                SteamFriends.GetFriendGamePlayed(friendSteamId, out info);
                // Debug.Log(friendName);

            }
        }
        #endregion
