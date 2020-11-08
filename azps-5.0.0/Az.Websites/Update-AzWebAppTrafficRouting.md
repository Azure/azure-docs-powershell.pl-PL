---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225119"
---
# <span data-ttu-id="b9a56-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b9a56-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="b9a56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9a56-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a56-103">Aktualizowanie reguły routingu do gniazda.</span><span class="sxs-lookup"><span data-stu-id="b9a56-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="b9a56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9a56-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a56-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9a56-105">DESCRIPTION</span></span>
<span data-ttu-id="b9a56-106">Polecenie cmdlet **Update-AzWebAppTrafficRouting** aktualizuje konfigurację reguły routingu dla miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b9a56-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="b9a56-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9a56-107">EXAMPLES</span></span>

### <span data-ttu-id="b9a56-108">Przykład 1 Aktualizowanie reguły routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda STG</span><span class="sxs-lookup"><span data-stu-id="b9a56-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="b9a56-109">To polecenie powoduje zaktualizowanie reguły routingu w celu przeniesienia 15% ruchu produkcyjnego do gniazda STG.</span><span class="sxs-lookup"><span data-stu-id="b9a56-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="b9a56-110">Przykład 2 aktualizowanie reguły routingu w celu przetransferowania ruchu produkcyjnego do gniazd STG z zakresu od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="b9a56-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="b9a56-111">To polecenie aktualizuje regułę routingu w celu przetransferowania ruchu produkcyjnego do zakresów STG od 50% do 90% w sposób przyrostowy.</span><span class="sxs-lookup"><span data-stu-id="b9a56-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="b9a56-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9a56-112">PARAMETERS</span></span>

### <span data-ttu-id="b9a56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a56-113">-DefaultProfile</span></span>
<span data-ttu-id="b9a56-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a56-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9a56-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a56-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="b9a56-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="b9a56-117">-RoutingRule</span></span>
<span data-ttu-id="b9a56-118">RoutingRule aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b9a56-118">Web App RoutingRule.</span></span>
<span data-ttu-id="b9a56-119">Przykład:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="b9a56-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="b9a56-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b9a56-120">-WebAppName</span></span>
<span data-ttu-id="b9a56-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b9a56-121">WebApp Name</span></span>

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

### <span data-ttu-id="b9a56-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9a56-122">-Confirm</span></span>
<span data-ttu-id="b9a56-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a56-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a56-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a56-124">-WhatIf</span></span>
<span data-ttu-id="b9a56-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a56-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a56-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9a56-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a56-127">CommonParameters</span></span>
<span data-ttu-id="b9a56-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a56-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9a56-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a56-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9a56-130">INPUTS</span></span>

### <span data-ttu-id="b9a56-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9a56-131">None</span></span>

## <span data-ttu-id="b9a56-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9a56-132">OUTPUTS</span></span>

### <span data-ttu-id="b9a56-133">Microsoft. Azure. Management. Web. MODELES. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="b9a56-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="b9a56-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9a56-134">NOTES</span></span>

## <span data-ttu-id="b9a56-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9a56-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9a56-136">Dodaj-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b9a56-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b9a56-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b9a56-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b9a56-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b9a56-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)