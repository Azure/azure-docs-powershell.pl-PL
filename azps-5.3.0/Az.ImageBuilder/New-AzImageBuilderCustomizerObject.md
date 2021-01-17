---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489549"
---
# <span data-ttu-id="496cb-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="496cb-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="496cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="496cb-102">SYNOPSIS</span></span>
<span data-ttu-id="496cb-103">Omówienie dostosowywania jednostki obrazu</span><span class="sxs-lookup"><span data-stu-id="496cb-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="496cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="496cb-104">SYNTAX</span></span>

### <span data-ttu-id="496cb-105">ShellCustomizer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="496cb-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="496cb-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="496cb-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="496cb-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="496cb-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="496cb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="496cb-110">DESCRIPTION</span></span>
<span data-ttu-id="496cb-111">Omówienie dostosowywania jednostki obrazu</span><span class="sxs-lookup"><span data-stu-id="496cb-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="496cb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="496cb-112">EXAMPLES</span></span>

### <span data-ttu-id="496cb-113">Przykład 1: Tworzenie konfiguratora aktualizacji systemu Windows</span><span class="sxs-lookup"><span data-stu-id="496cb-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="496cb-114">To polecenie tworzy konfiguratora aktualizacji systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="496cb-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="496cb-115">Przykład 2: Tworzenie konfiguratora plików</span><span class="sxs-lookup"><span data-stu-id="496cb-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="496cb-116">To polecenie tworzy konfiguratora plików.</span><span class="sxs-lookup"><span data-stu-id="496cb-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="496cb-117">Przykład 3: Tworzenie konfiguratora programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="496cb-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="496cb-118">To polecenie tworzy konfiguratora programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="496cb-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="496cb-119">Przykład 4: Tworzenie konfiguratora ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="496cb-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="496cb-120">To polecenie tworzy konfiguratora ponownego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="496cb-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="496cb-121">Przykład 5: Tworzenie konfiguratora powłoki</span><span class="sxs-lookup"><span data-stu-id="496cb-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="496cb-122">To polecenie tworzy konfiguratora powłoki.</span><span class="sxs-lookup"><span data-stu-id="496cb-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="496cb-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="496cb-123">PARAMETERS</span></span>

### <span data-ttu-id="496cb-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="496cb-124">-CustomizerName</span></span>
<span data-ttu-id="496cb-125">Przyjazna nazwa, która umożliwia określenie kontekstu tego kroku dostosowania.</span><span class="sxs-lookup"><span data-stu-id="496cb-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-126">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="496cb-126">-Destination</span></span>
<span data-ttu-id="496cb-127">Bezwzględna ścieżka do pliku (z zagnieżdżonymi strukturami katalogów), w którym do maszyny wirtualnej zostanie przekazany plik (z sourceUri).</span><span class="sxs-lookup"><span data-stu-id="496cb-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-128">-FileCustomizer</span></span>
<span data-ttu-id="496cb-129">Umożliwia przekazywanie plików do maszyn wirtualnych (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="496cb-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="496cb-130">Odpowiada wydziałowi obsługi plików programu pakujący.</span><span class="sxs-lookup"><span data-stu-id="496cb-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="496cb-131">-Filter</span></span>
<span data-ttu-id="496cb-132">Tablica filtrów umożliwia wybranie aktualizacji do zastosowania.</span><span class="sxs-lookup"><span data-stu-id="496cb-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="496cb-133">Pomiń lub określ pustą tablicę, aby użyć domyślnej (brak filtru).</span><span class="sxs-lookup"><span data-stu-id="496cb-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="496cb-134">Skorzystaj z powyższego linku, aby zapoznać się z przykładami i szczegółowym opisem tego pola.</span><span class="sxs-lookup"><span data-stu-id="496cb-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-135">-W tekście</span><span class="sxs-lookup"><span data-stu-id="496cb-135">-Inline</span></span>
<span data-ttu-id="496cb-136">Tablica poleceń powłoki do wykonania.</span><span class="sxs-lookup"><span data-stu-id="496cb-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="496cb-138">Uruchamia określony program PowerShell na maszynie wirtualnej (Windows).</span><span class="sxs-lookup"><span data-stu-id="496cb-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="496cb-139">Odpowiada programowi do obsługi programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="496cb-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="496cb-140">Można określić dokładnie jedno z "scriptUri" lub "w tekście".</span><span class="sxs-lookup"><span data-stu-id="496cb-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="496cb-141">-RestartCheckCommand</span></span>
<span data-ttu-id="496cb-142">Polecenie sprawdzenia, czy ponowne uruchomienie zostało pomyślnie zakończone [domyślnie: ' '].</span><span class="sxs-lookup"><span data-stu-id="496cb-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="496cb-143">-RestartCommand</span></span>
<span data-ttu-id="496cb-144">Polecenie wykonania ponownego uruchamiania [domyślnie: "shutdown/r/f/t 0/c pakujący"]</span><span class="sxs-lookup"><span data-stu-id="496cb-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-145">-RestartCustomizer</span></span>
<span data-ttu-id="496cb-146">Ponowna rozruch maszyny wirtualnej i oczekiwanie na powrót do trybu online (Windows).</span><span class="sxs-lookup"><span data-stu-id="496cb-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="496cb-147">Odpowiada pakietowi pakującemu na ponowne uruchomienie systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="496cb-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="496cb-148">-RestartTimeout</span></span>
<span data-ttu-id="496cb-149">Limit czasu ponownego uruchamiania określony jako ciąg wielkości i jednostki, na przykład "mln" (5 minut) lub "2H" (2 godziny) [domyślnie: "mln"].</span><span class="sxs-lookup"><span data-stu-id="496cb-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="496cb-150">-RunElevated</span></span>
<span data-ttu-id="496cb-151">Jeśli jest określony, skrypt programu PowerShell będzie uruchomiony z podniesionymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="496cb-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="496cb-152">-ScriptUri</span></span>
<span data-ttu-id="496cb-153">Identyfikator URI skryptu powłoki, który ma zostać uruchomiony w celu dostosowania.</span><span class="sxs-lookup"><span data-stu-id="496cb-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="496cb-154">Może to być link z usługą GitHub, identyfikator URI SAS dla magazynu Azure itd.</span><span class="sxs-lookup"><span data-stu-id="496cb-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="496cb-155">-SearchCriterion</span></span>
<span data-ttu-id="496cb-156">Kryteria wyszukiwania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="496cb-156">Criteria to search updates.</span></span>
<span data-ttu-id="496cb-157">Pomiń lub określ pusty ciąg, aby użyć ustawień domyślnych (Wyszukaj wszystkie).</span><span class="sxs-lookup"><span data-stu-id="496cb-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="496cb-158">Skorzystaj z powyższego linku, aby zapoznać się z przykładami i szczegółowym opisem tego pola.</span><span class="sxs-lookup"><span data-stu-id="496cb-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="496cb-159">-Sha256Checksum</span></span>
<span data-ttu-id="496cb-160">SHA256 Checksum skryptu powłoki podanego w polu scriptUri.</span><span class="sxs-lookup"><span data-stu-id="496cb-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-161">-ShellCustomizer</span></span>
<span data-ttu-id="496cb-162">Powoduje uruchomienie skryptu powłoki podczas fazy dostosowywania (Linux).</span><span class="sxs-lookup"><span data-stu-id="496cb-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="496cb-163">Odpowiada aprowizacji powłoki programu pakujący.</span><span class="sxs-lookup"><span data-stu-id="496cb-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="496cb-164">Można określić dokładnie jedno z "scriptUri" lub "w tekście".</span><span class="sxs-lookup"><span data-stu-id="496cb-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="496cb-165">-SourceUri</span></span>
<span data-ttu-id="496cb-166">Identyfikator URI pliku, który ma zostać przekazany w celu dostosowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="496cb-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="496cb-167">Może to być link z usługą GitHub, identyfikator URI SAS dla magazynu Azure itd.</span><span class="sxs-lookup"><span data-stu-id="496cb-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="496cb-168">-UpdateLimit</span></span>
<span data-ttu-id="496cb-169">Maksymalna liczba aktualizacji do jednoczesnego zastosowania.</span><span class="sxs-lookup"><span data-stu-id="496cb-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="496cb-170">Pomiń lub określ wartość 0, aby użyć wartości domyślnej (1000).</span><span class="sxs-lookup"><span data-stu-id="496cb-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="496cb-171">-ValidExitCode</span></span>
<span data-ttu-id="496cb-172">Prawidłowe kody wyjściowe skryptu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="496cb-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="496cb-173">[Domyślnie: 0].</span><span class="sxs-lookup"><span data-stu-id="496cb-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="496cb-175">Instaluje aktualizacje systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="496cb-175">Installs Windows Updates.</span></span>
<span data-ttu-id="496cb-176">Odpowiada pakietowi obsługi administracyjna usługi Windows Update https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="496cb-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496cb-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496cb-177">CommonParameters</span></span>
<span data-ttu-id="496cb-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496cb-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496cb-179">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="496cb-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496cb-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="496cb-180">INPUTS</span></span>

## <span data-ttu-id="496cb-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="496cb-181">OUTPUTS</span></span>

### <span data-ttu-id="496cb-182">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="496cb-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="496cb-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="496cb-183">NOTES</span></span>

<span data-ttu-id="496cb-184">PISUJE</span><span class="sxs-lookup"><span data-stu-id="496cb-184">ALIASES</span></span>

## <span data-ttu-id="496cb-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="496cb-185">RELATED LINKS</span></span>

