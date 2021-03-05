---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 283b3dd7ec57150d1c93a6e01a85251ed94fbdf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973057"
---
# <span data-ttu-id="5c8bb-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="5c8bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8bb-103">Tworzy miejsce na aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="5c8bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c8bb-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c8bb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c8bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5c8bb-106">Polecenie **cmdlet New-AzWebAppSlot** tworzy slot aplikacji Azure Web App w danej grupie zasobów, która korzysta z określonego planu usługi aplikacji i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="5c8bb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c8bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5c8bb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c8bb-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="5c8bb-109">To polecenie tworzy slot o nazwie Slot001 pod istniejącymi nazwami aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-WestUS w centrum danych Zachód USA.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="5c8bb-110">To polecenie korzysta z istniejącego planu usługi aplikacji o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="5c8bb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c8bb-111">PARAMETERS</span></span>

### <span data-ttu-id="5c8bb-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5c8bb-112">-AppServicePlan</span></span>
<span data-ttu-id="5c8bb-113">Nazwa planu serwisowego aplikacji lub identyfikator planu usługi aplikacji. Jeśli plan usługi miejsca i aplikacji znajduje się w różnych grupach zasobów, użyj identyfikatora zamiast nazwy.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="5c8bb-114">Identyfikator planu usługi aplikacji można pobrać przy użyciu: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id zwraca identyfikator planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="5c8bb-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="5c8bb-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="5c8bb-116">Ustawienia aplikacji zastępują skróty</span><span class="sxs-lookup"><span data-stu-id="5c8bb-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="5c8bb-117">-AseName</span></span>
<span data-ttu-id="5c8bb-118">Nazwa środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c8bb-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8bb-119">-AseResourceGroupName</span></span>
<span data-ttu-id="5c8bb-120">Nazwa grupy zasobów środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c8bb-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5c8bb-121">-AsJob</span></span>
<span data-ttu-id="5c8bb-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5c8bb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c8bb-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="5c8bb-123">-ContainerImageName</span></span>
<span data-ttu-id="5c8bb-124">Container Image Name and optional tag, example (image:tag)</span><span class="sxs-lookup"><span data-stu-id="5c8bb-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="5c8bb-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="5c8bb-126">Hasło do rejestru dla kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="5c8bb-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="5c8bb-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="5c8bb-128">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="5c8bb-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="5c8bb-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="5c8bb-130">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="5c8bb-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8bb-131">-DefaultProfile</span></span>
<span data-ttu-id="5c8bb-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c8bb-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="5c8bb-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="5c8bb-134">Włączenie/wyłączenie kontenera ciągłego wdrożenia sieci Web</span><span class="sxs-lookup"><span data-stu-id="5c8bb-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="5c8bb-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="5c8bb-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="5c8bb-136">Opcja Ignoruj niestandardowe nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="5c8bb-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="5c8bb-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="5c8bb-138">Opcja Ignoruj kontrolkę źródła</span><span class="sxs-lookup"><span data-stu-id="5c8bb-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5c8bb-139">-Name</span></span>
<span data-ttu-id="5c8bb-140">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="5c8bb-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8bb-141">-ResourceGroupName</span></span>
<span data-ttu-id="5c8bb-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5c8bb-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-143">— Slot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-143">-Slot</span></span>
<span data-ttu-id="5c8bb-144">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="5c8bb-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="5c8bb-145">-SourceWebApp</span></span>
<span data-ttu-id="5c8bb-146">Obiekt Source WebApp</span><span class="sxs-lookup"><span data-stu-id="5c8bb-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c8bb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8bb-147">CommonParameters</span></span>
<span data-ttu-id="5c8bb-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8bb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8bb-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c8bb-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8bb-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c8bb-150">INPUTS</span></span>

### <span data-ttu-id="5c8bb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="5c8bb-151">System.String</span></span>

### <span data-ttu-id="5c8bb-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5c8bb-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5c8bb-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c8bb-153">OUTPUTS</span></span>

### <span data-ttu-id="5c8bb-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5c8bb-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5c8bb-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c8bb-155">NOTES</span></span>

## <span data-ttu-id="5c8bb-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c8bb-156">RELATED LINKS</span></span>

[<span data-ttu-id="5c8bb-157">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="5c8bb-158">Remove-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="5c8bb-159">Restart-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="5c8bb-160">Set-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="5c8bb-161">Start-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="5c8bb-162">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="5c8bb-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="5c8bb-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5c8bb-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="5c8bb-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c8bb-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
