---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188699"
---
# <span data-ttu-id="e8471-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-101">New-AzWebApp</span></span>

## <span data-ttu-id="e8471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8471-102">SYNOPSIS</span></span>
<span data-ttu-id="e8471-103">Tworzy aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e8471-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="e8471-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8471-104">SYNTAX</span></span>

### <span data-ttu-id="e8471-105">SimpleParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e8471-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8471-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="e8471-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8471-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8471-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8471-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8471-108">DESCRIPTION</span></span>
<span data-ttu-id="e8471-109">Polecenie **cmdlet New-AzWebApp** tworzy aplikację Azure Web App w danej grupie zasobów, która korzysta z określonego planu usługi aplikacji i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="e8471-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="e8471-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8471-110">EXAMPLES</span></span>

### <span data-ttu-id="e8471-111">Przykład 1. Tworzenie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="e8471-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="e8471-112">To polecenie tworzy aplikację Azure Web App o nazwie ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-WestUS w centrum danych Zachód USA.</span><span class="sxs-lookup"><span data-stu-id="e8471-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="e8471-113">To polecenie korzysta z istniejącego planu usługi aplikacji o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e8471-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="e8471-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8471-114">PARAMETERS</span></span>

### <span data-ttu-id="e8471-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e8471-115">-AppServicePlan</span></span>
<span data-ttu-id="e8471-116">Nazwa planu serwisowego aplikacji lub identyfikator planu usługi aplikacji. Jeśli plan usługi WebApp i aplikacji należy do różnych grup zasobów, użyj identyfikatora zamiast nazwy.</span><span class="sxs-lookup"><span data-stu-id="e8471-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="e8471-117">Identyfikator planu usługi aplikacji można pobrać za pomocą: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id zwraca identyfikator planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8471-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="e8471-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="e8471-119">Ustawienia aplikacji zastępują tabelę Skróty</span><span class="sxs-lookup"><span data-stu-id="e8471-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="e8471-120">-AseName</span></span>
<span data-ttu-id="e8471-121">Nazwa środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8471-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8471-122">-AseResourceGroupName</span></span>
<span data-ttu-id="e8471-123">Nazwa grupy zasobów środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8471-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e8471-124">-AsJob</span></span>
<span data-ttu-id="e8471-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e8471-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="e8471-126">-ContainerImageName</span></span>
<span data-ttu-id="e8471-127">Container Image Name and optional tag, example (image:tag)</span><span class="sxs-lookup"><span data-stu-id="e8471-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="e8471-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="e8471-129">Hasło do rejestru dla kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="e8471-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="e8471-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="e8471-131">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="e8471-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="e8471-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="e8471-133">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="e8471-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8471-134">-DefaultProfile</span></span>
<span data-ttu-id="e8471-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8471-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="e8471-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="e8471-137">Włączenie/wyłączenie kontenera ciągłego wdrożenia sieci Web</span><span class="sxs-lookup"><span data-stu-id="e8471-137">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="e8471-138">-GitRepositoryPath</span></span>
<span data-ttu-id="e8471-139">Ścieżka do repozytorium GitHub zawierającego aplikację sieci Web do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e8471-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="e8471-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="e8471-141">Opcja Ignoruj niestandardowe nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="e8471-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="e8471-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="e8471-143">Opcja Ignoruj kontrolkę źródła</span><span class="sxs-lookup"><span data-stu-id="e8471-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e8471-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="e8471-145">Opcja Uwzględnij źródłowe miejsca w aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8471-146">-Location</span></span>
<span data-ttu-id="e8471-147">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8471-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e8471-148">-Name</span></span>
<span data-ttu-id="e8471-149">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8471-150">-ResourceGroupName</span></span>
<span data-ttu-id="e8471-151">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e8471-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-152">-SourceWebApp</span></span>
<span data-ttu-id="e8471-153">Obiekt Source WebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e8471-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="e8471-155">Identyfikator zasobu istniejącego profilu menedżera ruchu</span><span class="sxs-lookup"><span data-stu-id="e8471-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8471-156">-Confirm</span></span>
<span data-ttu-id="e8471-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8471-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8471-158">-WhatIf</span></span>
<span data-ttu-id="e8471-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8471-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8471-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e8471-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8471-161">CommonParameters</span></span>
<span data-ttu-id="e8471-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8471-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8471-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8471-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8471-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8471-164">INPUTS</span></span>

### <span data-ttu-id="e8471-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e8471-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e8471-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8471-166">OUTPUTS</span></span>

### <span data-ttu-id="e8471-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e8471-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e8471-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8471-168">NOTES</span></span>

## <span data-ttu-id="e8471-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8471-169">RELATED LINKS</span></span>

[<span data-ttu-id="e8471-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e8471-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e8471-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e8471-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e8471-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e8471-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


