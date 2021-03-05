---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010961"
---
# <span data-ttu-id="7a99e-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7a99e-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="7a99e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a99e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a99e-103">Zaktualizuj regułę routingu do gniazda.</span><span class="sxs-lookup"><span data-stu-id="7a99e-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="7a99e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a99e-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a99e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a99e-105">DESCRIPTION</span></span>
<span data-ttu-id="7a99e-106">Polecenie **cmdlet Update-AzWebAppTrafficRouting** aktualizuje konfigurację reguły routingu dla gniazda aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7a99e-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="7a99e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a99e-107">EXAMPLES</span></span>

### <span data-ttu-id="7a99e-108">Przykład 1. Aktualizowanie reguły routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda Stg</span><span class="sxs-lookup"><span data-stu-id="7a99e-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="7a99e-109">To polecenie aktualizuje regułę routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda Stg.</span><span class="sxs-lookup"><span data-stu-id="7a99e-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="7a99e-110">Przykład 2. Aktualizowanie reguły routingu w celu przeniesienia ruchu produkcyjnego do zakresów slotów Stg z zakresu od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="7a99e-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="7a99e-111">To polecenie aktualizuje regułę routingu w celu przeniesienia ruchu produkcyjnego do zakresów slotów Stg z zakresu od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="7a99e-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="7a99e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a99e-112">PARAMETERS</span></span>

### <span data-ttu-id="7a99e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a99e-113">-DefaultProfile</span></span>
<span data-ttu-id="7a99e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a99e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a99e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a99e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a99e-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a99e-116">ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a99e-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a99e-117">-RoutingRule</span></span>
<span data-ttu-id="7a99e-118">RoutingRule aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7a99e-118">Web App RoutingRule.</span></span>
<span data-ttu-id="7a99e-119">Przykład: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="7a99e-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a99e-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7a99e-120">-WebAppName</span></span>
<span data-ttu-id="7a99e-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="7a99e-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a99e-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a99e-122">-Confirm</span></span>
<span data-ttu-id="7a99e-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a99e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a99e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a99e-124">-WhatIf</span></span>
<span data-ttu-id="7a99e-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a99e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a99e-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a99e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a99e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a99e-127">CommonParameters</span></span>
<span data-ttu-id="7a99e-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a99e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a99e-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a99e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a99e-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a99e-130">INPUTS</span></span>

### <span data-ttu-id="7a99e-131">Brak</span><span class="sxs-lookup"><span data-stu-id="7a99e-131">None</span></span>

## <span data-ttu-id="7a99e-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a99e-132">OUTPUTS</span></span>

### <span data-ttu-id="7a99e-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="7a99e-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="7a99e-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a99e-134">NOTES</span></span>

## <span data-ttu-id="7a99e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a99e-135">RELATED LINKS</span></span>

[<span data-ttu-id="7a99e-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7a99e-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7a99e-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7a99e-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7a99e-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7a99e-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)