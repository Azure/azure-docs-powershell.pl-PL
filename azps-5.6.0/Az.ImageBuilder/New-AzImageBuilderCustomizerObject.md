---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 97e59efcc20f8ce025b2e90285ef051edc8272dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013057"
---
# <span data-ttu-id="16517-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="16517-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="16517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16517-102">SYNOPSIS</span></span>
<span data-ttu-id="16517-103">W tym artykule opisano jednostkę dostosowywania obrazu</span><span class="sxs-lookup"><span data-stu-id="16517-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="16517-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16517-104">SYNTAX</span></span>

### <span data-ttu-id="16517-105">ShellCustomizer (domyślna)</span><span class="sxs-lookup"><span data-stu-id="16517-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="16517-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="16517-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="16517-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="16517-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="16517-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="16517-110">DESCRIPTION</span></span>
<span data-ttu-id="16517-111">W tym artykule opisano jednostkę dostosowywania obrazu</span><span class="sxs-lookup"><span data-stu-id="16517-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="16517-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16517-112">EXAMPLES</span></span>

### <span data-ttu-id="16517-113">Przykład 1. Tworzenie dostosowywania aktualizacji systemu Windows</span><span class="sxs-lookup"><span data-stu-id="16517-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="16517-114">To polecenie tworzy dostosowywanie aktualizacji systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="16517-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="16517-115">Przykład 2. Tworzenie dostosowywanie pliku</span><span class="sxs-lookup"><span data-stu-id="16517-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="16517-116">To polecenie tworzy dostosowywanie pliku.</span><span class="sxs-lookup"><span data-stu-id="16517-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="16517-117">Przykład 3. Tworzenie dostosowywanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="16517-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="16517-118">To polecenie tworzy dostosowywanie programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16517-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="16517-119">Przykład 4. Tworzenie dostosowania ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="16517-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="16517-120">To polecenie powoduje utworzenie dostosowania ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="16517-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="16517-121">Przykład 5. Tworzenie dostosowywacza powłoki</span><span class="sxs-lookup"><span data-stu-id="16517-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="16517-122">To polecenie tworzy dostosowywanie powłoki.</span><span class="sxs-lookup"><span data-stu-id="16517-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="16517-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16517-123">PARAMETERS</span></span>

### <span data-ttu-id="16517-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="16517-124">-CustomizerName</span></span>
<span data-ttu-id="16517-125">Przyjazna nazwa w celu zapewnienia kontekstu na temat tego kroku dostosowywania.</span><span class="sxs-lookup"><span data-stu-id="16517-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="16517-126">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="16517-126">-Destination</span></span>
<span data-ttu-id="16517-127">Ścieżka bezwzględna do pliku (z już utworzoną strukturą katalogów zagnieżdżonych), do którego plik (ze sourceUri) zostanie przekazany w maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="16517-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="16517-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-128">-FileCustomizer</span></span>
<span data-ttu-id="16517-129">Przesyła pliki do maszyn wirtualnych (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="16517-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="16517-130">Odpowiada inicjatorowi plików Packer.</span><span class="sxs-lookup"><span data-stu-id="16517-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="16517-131">— Filtr</span><span class="sxs-lookup"><span data-stu-id="16517-131">-Filter</span></span>
<span data-ttu-id="16517-132">Tablica filtrów do wybierania aktualizacji do zastosowania.</span><span class="sxs-lookup"><span data-stu-id="16517-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="16517-133">Pomiń lub określ pustą tablicę, aby użyć domyślnej (bez filtru).</span><span class="sxs-lookup"><span data-stu-id="16517-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="16517-134">Przykłady i szczegółowy opis tego pola można znaleźć w powyższym linku.</span><span class="sxs-lookup"><span data-stu-id="16517-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="16517-135">— W tekście</span><span class="sxs-lookup"><span data-stu-id="16517-135">-Inline</span></span>
<span data-ttu-id="16517-136">Tablica poleceń powłoki do wykonania.</span><span class="sxs-lookup"><span data-stu-id="16517-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="16517-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="16517-138">Uruchamia określony program PowerShell na maszyny wirtualnej (Windows).</span><span class="sxs-lookup"><span data-stu-id="16517-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="16517-139">Odpowiada inicjatorowi programu PowerShell packer.</span><span class="sxs-lookup"><span data-stu-id="16517-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="16517-140">Można określić dokładnie jeden z "scriptUri" lub "inline".</span><span class="sxs-lookup"><span data-stu-id="16517-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="16517-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="16517-141">-RestartCheckCommand</span></span>
<span data-ttu-id="16517-142">Polecenie sprawdzania, czy ponowne uruchomienie zakończyło się pomyślnie [Domyślne: ''].</span><span class="sxs-lookup"><span data-stu-id="16517-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="16517-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="16517-143">-RestartCommand</span></span>
<span data-ttu-id="16517-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="16517-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="16517-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-145">-RestartCustomizer</span></span>
<span data-ttu-id="16517-146">Ponowne uruchomienie maszyny wirtualnej i oczekiwanie na jej powrót do trybu online (Windows).</span><span class="sxs-lookup"><span data-stu-id="16517-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="16517-147">Odpowiada funkcji inicjowania obsługi po ponownym uruchomieniu programu Windows Packer.</span><span class="sxs-lookup"><span data-stu-id="16517-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="16517-148">- RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="16517-148">-RestartTimeout</span></span>
<span data-ttu-id="16517-149">Ponownie uruchom limit czasu określony jako ciąg wielkości i jednostki, na przykład '5m' (5 minut) lub '2h' (2 godziny) [Domyślna: '5m'].</span><span class="sxs-lookup"><span data-stu-id="16517-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="16517-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="16517-150">-RunElevated</span></span>
<span data-ttu-id="16517-151">Jeśli zostanie określona, skrypt programu PowerShell zostanie uruchomiony z podwyższonym poziomem uprawnień.</span><span class="sxs-lookup"><span data-stu-id="16517-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="16517-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="16517-152">-ScriptUri</span></span>
<span data-ttu-id="16517-153">URI skryptu powłoki, który ma zostać uruchomiony w celu dostosowywania.</span><span class="sxs-lookup"><span data-stu-id="16517-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="16517-154">Może to być link github, URI SAS dla usługi Azure Storage itp.</span><span class="sxs-lookup"><span data-stu-id="16517-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="16517-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="16517-155">-SearchCriterion</span></span>
<span data-ttu-id="16517-156">Kryteria wyszukiwania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="16517-156">Criteria to search updates.</span></span>
<span data-ttu-id="16517-157">Pomiń lub określ pusty ciąg, aby użyć wartości domyślnej (wyszukaj wszystko).</span><span class="sxs-lookup"><span data-stu-id="16517-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="16517-158">Przykłady i szczegółowy opis tego pola można znaleźć w powyższym linku.</span><span class="sxs-lookup"><span data-stu-id="16517-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="16517-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="16517-159">-Sha256Checksum</span></span>
<span data-ttu-id="16517-160">Sha256 checksum of the shell script provided in the scriptUri field.</span><span class="sxs-lookup"><span data-stu-id="16517-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="16517-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-161">-ShellCustomizer</span></span>
<span data-ttu-id="16517-162">Uruchamia skrypt powłoki w fazie dostosowywania (Linux).</span><span class="sxs-lookup"><span data-stu-id="16517-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="16517-163">Odpowiada inicjatorowi powłoki Packer.</span><span class="sxs-lookup"><span data-stu-id="16517-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="16517-164">Można określić dokładnie jeden z "scriptUri" lub "inline".</span><span class="sxs-lookup"><span data-stu-id="16517-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="16517-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="16517-165">-SourceUri</span></span>
<span data-ttu-id="16517-166">Identyfikator URI pliku, który ma zostać przekazany w celu dostosowywania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="16517-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="16517-167">Może to być link github, URI SAS dla usługi Azure Storage itp.</span><span class="sxs-lookup"><span data-stu-id="16517-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="16517-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="16517-168">-UpdateLimit</span></span>
<span data-ttu-id="16517-169">Maksymalna liczba aktualizacji, które mają być stosowane jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="16517-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="16517-170">Pomiń lub określ wartość 0, aby użyć wartości domyślnej (1000).</span><span class="sxs-lookup"><span data-stu-id="16517-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="16517-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="16517-171">-ValidExitCode</span></span>
<span data-ttu-id="16517-172">Prawidłowe kody wyjścia dla skryptu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16517-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="16517-173">[Domyślne: 0].</span><span class="sxs-lookup"><span data-stu-id="16517-173">[Default: 0].</span></span>

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

### <span data-ttu-id="16517-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="16517-175">Instaluje aktualizacje systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="16517-175">Installs Windows Updates.</span></span>
<span data-ttu-id="16517-176">Odpowiada funkcji obsługi administracyjnej usługi Windows Update Packer https://github.com/rgl/packer-provisioner-windows-update) (.</span><span class="sxs-lookup"><span data-stu-id="16517-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="16517-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16517-177">CommonParameters</span></span>
<span data-ttu-id="16517-178">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16517-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16517-179">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16517-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16517-180">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16517-180">INPUTS</span></span>

## <span data-ttu-id="16517-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16517-181">OUTPUTS</span></span>

### <span data-ttu-id="16517-182">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="16517-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="16517-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16517-183">NOTES</span></span>

<span data-ttu-id="16517-184">ALIASY</span><span class="sxs-lookup"><span data-stu-id="16517-184">ALIASES</span></span>

## <span data-ttu-id="16517-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16517-185">RELATED LINKS</span></span>

