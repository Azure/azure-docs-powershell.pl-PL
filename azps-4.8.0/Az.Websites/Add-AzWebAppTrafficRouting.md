---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221416"
---
# <span data-ttu-id="2a968-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2a968-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="2a968-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a968-102">SYNOPSIS</span></span>
<span data-ttu-id="2a968-103">Dodawanie reguły routingu do gniazda.</span><span class="sxs-lookup"><span data-stu-id="2a968-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="2a968-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a968-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a968-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a968-105">DESCRIPTION</span></span>
<span data-ttu-id="2a968-106">Polecenie cmdlet **Add-AzWebAppTrafficRouting** umożliwia dodanie reguły routingu do miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2a968-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="2a968-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a968-107">EXAMPLES</span></span>

### <span data-ttu-id="2a968-108">Przykład 1 dodanie reguły routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda STG</span><span class="sxs-lookup"><span data-stu-id="2a968-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="2a968-109">To polecenie umożliwia dodanie reguły routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda STG</span><span class="sxs-lookup"><span data-stu-id="2a968-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="2a968-110">Przykład 2 dodanie reguły routingu w celu przetransferowania ruchu produkcyjnego do gniazd STG z zakresu od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="2a968-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="2a968-111">To polecenie umożliwia dodanie reguły routingu w celu przetransferowania ruchu produkcyjnego do zakresów STG od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="2a968-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="2a968-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a968-112">PARAMETERS</span></span>

### <span data-ttu-id="2a968-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a968-113">-DefaultProfile</span></span>
<span data-ttu-id="2a968-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a968-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a968-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a968-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a968-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2a968-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2a968-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a968-117">-RoutingRule</span></span>
<span data-ttu-id="2a968-118">RoutingRule aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2a968-118">Web App RoutingRule.</span></span>
<span data-ttu-id="2a968-119">Przykład:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="2a968-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="2a968-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2a968-120">-WebAppName</span></span>
<span data-ttu-id="2a968-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a968-121">WebApp Name</span></span>

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

### <span data-ttu-id="2a968-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a968-122">-Confirm</span></span>
<span data-ttu-id="2a968-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a968-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a968-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a968-124">-WhatIf</span></span>
<span data-ttu-id="2a968-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a968-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a968-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a968-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a968-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a968-127">CommonParameters</span></span>
<span data-ttu-id="2a968-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a968-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a968-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a968-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a968-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a968-130">INPUTS</span></span>

### <span data-ttu-id="2a968-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2a968-131">None</span></span>

## <span data-ttu-id="2a968-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a968-132">OUTPUTS</span></span>

### <span data-ttu-id="2a968-133">Microsoft. Azure. Management. Web. MODELES. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="2a968-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="2a968-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a968-134">NOTES</span></span>

## <span data-ttu-id="2a968-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a968-135">RELATED LINKS</span></span>
[<span data-ttu-id="2a968-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2a968-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="2a968-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2a968-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="2a968-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2a968-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
