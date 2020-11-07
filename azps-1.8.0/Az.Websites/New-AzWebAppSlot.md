---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707291"
---
# <span data-ttu-id="1b2ad-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="1b2ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2ad-103">Tworzy miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1b2ad-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="1b2ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b2ad-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b2ad-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2ad-106">Polecenie cmdlet **New-AzWebAppSlot** tworzy miejsce w usłudze Azure Web App w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="1b2ad-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="1b2ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b2ad-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2ad-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b2ad-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="1b2ad-109">To polecenie tworzy gniazdo o nazwie Slot001 w obszarze istniejących nazw aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-zachód w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="1b2ad-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="1b2ad-110">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1b2ad-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="1b2ad-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b2ad-111">PARAMETERS</span></span>

### <span data-ttu-id="1b2ad-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1b2ad-112">-AppServicePlan</span></span>
<span data-ttu-id="1b2ad-113">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="1b2ad-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="1b2ad-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="1b2ad-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="1b2ad-115">Ustawienia aplikacji zastępuje obiekt Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b2ad-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="1b2ad-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="1b2ad-116">-AseName</span></span>
<span data-ttu-id="1b2ad-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="1b2ad-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="1b2ad-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2ad-118">-AseResourceGroupName</span></span>
<span data-ttu-id="1b2ad-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="1b2ad-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="1b2ad-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b2ad-120">-AsJob</span></span>
<span data-ttu-id="1b2ad-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1b2ad-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b2ad-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="1b2ad-122">-ContainerImageName</span></span>
<span data-ttu-id="1b2ad-123">Nazwa obrazu kontenera i znacznik opcjonalny, na przykład (Image: tag)</span><span class="sxs-lookup"><span data-stu-id="1b2ad-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="1b2ad-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="1b2ad-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="1b2ad-125">Hasło rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="1b2ad-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="1b2ad-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="1b2ad-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="1b2ad-127">Adres URL serwera rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="1b2ad-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="1b2ad-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="1b2ad-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="1b2ad-129">Nazwa użytkownika rejestru kontenera prywatnego</span><span class="sxs-lookup"><span data-stu-id="1b2ad-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="1b2ad-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2ad-130">-DefaultProfile</span></span>
<span data-ttu-id="1b2ad-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2ad-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2ad-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="1b2ad-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="1b2ad-133">Włączanie/wyłączanie elementu webhook ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="1b2ad-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="1b2ad-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="1b2ad-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="1b2ad-135">Ignoruj niestandardowe opcje nazw hostów</span><span class="sxs-lookup"><span data-stu-id="1b2ad-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="1b2ad-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="1b2ad-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="1b2ad-137">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="1b2ad-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="1b2ad-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b2ad-138">-Name</span></span>
<span data-ttu-id="1b2ad-139">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b2ad-139">Webapp Name</span></span>

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

### <span data-ttu-id="1b2ad-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2ad-140">-ResourceGroupName</span></span>
<span data-ttu-id="1b2ad-141">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1b2ad-141">Resource Group Name</span></span>

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

### <span data-ttu-id="1b2ad-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-142">-Slot</span></span>
<span data-ttu-id="1b2ad-143">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b2ad-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="1b2ad-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="1b2ad-144">-SourceWebApp</span></span>
<span data-ttu-id="1b2ad-145">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b2ad-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="1b2ad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2ad-146">CommonParameters</span></span>
<span data-ttu-id="1b2ad-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2ad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2ad-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2ad-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2ad-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b2ad-149">INPUTS</span></span>

### <span data-ttu-id="1b2ad-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1b2ad-150">System.String</span></span>

### <span data-ttu-id="1b2ad-151">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b2ad-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b2ad-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b2ad-152">OUTPUTS</span></span>

### <span data-ttu-id="1b2ad-153">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b2ad-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b2ad-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b2ad-154">NOTES</span></span>

## <span data-ttu-id="1b2ad-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b2ad-155">RELATED LINKS</span></span>

[<span data-ttu-id="1b2ad-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1b2ad-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="1b2ad-158">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="1b2ad-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="1b2ad-160">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="1b2ad-161">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b2ad-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="1b2ad-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1b2ad-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="1b2ad-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b2ad-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
