---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551947"
---
# <span data-ttu-id="77d12-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="77d12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77d12-102">SYNOPSIS</span></span>
<span data-ttu-id="77d12-103">Tworzy miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="77d12-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77d12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77d12-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77d12-105">DESCRIPTION</span></span>
<span data-ttu-id="77d12-106">Polecenie cmdlet **New-AzureRmWebAppSlot** tworzy miejsce w usłudze Azure Web App w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="77d12-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="77d12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77d12-107">EXAMPLES</span></span>

### <span data-ttu-id="77d12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77d12-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="77d12-109">To polecenie tworzy gniazdo o nazwie Slot001 w obszarze istniejących nazw aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-zachód w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="77d12-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="77d12-110">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="77d12-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="77d12-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77d12-111">PARAMETERS</span></span>

### <span data-ttu-id="77d12-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="77d12-112">-AppServicePlan</span></span>
<span data-ttu-id="77d12-113">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="77d12-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="77d12-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="77d12-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="77d12-115">Ustawienia aplikacji zastępuje obiekt Hashtable</span><span class="sxs-lookup"><span data-stu-id="77d12-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="77d12-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="77d12-116">-AseName</span></span>
<span data-ttu-id="77d12-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="77d12-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="77d12-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d12-118">-AseResourceGroupName</span></span>
<span data-ttu-id="77d12-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="77d12-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="77d12-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77d12-120">-AsJob</span></span>
<span data-ttu-id="77d12-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77d12-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77d12-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="77d12-122">-ContainerImageName</span></span>
<span data-ttu-id="77d12-123">Nazwa obrazu kontenera i znacznik opcjonalny, na przykład (Image: tag)</span><span class="sxs-lookup"><span data-stu-id="77d12-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="77d12-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="77d12-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="77d12-125">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="77d12-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="77d12-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="77d12-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="77d12-127">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="77d12-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="77d12-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="77d12-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="77d12-129">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="77d12-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="77d12-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d12-130">-DefaultProfile</span></span>
<span data-ttu-id="77d12-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77d12-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77d12-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="77d12-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="77d12-133">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="77d12-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="77d12-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="77d12-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="77d12-135">Ignoruj niestandardowe opcje nazw hostów</span><span class="sxs-lookup"><span data-stu-id="77d12-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="77d12-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="77d12-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="77d12-137">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="77d12-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="77d12-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77d12-138">-Name</span></span>
<span data-ttu-id="77d12-139">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="77d12-139">Webapp Name</span></span>

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

### <span data-ttu-id="77d12-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d12-140">-ResourceGroupName</span></span>
<span data-ttu-id="77d12-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="77d12-141">Resource Group Name</span></span>

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

### <span data-ttu-id="77d12-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="77d12-142">-Slot</span></span>
<span data-ttu-id="77d12-143">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="77d12-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="77d12-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="77d12-144">-SourceWebApp</span></span>
<span data-ttu-id="77d12-145">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="77d12-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="77d12-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d12-146">CommonParameters</span></span>
<span data-ttu-id="77d12-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d12-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d12-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d12-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d12-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d12-149">INPUTS</span></span>

### <span data-ttu-id="77d12-150">System. String</span><span class="sxs-lookup"><span data-stu-id="77d12-150">System.String</span></span>

### <span data-ttu-id="77d12-151">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="77d12-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="77d12-152">Parametry: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77d12-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="77d12-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77d12-153">OUTPUTS</span></span>

### <span data-ttu-id="77d12-154">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="77d12-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="77d12-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77d12-155">NOTES</span></span>

## <span data-ttu-id="77d12-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77d12-156">RELATED LINKS</span></span>

[<span data-ttu-id="77d12-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="77d12-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="77d12-159">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="77d12-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="77d12-161">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="77d12-162">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77d12-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="77d12-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="77d12-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="77d12-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="77d12-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
