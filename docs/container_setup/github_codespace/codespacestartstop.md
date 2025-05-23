### How to Stop Codespaces?

#### 1. Navigate to Codespaces Panel

To stop codespace we just need to navigate to the Codespaces option in the
bottom left of the Codespace panel.

![stop codespace](../../assets/rdev14.png)

#### 2. Open Dropdown Menu

After clicking on codespaces option we will get a drop down above something
like this👇

![stop codespace](../../assets/rdev15.png)

#### 3. Stop Current Codespace

Click on "Stop Current Codespace". It will stop the codespaces you are
currently using or running.

#### 4. Redirect to Restart Page'

You will be redirected to a Restart Codespace page. The page shows a

![stop codespace](../../assets/rdev16.png)

!!! Note
    Idle Timeout:
    If you do not interact with the codespace, it will close automatically when
    it reaches the idle timeout limit. By default, this is 30 minutes, but you
    can [set a personal timeout](https://docs.github.com/en/codespaces/setting-your-user-preferences/setting-your-timeout-period-for-github-codespaces#setting-your-default-timeout-period)
    limit in your GitHub settings.

The code changes and operations we have performed inside the codespace will
still be inside the stopped codespace. If your codespace is stopped then you can

### How to Restart Codespaces again?

#### 1. Access Codespaces List

Go to [github.com/codespaces](https://github.com/codespaces)

#### 2. Restart a Codespace

Here we can see a list of the codespaces we have created

 ![stop codespace](../../assets/rdev17.png)

#### 3. Check Active Status

To restart it, we can just click on the codespaces we wanted

#### 4. Manage Codespaces

<!-- markdownlint-disable-next-line MD012 -->

![stop codespace](../../assets/rdev18.png)

### Setting a Default Retention Period for Your Codespaces

#### 1.Access Settings

- Click your profile photo in the upper-right corner of any GitHub page.
- Click "Settings."

#### 2.Navigate to Codespaces Settings

- In the sidebar, under "Code, planning, and automation," click "Codespaces."

#### 3.Set Retention Period

- Under "Default retention period," enter the number of days (between 0 and 30)
for which you want your codespaces to be retained after they have been stopped.
Example: Setting it to 30 days.  ![retain
codespace](../../assets/manage_codespace.png)
!!! Warning
    Setting the retention period to 0 days will result in immediate deletion
    of codespaces when stopped or when they timeout due to inactivity.
    For more details, refer to ["Setting your timeout period for GitHub Codespaces."](https://docs.github.com/en/codespaces/setting-your-user-preferences/setting-your-timeout-period-for-github-codespaces#setting-your-default-timeout-period)

#### 4.Save Changes

- Click "Save" to apply the new retention period.

This allows you to customize how long your codespaces are kept before automatic
deletion, balancing convenience and storage management.

### Auto Delete Codespace

- Go to the "Your codespaces" page at
- Find the codespace you want to exempt from deletion.
- Click the options menu (three dots) to the right of the codespace.
- Select "Auto Delete Codespace" from the dropdown menu. The bookmarked
  codespaces will not be auto-deleted.
