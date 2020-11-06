---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524205"
---
# <span data-ttu-id="1f7b8-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="1f7b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7b8-103">Tworzy aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f7b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f7b8-104">SYNTAX</span></span>

### <span data-ttu-id="1f7b8-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f7b8-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f7b8-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="1f7b8-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f7b8-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f7b8-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f7b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1f7b8-108">DESCRIPTION</span></span>
<span data-ttu-id="1f7b8-109">Polecenie cmdlet **New-AzureRmWebApp** umożliwia utworzenie aplikacji sieci Web platformy Azure w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="1f7b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f7b8-110">EXAMPLES</span></span>

### <span data-ttu-id="1f7b8-111">Przykład 1: Tworzenie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="1f7b8-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="1f7b8-112">To polecenie tworzy aplikację Azure Web App o nazwie ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-Zachodnia w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="1f7b8-113">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="1f7b8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f7b8-114">PARAMETERS</span></span>

### <span data-ttu-id="1f7b8-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1f7b8-115">-AppServicePlan</span></span>
<span data-ttu-id="1f7b8-116">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="1f7b8-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="1f7b8-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="1f7b8-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="1f7b8-118">Ustawienia aplikacji zastępuje obiekt HashTable</span><span class="sxs-lookup"><span data-stu-id="1f7b8-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="1f7b8-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-119">-AseName</span></span>
<span data-ttu-id="1f7b8-120">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="1f7b8-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="1f7b8-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-121">-AseResourceGroupName</span></span>
<span data-ttu-id="1f7b8-122">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="1f7b8-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="1f7b8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f7b8-123">-AsJob</span></span>
<span data-ttu-id="1f7b8-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f7b8-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f7b8-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-125">-ContainerImageName</span></span>
<span data-ttu-id="1f7b8-126">Nazwa obrazu kontenera i znacznik opcjonalny, na przykład (Image: tag)</span><span class="sxs-lookup"><span data-stu-id="1f7b8-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="1f7b8-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="1f7b8-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="1f7b8-128">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="1f7b8-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="1f7b8-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="1f7b8-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="1f7b8-130">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="1f7b8-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="1f7b8-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="1f7b8-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="1f7b8-132">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="1f7b8-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="1f7b8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7b8-133">-DefaultProfile</span></span>
<span data-ttu-id="1f7b8-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7b8-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="1f7b8-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="1f7b8-136">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="1f7b8-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="1f7b8-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="1f7b8-137">-GitRepositoryPath</span></span>
<span data-ttu-id="1f7b8-138">Ścieżka do repozytorium GitHub containign aplikacji sieci Web do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="1f7b8-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="1f7b8-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="1f7b8-140">Ignorowanie opcji niestandardowych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="1f7b8-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="1f7b8-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="1f7b8-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="1f7b8-142">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="1f7b8-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="1f7b8-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="1f7b8-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="1f7b8-144">Uwzględnij źródłowe gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f7b8-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="1f7b8-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1f7b8-145">-Location</span></span>
<span data-ttu-id="1f7b8-146">Pozycję</span><span class="sxs-lookup"><span data-stu-id="1f7b8-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7b8-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f7b8-147">-Name</span></span>
<span data-ttu-id="1f7b8-148">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f7b8-148">WebApp Name</span></span>

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

### <span data-ttu-id="1f7b8-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-149">-ResourceGroupName</span></span>
<span data-ttu-id="1f7b8-150">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1f7b8-150">Resource Group Name</span></span>

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

### <span data-ttu-id="1f7b8-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-151">-SourceWebApp</span></span>
<span data-ttu-id="1f7b8-152">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="1f7b8-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="1f7b8-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f7b8-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="1f7b8-154">Identyfikator zasobu istniejącego profilu Menedżera ruchu</span><span class="sxs-lookup"><span data-stu-id="1f7b8-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="1f7b8-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f7b8-155">-Confirm</span></span>
<span data-ttu-id="1f7b8-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7b8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7b8-157">-WhatIf</span></span>
<span data-ttu-id="1f7b8-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f7b8-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7b8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7b8-160">CommonParameters</span></span>
<span data-ttu-id="1f7b8-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7b8-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7b8-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7b8-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f7b8-163">INPUTS</span></span>

### <span data-ttu-id="1f7b8-164">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="1f7b8-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="1f7b8-165">Parametry: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1f7b8-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="1f7b8-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f7b8-166">OUTPUTS</span></span>

### <span data-ttu-id="1f7b8-167">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="1f7b8-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="1f7b8-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f7b8-168">NOTES</span></span>

## <span data-ttu-id="1f7b8-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f7b8-169">RELATED LINKS</span></span>

[<span data-ttu-id="1f7b8-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1f7b8-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1f7b8-172">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1f7b8-173">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1f7b8-174">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1f7b8-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


