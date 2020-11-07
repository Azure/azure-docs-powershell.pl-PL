---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 8120b22f02d137ff261b1b4e345b917d6ae82a5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707308"
---
# <span data-ttu-id="0c6da-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-101">New-AzWebApp</span></span>

## <span data-ttu-id="0c6da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c6da-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6da-103">Tworzy aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0c6da-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="0c6da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c6da-104">SYNTAX</span></span>

### <span data-ttu-id="0c6da-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c6da-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6da-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="0c6da-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6da-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c6da-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0c6da-108">DESCRIPTION</span></span>
<span data-ttu-id="0c6da-109">Polecenie cmdlet **New-AzWebApp** umożliwia utworzenie aplikacji sieci Web platformy Azure w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="0c6da-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="0c6da-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c6da-110">EXAMPLES</span></span>

### <span data-ttu-id="0c6da-111">Przykład 1: Tworzenie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="0c6da-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="0c6da-112">To polecenie tworzy aplikację Azure Web App o nazwie ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-Zachodnia w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="0c6da-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="0c6da-113">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0c6da-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="0c6da-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c6da-114">PARAMETERS</span></span>

### <span data-ttu-id="0c6da-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c6da-115">-AppServicePlan</span></span>
<span data-ttu-id="0c6da-116">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="0c6da-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="0c6da-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="0c6da-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="0c6da-118">Ustawienia aplikacji zastępuje obiekt HashTable</span><span class="sxs-lookup"><span data-stu-id="0c6da-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="0c6da-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="0c6da-119">-AseName</span></span>
<span data-ttu-id="0c6da-120">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="0c6da-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="0c6da-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6da-121">-AseResourceGroupName</span></span>
<span data-ttu-id="0c6da-122">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="0c6da-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="0c6da-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c6da-123">-AsJob</span></span>
<span data-ttu-id="0c6da-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c6da-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c6da-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="0c6da-125">-ContainerImageName</span></span>
<span data-ttu-id="0c6da-126">Nazwa obrazu kontenera i znacznik opcjonalny, na przykład (Image: tag)</span><span class="sxs-lookup"><span data-stu-id="0c6da-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="0c6da-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="0c6da-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="0c6da-128">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="0c6da-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="0c6da-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="0c6da-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="0c6da-130">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="0c6da-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="0c6da-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="0c6da-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="0c6da-132">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="0c6da-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="0c6da-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6da-133">-DefaultProfile</span></span>
<span data-ttu-id="0c6da-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6da-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c6da-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="0c6da-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="0c6da-136">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="0c6da-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="0c6da-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="0c6da-137">-GitRepositoryPath</span></span>
<span data-ttu-id="0c6da-138">Ścieżka do repozytorium GitHub zawierającego aplikację sieci Web do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0c6da-138">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="0c6da-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="0c6da-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="0c6da-140">Ignorowanie opcji niestandardowych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="0c6da-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="0c6da-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="0c6da-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="0c6da-142">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="0c6da-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="0c6da-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0c6da-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="0c6da-144">Uwzględnij źródłowe gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="0c6da-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="0c6da-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0c6da-145">-Location</span></span>
<span data-ttu-id="0c6da-146">Pozycję</span><span class="sxs-lookup"><span data-stu-id="0c6da-146">Location</span></span>

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

### <span data-ttu-id="0c6da-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c6da-147">-Name</span></span>
<span data-ttu-id="0c6da-148">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="0c6da-148">WebApp Name</span></span>

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

### <span data-ttu-id="0c6da-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6da-149">-ResourceGroupName</span></span>
<span data-ttu-id="0c6da-150">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c6da-150">Resource Group Name</span></span>

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

### <span data-ttu-id="0c6da-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-151">-SourceWebApp</span></span>
<span data-ttu-id="0c6da-152">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="0c6da-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="0c6da-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c6da-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="0c6da-154">Identyfikator zasobu istniejącego profilu Menedżera ruchu</span><span class="sxs-lookup"><span data-stu-id="0c6da-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="0c6da-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c6da-155">-Confirm</span></span>
<span data-ttu-id="0c6da-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6da-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6da-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6da-157">-WhatIf</span></span>
<span data-ttu-id="0c6da-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6da-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c6da-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c6da-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6da-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6da-160">CommonParameters</span></span>
<span data-ttu-id="0c6da-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6da-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6da-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6da-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6da-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c6da-163">INPUTS</span></span>

### <span data-ttu-id="0c6da-164">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="0c6da-164">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0c6da-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c6da-165">OUTPUTS</span></span>

### <span data-ttu-id="0c6da-166">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="0c6da-166">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0c6da-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c6da-167">NOTES</span></span>

## <span data-ttu-id="0c6da-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c6da-168">RELATED LINKS</span></span>

[<span data-ttu-id="0c6da-169">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-169">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0c6da-170">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-170">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0c6da-171">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-171">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0c6da-172">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-172">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0c6da-173">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c6da-173">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


