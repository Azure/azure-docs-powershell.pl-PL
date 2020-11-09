---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304027"
---
# <span data-ttu-id="4d7cd-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="4d7cd-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="4d7cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7cd-103">Omówienie dostosowywania jednostki obrazu</span><span class="sxs-lookup"><span data-stu-id="4d7cd-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="4d7cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d7cd-104">SYNTAX</span></span>

### <span data-ttu-id="4d7cd-105">ShellCustomizer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d7cd-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="4d7cd-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="4d7cd-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d7cd-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="4d7cd-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4d7cd-110">Opis</span><span class="sxs-lookup"><span data-stu-id="4d7cd-110">DESCRIPTION</span></span>
<span data-ttu-id="4d7cd-111">Omówienie dostosowywania jednostki obrazu</span><span class="sxs-lookup"><span data-stu-id="4d7cd-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="4d7cd-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d7cd-112">EXAMPLES</span></span>

### <span data-ttu-id="4d7cd-113">Przykład 1: Tworzenie konfiguratora aktualizacji systemu Windows</span><span class="sxs-lookup"><span data-stu-id="4d7cd-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="4d7cd-114">To polecenie tworzy konfiguratora aktualizacji systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="4d7cd-115">Przykład 2: Tworzenie konfiguratora plików</span><span class="sxs-lookup"><span data-stu-id="4d7cd-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="4d7cd-116">To polecenie tworzy konfiguratora plików.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="4d7cd-117">Przykład 3: Tworzenie konfiguratora programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="4d7cd-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="4d7cd-118">To polecenie tworzy konfiguratora programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="4d7cd-119">Przykład 4: Tworzenie konfiguratora ponownego uruchamiania</span><span class="sxs-lookup"><span data-stu-id="4d7cd-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="4d7cd-120">To polecenie tworzy konfiguratora ponownego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="4d7cd-121">Przykład 5: Tworzenie konfiguratora powłoki</span><span class="sxs-lookup"><span data-stu-id="4d7cd-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="4d7cd-122">To polecenie tworzy konfiguratora powłoki.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="4d7cd-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d7cd-123">PARAMETERS</span></span>

### <span data-ttu-id="4d7cd-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="4d7cd-124">-CustomizerName</span></span>
<span data-ttu-id="4d7cd-125">Przyjazna nazwa, która umożliwia określenie kontekstu tego kroku dostosowania.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="4d7cd-126">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="4d7cd-126">-Destination</span></span>
<span data-ttu-id="4d7cd-127">Bezwzględna ścieżka do pliku (z zagnieżdżonymi strukturami katalogów), w którym do maszyny wirtualnej zostanie przekazany plik (z sourceUri).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="4d7cd-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-128">-FileCustomizer</span></span>
<span data-ttu-id="4d7cd-129">Umożliwia przekazywanie plików do maszyn wirtualnych (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="4d7cd-130">Odpowiada wydziałowi obsługi plików programu pakujący.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="4d7cd-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="4d7cd-131">-Filter</span></span>
<span data-ttu-id="4d7cd-132">Tablica filtrów umożliwia wybranie aktualizacji do zastosowania.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="4d7cd-133">Pomiń lub określ pustą tablicę, aby użyć domyślnej (brak filtru).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="4d7cd-134">Skorzystaj z powyższego linku, aby zapoznać się z przykładami i szczegółowym opisem tego pola.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="4d7cd-135">-W tekście</span><span class="sxs-lookup"><span data-stu-id="4d7cd-135">-Inline</span></span>
<span data-ttu-id="4d7cd-136">Tablica poleceń powłoki do wykonania.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="4d7cd-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="4d7cd-138">Uruchamia określony program PowerShell na maszynie wirtualnej (Windows).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="4d7cd-139">Odpowiada programowi do obsługi programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="4d7cd-140">Można określić dokładnie jedno z "scriptUri" lub "w tekście".</span><span class="sxs-lookup"><span data-stu-id="4d7cd-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="4d7cd-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="4d7cd-141">-RestartCheckCommand</span></span>
<span data-ttu-id="4d7cd-142">Polecenie sprawdzenia, czy ponowne uruchomienie zostało pomyślnie zakończone [domyślnie: ' '].</span><span class="sxs-lookup"><span data-stu-id="4d7cd-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="4d7cd-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="4d7cd-143">-RestartCommand</span></span>
<span data-ttu-id="4d7cd-144">Polecenie wykonania ponownego uruchamiania [domyślnie: "shutdown/r/f/t 0/c pakujący"]</span><span class="sxs-lookup"><span data-stu-id="4d7cd-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="4d7cd-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-145">-RestartCustomizer</span></span>
<span data-ttu-id="4d7cd-146">Ponowna rozruch maszyny wirtualnej i oczekiwanie na powrót do trybu online (Windows).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="4d7cd-147">Odpowiada pakietowi pakującemu na ponowne uruchomienie systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="4d7cd-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="4d7cd-148">-RestartTimeout</span></span>
<span data-ttu-id="4d7cd-149">Limit czasu ponownego uruchamiania określony jako ciąg wielkości i jednostki, na przykład "mln" (5 minut) lub "2H" (2 godziny) [domyślnie: "mln"].</span><span class="sxs-lookup"><span data-stu-id="4d7cd-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="4d7cd-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="4d7cd-150">-RunElevated</span></span>
<span data-ttu-id="4d7cd-151">Jeśli jest określony, skrypt programu PowerShell będzie uruchomiony z podniesionymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="4d7cd-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="4d7cd-152">-ScriptUri</span></span>
<span data-ttu-id="4d7cd-153">Identyfikator URI skryptu powłoki, który ma zostać uruchomiony w celu dostosowania.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="4d7cd-154">Może to być link z usługą GitHub, identyfikator URI SAS dla magazynu Azure itd.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="4d7cd-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="4d7cd-155">-SearchCriterion</span></span>
<span data-ttu-id="4d7cd-156">Kryteria wyszukiwania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-156">Criteria to search updates.</span></span>
<span data-ttu-id="4d7cd-157">Pomiń lub określ pusty ciąg, aby użyć ustawień domyślnych (Wyszukaj wszystkie).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="4d7cd-158">Skorzystaj z powyższego linku, aby zapoznać się z przykładami i szczegółowym opisem tego pola.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="4d7cd-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="4d7cd-159">-Sha256Checksum</span></span>
<span data-ttu-id="4d7cd-160">SHA256 Checksum skryptu powłoki podanego w polu scriptUri.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="4d7cd-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-161">-ShellCustomizer</span></span>
<span data-ttu-id="4d7cd-162">Powoduje uruchomienie skryptu powłoki podczas fazy dostosowywania (Linux).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="4d7cd-163">Odpowiada aprowizacji powłoki programu pakujący.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="4d7cd-164">Można określić dokładnie jedno z "scriptUri" lub "w tekście".</span><span class="sxs-lookup"><span data-stu-id="4d7cd-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="4d7cd-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="4d7cd-165">-SourceUri</span></span>
<span data-ttu-id="4d7cd-166">Identyfikator URI pliku, który ma zostać przekazany w celu dostosowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="4d7cd-167">Może to być link z usługą GitHub, identyfikator URI SAS dla magazynu Azure itd.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="4d7cd-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="4d7cd-168">-UpdateLimit</span></span>
<span data-ttu-id="4d7cd-169">Maksymalna liczba aktualizacji do jednoczesnego zastosowania.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="4d7cd-170">Pomiń lub określ wartość 0, aby użyć wartości domyślnej (1000).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="4d7cd-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="4d7cd-171">-ValidExitCode</span></span>
<span data-ttu-id="4d7cd-172">Prawidłowe kody wyjściowe skryptu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="4d7cd-173">[Domyślnie: 0].</span><span class="sxs-lookup"><span data-stu-id="4d7cd-173">[Default: 0].</span></span>

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

### <span data-ttu-id="4d7cd-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="4d7cd-175">Instaluje aktualizacje systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-175">Installs Windows Updates.</span></span>
<span data-ttu-id="4d7cd-176">Odpowiada pakietowi obsługi administracyjna usługi Windows Update https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="4d7cd-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="4d7cd-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7cd-177">CommonParameters</span></span>
<span data-ttu-id="4d7cd-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7cd-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7cd-179">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d7cd-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7cd-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d7cd-180">INPUTS</span></span>

## <span data-ttu-id="4d7cd-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d7cd-181">OUTPUTS</span></span>

### <span data-ttu-id="4d7cd-182">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="4d7cd-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="4d7cd-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d7cd-183">NOTES</span></span>

<span data-ttu-id="4d7cd-184">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4d7cd-184">ALIASES</span></span>

## <span data-ttu-id="4d7cd-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d7cd-185">RELATED LINKS</span></span>

