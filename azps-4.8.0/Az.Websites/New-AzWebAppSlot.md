---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220976"
---
# <span data-ttu-id="71b76-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="71b76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71b76-102">SYNOPSIS</span></span>
<span data-ttu-id="71b76-103">Tworzy miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="71b76-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="71b76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71b76-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71b76-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71b76-105">DESCRIPTION</span></span>
<span data-ttu-id="71b76-106">Polecenie cmdlet **New-AzWebAppSlot** tworzy miejsce w usłudze Azure Web App w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="71b76-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="71b76-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71b76-107">EXAMPLES</span></span>

### <span data-ttu-id="71b76-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71b76-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="71b76-109">To polecenie tworzy gniazdo o nazwie Slot001 w obszarze istniejących nazw aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-zachód w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="71b76-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="71b76-110">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="71b76-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="71b76-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71b76-111">PARAMETERS</span></span>

### <span data-ttu-id="71b76-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="71b76-112">-AppServicePlan</span></span>
<span data-ttu-id="71b76-113">Nazwa planu usługi App Service lub identyfikator planu usługi App Service. Jeśli plan i usługa App Service nie znajdują się w różnych grupach zasobów, użyj identyfikatora zamiast nazwy.</span><span class="sxs-lookup"><span data-stu-id="71b76-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="71b76-114">Identyfikator planu usługi App Service można pobrać, używając: $asp = Get-AzAppServicePlan-resourceName myRG-Name MyWebapp $asp. ID zwraca identyfikator planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="71b76-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="71b76-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="71b76-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="71b76-116">Ustawienia aplikacji zastępuje obiekt Hashtable</span><span class="sxs-lookup"><span data-stu-id="71b76-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="71b76-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="71b76-117">-AseName</span></span>
<span data-ttu-id="71b76-118">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="71b76-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="71b76-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b76-119">-AseResourceGroupName</span></span>
<span data-ttu-id="71b76-120">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="71b76-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="71b76-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71b76-121">-AsJob</span></span>
<span data-ttu-id="71b76-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="71b76-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71b76-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="71b76-123">-ContainerImageName</span></span>
<span data-ttu-id="71b76-124">Nazwa obrazu kontenera i znacznik opcjonalny, na przykład (Image: tag)</span><span class="sxs-lookup"><span data-stu-id="71b76-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="71b76-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="71b76-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="71b76-126">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="71b76-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="71b76-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="71b76-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="71b76-128">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="71b76-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="71b76-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="71b76-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="71b76-130">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="71b76-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="71b76-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b76-131">-DefaultProfile</span></span>
<span data-ttu-id="71b76-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71b76-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b76-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="71b76-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="71b76-134">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="71b76-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="71b76-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="71b76-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="71b76-136">Ignoruj niestandardowe opcje nazw hostów</span><span class="sxs-lookup"><span data-stu-id="71b76-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="71b76-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="71b76-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="71b76-138">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="71b76-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="71b76-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71b76-139">-Name</span></span>
<span data-ttu-id="71b76-140">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="71b76-140">Webapp Name</span></span>

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

### <span data-ttu-id="71b76-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b76-141">-ResourceGroupName</span></span>
<span data-ttu-id="71b76-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="71b76-142">Resource Group Name</span></span>

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

### <span data-ttu-id="71b76-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="71b76-143">-Slot</span></span>
<span data-ttu-id="71b76-144">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="71b76-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="71b76-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="71b76-145">-SourceWebApp</span></span>
<span data-ttu-id="71b76-146">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="71b76-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="71b76-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b76-147">CommonParameters</span></span>
<span data-ttu-id="71b76-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b76-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b76-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b76-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b76-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b76-150">INPUTS</span></span>

### <span data-ttu-id="71b76-151">System. String</span><span class="sxs-lookup"><span data-stu-id="71b76-151">System.String</span></span>

### <span data-ttu-id="71b76-152">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="71b76-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="71b76-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71b76-153">OUTPUTS</span></span>

### <span data-ttu-id="71b76-154">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="71b76-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="71b76-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71b76-155">NOTES</span></span>

## <span data-ttu-id="71b76-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71b76-156">RELATED LINKS</span></span>

[<span data-ttu-id="71b76-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="71b76-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="71b76-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="71b76-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="71b76-161">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="71b76-162">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71b76-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="71b76-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="71b76-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="71b76-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71b76-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
