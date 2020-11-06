---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546296"
---
# <span data-ttu-id="09a15-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09a15-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="09a15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09a15-102">SYNOPSIS</span></span>
<span data-ttu-id="09a15-103">Umożliwia ustawienie planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="09a15-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09a15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09a15-104">SYNTAX</span></span>

### <span data-ttu-id="09a15-105">S1</span><span class="sxs-lookup"><span data-stu-id="09a15-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09a15-106">S2</span><span class="sxs-lookup"><span data-stu-id="09a15-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09a15-107">Opis</span><span class="sxs-lookup"><span data-stu-id="09a15-107">DESCRIPTION</span></span>
<span data-ttu-id="09a15-108">Polecenie cmdlet **Set-AzureRmAppServicePlan** określa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="09a15-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="09a15-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09a15-109">EXAMPLES</span></span>

### <span data-ttu-id="09a15-110">1: modyfikowanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="09a15-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="09a15-111">To polecenie ustawia opcję PerSiteScaling na wartość prawda w planie usługi App Service o nazwie ContosoASP należącego do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="09a15-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="09a15-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09a15-112">PARAMETERS</span></span>

### <span data-ttu-id="09a15-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="09a15-113">-AdminSiteName</span></span>
<span data-ttu-id="09a15-114">Nazwa witryny administracyjnej</span><span class="sxs-lookup"><span data-stu-id="09a15-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09a15-115">-AppServicePlan</span></span>
<span data-ttu-id="09a15-116">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="09a15-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09a15-117">-AsJob</span></span>
<span data-ttu-id="09a15-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="09a15-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09a15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a15-119">-DefaultProfile</span></span>
<span data-ttu-id="09a15-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09a15-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09a15-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09a15-121">-Name</span></span>
<span data-ttu-id="09a15-122">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="09a15-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="09a15-123">-NumberofWorkers</span></span>
<span data-ttu-id="09a15-124">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="09a15-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="09a15-125">-PerSiteScaling</span></span>
<span data-ttu-id="09a15-126">Wartość logiczna skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="09a15-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a15-127">-ResourceGroupName</span></span>
<span data-ttu-id="09a15-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="09a15-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-129">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="09a15-129">-Tier</span></span>
<span data-ttu-id="09a15-130">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="09a15-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="09a15-131">-WorkerSize</span></span>
<span data-ttu-id="09a15-132">Rozmiar pracownika</span><span class="sxs-lookup"><span data-stu-id="09a15-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a15-133">CommonParameters</span></span>
<span data-ttu-id="09a15-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a15-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a15-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a15-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09a15-136">INPUTS</span></span>

### <span data-ttu-id="09a15-137">Microsoft. Azure. Management. Web. MODELES. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09a15-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="09a15-138">Parametry: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="09a15-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="09a15-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09a15-139">OUTPUTS</span></span>

### <span data-ttu-id="09a15-140">Microsoft. Azure. Management. Web. MODELES. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09a15-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="09a15-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09a15-141">NOTES</span></span>

## <span data-ttu-id="09a15-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09a15-142">RELATED LINKS</span></span>

[<span data-ttu-id="09a15-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="09a15-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="09a15-144">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="09a15-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="09a15-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="09a15-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="09a15-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="09a15-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="09a15-147">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="09a15-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="09a15-148">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="09a15-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


