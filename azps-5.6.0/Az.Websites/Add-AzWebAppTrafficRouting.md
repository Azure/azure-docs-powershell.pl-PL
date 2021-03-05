---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983930"
---
# <span data-ttu-id="f8c03-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f8c03-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="f8c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c03-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c03-103">Dodaj regułę routingu do gniazda.</span><span class="sxs-lookup"><span data-stu-id="f8c03-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="f8c03-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f8c03-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8c03-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f8c03-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c03-106">Polecenie **cmdlet Add-AzWebAppTrafficRouting** dodaje regułę routingu do gniazda aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f8c03-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="f8c03-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f8c03-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c03-108">Przykład 1. Dodawanie reguły routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda Stg</span><span class="sxs-lookup"><span data-stu-id="f8c03-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="f8c03-109">To polecenie dodaje regułę routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda Stg</span><span class="sxs-lookup"><span data-stu-id="f8c03-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="f8c03-110">Przykład 2 Dodawanie reguły routingu w celu przenoszenia ruchu produkcyjnego do zakresów slotów Stg z zakresu od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="f8c03-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="f8c03-111">To polecenie dodaje regułę routingu w celu przenoszenia ruchu produkcyjnego do zakresów przedziałów stg z zakresu od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="f8c03-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="f8c03-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8c03-112">PARAMETERS</span></span>

### <span data-ttu-id="f8c03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c03-113">-DefaultProfile</span></span>
<span data-ttu-id="f8c03-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c03-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c03-115">-ResourceGroupName</span></span>
<span data-ttu-id="f8c03-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f8c03-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f8c03-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8c03-117">-RoutingRule</span></span>
<span data-ttu-id="f8c03-118">RoutingRule aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f8c03-118">Web App RoutingRule.</span></span>
<span data-ttu-id="f8c03-119">Przykład: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="f8c03-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="f8c03-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f8c03-120">-WebAppName</span></span>
<span data-ttu-id="f8c03-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="f8c03-121">WebApp Name</span></span>

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

### <span data-ttu-id="f8c03-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8c03-122">-Confirm</span></span>
<span data-ttu-id="f8c03-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8c03-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c03-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c03-124">-WhatIf</span></span>
<span data-ttu-id="f8c03-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8c03-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8c03-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f8c03-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c03-127">CommonParameters</span></span>
<span data-ttu-id="f8c03-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c03-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8c03-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c03-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8c03-130">INPUTS</span></span>

### <span data-ttu-id="f8c03-131">Brak</span><span class="sxs-lookup"><span data-stu-id="f8c03-131">None</span></span>

## <span data-ttu-id="f8c03-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8c03-132">OUTPUTS</span></span>

### <span data-ttu-id="f8c03-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="f8c03-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="f8c03-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f8c03-134">NOTES</span></span>

## <span data-ttu-id="f8c03-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8c03-135">RELATED LINKS</span></span>
[<span data-ttu-id="f8c03-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f8c03-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f8c03-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f8c03-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f8c03-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f8c03-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
