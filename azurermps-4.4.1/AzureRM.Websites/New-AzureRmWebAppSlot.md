---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553728"
---
# <span data-ttu-id="4d3ac-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="4d3ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3ac-103">Tworzy miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4d3ac-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d3ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d3ac-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d3ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d3ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4d3ac-106">Polecenie cmdlet **New-AzureRmWebAppSlot** tworzy miejsce w usłudze Azure Web App w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="4d3ac-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="4d3ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d3ac-107">EXAMPLES</span></span>

### <span data-ttu-id="4d3ac-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d3ac-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="4d3ac-109">To polecenie tworzy gniazdo o nazwie Slot001 w obszarze istniejących nazw aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-zachód w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="4d3ac-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="4d3ac-110">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4d3ac-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="4d3ac-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d3ac-111">PARAMETERS</span></span>

### <span data-ttu-id="4d3ac-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d3ac-112">-AppServicePlan</span></span>
<span data-ttu-id="4d3ac-113">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="4d3ac-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="4d3ac-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="4d3ac-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="4d3ac-115">Ustawienia aplikacji zastępuje obiekt Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d3ac-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="4d3ac-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="4d3ac-116">-AseName</span></span>
<span data-ttu-id="4d3ac-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="4d3ac-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="4d3ac-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3ac-118">-AseResourceGroupName</span></span>
<span data-ttu-id="4d3ac-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="4d3ac-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="4d3ac-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="4d3ac-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="4d3ac-121">Ignoruj niestandardowe opcje nazw hostów</span><span class="sxs-lookup"><span data-stu-id="4d3ac-121">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="4d3ac-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="4d3ac-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="4d3ac-123">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="4d3ac-123">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="4d3ac-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d3ac-124">-Name</span></span>
<span data-ttu-id="4d3ac-125">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="4d3ac-125">Webapp Name</span></span>

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

### <span data-ttu-id="4d3ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d3ac-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4d3ac-127">Resource Group Name</span></span>

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

### <span data-ttu-id="4d3ac-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-128">-Slot</span></span>
<span data-ttu-id="4d3ac-129">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="4d3ac-129">Webapp Slot Name</span></span>

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

### <span data-ttu-id="4d3ac-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="4d3ac-130">-SourceWebApp</span></span>
<span data-ttu-id="4d3ac-131">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="4d3ac-131">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3ac-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3ac-132">-DefaultProfile</span></span>
<span data-ttu-id="4d3ac-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3ac-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d3ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3ac-134">CommonParameters</span></span>
<span data-ttu-id="4d3ac-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3ac-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d3ac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3ac-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d3ac-137">INPUTS</span></span>

### <span data-ttu-id="4d3ac-138">Klienta</span><span class="sxs-lookup"><span data-stu-id="4d3ac-138">Site</span></span>
<span data-ttu-id="4d3ac-139">Parametr "SourceWebApp" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="4d3ac-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4d3ac-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d3ac-140">OUTPUTS</span></span>

## <span data-ttu-id="4d3ac-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d3ac-141">NOTES</span></span>

## <span data-ttu-id="4d3ac-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d3ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="4d3ac-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="4d3ac-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="4d3ac-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="4d3ac-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="4d3ac-147">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="4d3ac-148">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3ac-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="4d3ac-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d3ac-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="4d3ac-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4d3ac-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
