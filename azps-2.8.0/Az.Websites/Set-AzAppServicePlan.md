---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888066"
---
# <span data-ttu-id="abcda-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="abcda-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="abcda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abcda-102">SYNOPSIS</span></span>
<span data-ttu-id="abcda-103">Umożliwia ustawienie planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="abcda-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="abcda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abcda-104">SYNTAX</span></span>

### <span data-ttu-id="abcda-105">S1</span><span class="sxs-lookup"><span data-stu-id="abcda-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abcda-106">S2</span><span class="sxs-lookup"><span data-stu-id="abcda-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abcda-107">Opis</span><span class="sxs-lookup"><span data-stu-id="abcda-107">DESCRIPTION</span></span>
<span data-ttu-id="abcda-108">Polecenie cmdlet **Set-AzAppServicePlan** określa plan usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="abcda-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="abcda-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abcda-109">EXAMPLES</span></span>

### <span data-ttu-id="abcda-110">1: modyfikowanie planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="abcda-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="abcda-111">To polecenie ustawia opcję PerSiteScaling na wartość prawda w planie usługi App Service o nazwie ContosoASP należącego do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="abcda-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="abcda-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abcda-112">PARAMETERS</span></span>

### <span data-ttu-id="abcda-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="abcda-113">-AdminSiteName</span></span>
<span data-ttu-id="abcda-114">Nazwa witryny administracyjnej</span><span class="sxs-lookup"><span data-stu-id="abcda-114">Admin Site Name</span></span>

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

### <span data-ttu-id="abcda-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="abcda-115">-AppServicePlan</span></span>
<span data-ttu-id="abcda-116">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="abcda-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="abcda-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abcda-117">-AsJob</span></span>
<span data-ttu-id="abcda-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="abcda-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abcda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abcda-119">-DefaultProfile</span></span>
<span data-ttu-id="abcda-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="abcda-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abcda-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abcda-121">-Name</span></span>
<span data-ttu-id="abcda-122">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="abcda-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="abcda-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="abcda-123">-NumberofWorkers</span></span>
<span data-ttu-id="abcda-124">Liczba pracowników</span><span class="sxs-lookup"><span data-stu-id="abcda-124">Number Of Workers</span></span>

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

### <span data-ttu-id="abcda-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="abcda-125">-PerSiteScaling</span></span>
<span data-ttu-id="abcda-126">Wartość logiczna skalowania dla witryny</span><span class="sxs-lookup"><span data-stu-id="abcda-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="abcda-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abcda-127">-ResourceGroupName</span></span>
<span data-ttu-id="abcda-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="abcda-128">Resource Group Name</span></span>

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

### <span data-ttu-id="abcda-129">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="abcda-129">-Tier</span></span>
<span data-ttu-id="abcda-130">Trójwarstwowej</span><span class="sxs-lookup"><span data-stu-id="abcda-130">Tier</span></span>

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

### <span data-ttu-id="abcda-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="abcda-131">-WorkerSize</span></span>
<span data-ttu-id="abcda-132">Rozmiar pracownika</span><span class="sxs-lookup"><span data-stu-id="abcda-132">Worker Size</span></span>

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

### <span data-ttu-id="abcda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcda-133">CommonParameters</span></span>
<span data-ttu-id="abcda-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abcda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcda-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcda-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcda-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abcda-136">INPUTS</span></span>

### <span data-ttu-id="abcda-137">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="abcda-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="abcda-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abcda-138">OUTPUTS</span></span>

### <span data-ttu-id="abcda-139">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="abcda-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="abcda-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abcda-140">NOTES</span></span>

## <span data-ttu-id="abcda-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abcda-141">RELATED LINKS</span></span>

[<span data-ttu-id="abcda-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abcda-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="abcda-143">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abcda-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="abcda-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abcda-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="abcda-145">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abcda-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="abcda-146">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abcda-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="abcda-147">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="abcda-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


