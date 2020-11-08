---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225558"
---
# <span data-ttu-id="ef1f5-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-101">New-AzWebApp</span></span>

## <span data-ttu-id="ef1f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1f5-103">Tworzy aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="ef1f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef1f5-104">SYNTAX</span></span>

### <span data-ttu-id="ef1f5-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef1f5-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="ef1f5-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef1f5-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef1f5-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef1f5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ef1f5-108">DESCRIPTION</span></span>
<span data-ttu-id="ef1f5-109">Polecenie cmdlet **New-AzWebApp** umożliwia utworzenie aplikacji sieci Web platformy Azure w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="ef1f5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef1f5-110">EXAMPLES</span></span>

### <span data-ttu-id="ef1f5-111">Przykład 1: Tworzenie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="ef1f5-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="ef1f5-112">To polecenie tworzy aplikację Azure Web App o nazwie ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-Zachodnia w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="ef1f5-113">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="ef1f5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef1f5-114">PARAMETERS</span></span>

### <span data-ttu-id="ef1f5-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef1f5-115">-AppServicePlan</span></span>
<span data-ttu-id="ef1f5-116">Nazwa planu usługi App Service lub identyfikator planu usługi App Service. Jeśli plan usługi aplikacji i App Service jest w różnych grupach zasobów, użyj identyfikatora zamiast nazwy.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="ef1f5-117">Identyfikator planu usługi App Service można pobrać, używając: $asp = Get-AzAppServicePlan-resourceName myRG-Name MyWebapp $asp. ID zwraca identyfikator planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="ef1f5-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="ef1f5-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="ef1f5-119">Ustawienia aplikacji zastępuje obiekt HashTable</span><span class="sxs-lookup"><span data-stu-id="ef1f5-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="ef1f5-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="ef1f5-120">-AseName</span></span>
<span data-ttu-id="ef1f5-121">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="ef1f5-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="ef1f5-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1f5-122">-AseResourceGroupName</span></span>
<span data-ttu-id="ef1f5-123">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="ef1f5-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="ef1f5-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef1f5-124">-AsJob</span></span>
<span data-ttu-id="ef1f5-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ef1f5-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef1f5-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ef1f5-126">-ContainerImageName</span></span>
<span data-ttu-id="ef1f5-127">Nazwa obrazu kontenera i znacznik opcjonalny, na przykład (Image: tag)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="ef1f5-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ef1f5-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ef1f5-129">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="ef1f5-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="ef1f5-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ef1f5-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ef1f5-131">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="ef1f5-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="ef1f5-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ef1f5-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="ef1f5-133">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="ef1f5-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="ef1f5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1f5-134">-DefaultProfile</span></span>
<span data-ttu-id="ef1f5-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef1f5-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ef1f5-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ef1f5-137">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="ef1f5-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ef1f5-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="ef1f5-138">-GitRepositoryPath</span></span>
<span data-ttu-id="ef1f5-139">Ścieżka do repozytorium GitHub zawierającego aplikację sieci Web do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="ef1f5-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="ef1f5-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="ef1f5-141">Ignorowanie opcji niestandardowych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="ef1f5-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="ef1f5-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="ef1f5-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="ef1f5-143">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="ef1f5-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="ef1f5-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ef1f5-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="ef1f5-145">Uwzględnij źródłowe gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="ef1f5-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="ef1f5-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ef1f5-146">-Location</span></span>
<span data-ttu-id="ef1f5-147">Pozycję</span><span class="sxs-lookup"><span data-stu-id="ef1f5-147">Location</span></span>

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

### <span data-ttu-id="ef1f5-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-148">-Name</span></span>
<span data-ttu-id="ef1f5-149">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="ef1f5-149">WebApp Name</span></span>

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

### <span data-ttu-id="ef1f5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1f5-150">-ResourceGroupName</span></span>
<span data-ttu-id="ef1f5-151">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ef1f5-151">Resource Group Name</span></span>

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

### <span data-ttu-id="ef1f5-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-152">-SourceWebApp</span></span>
<span data-ttu-id="ef1f5-153">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="ef1f5-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="ef1f5-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ef1f5-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="ef1f5-155">Identyfikator zasobu istniejącego profilu Menedżera ruchu</span><span class="sxs-lookup"><span data-stu-id="ef1f5-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="ef1f5-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef1f5-156">-Confirm</span></span>
<span data-ttu-id="ef1f5-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1f5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1f5-158">-WhatIf</span></span>
<span data-ttu-id="ef1f5-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef1f5-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1f5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1f5-161">CommonParameters</span></span>
<span data-ttu-id="ef1f5-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1f5-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1f5-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1f5-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef1f5-164">INPUTS</span></span>

### <span data-ttu-id="ef1f5-165">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="ef1f5-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ef1f5-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef1f5-166">OUTPUTS</span></span>

### <span data-ttu-id="ef1f5-167">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="ef1f5-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ef1f5-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef1f5-168">NOTES</span></span>

## <span data-ttu-id="ef1f5-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef1f5-169">RELATED LINKS</span></span>

[<span data-ttu-id="ef1f5-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ef1f5-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ef1f5-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ef1f5-173">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ef1f5-174">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ef1f5-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


