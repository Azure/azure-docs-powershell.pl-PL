---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: ba8fc7809bc9cea8ea34dbc4d15816134e8d7e13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872156"
---
# <span data-ttu-id="6aa52-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6aa52-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="6aa52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aa52-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa52-103">Umożliwia zaktualizowanie tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="6aa52-103">Updates a route table.</span></span>

## <span data-ttu-id="6aa52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aa52-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aa52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6aa52-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa52-106">Polecenie cmdlet **Set-AzRouteTable** umożliwia zaktualizowanie tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="6aa52-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="6aa52-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aa52-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa52-108">Przykład 1: aktualizowanie tabeli tras przez dodanie do niej konfiguracji trasy</span><span class="sxs-lookup"><span data-stu-id="6aa52-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="6aa52-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="6aa52-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="6aa52-110">Polecenie przekazuje tę tabelę do polecenia cmdlet Add-AzRouteConfig przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6aa52-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6aa52-111">Polecenie **Add-AzRouteConfig** dodaje trasę o nazwie Route07, a następnie przekazuje wynik do bieżącego polecenia cmdlet, co powoduje zaktualizowanie tabeli w celu odzwierciedlenia zmian.</span><span class="sxs-lookup"><span data-stu-id="6aa52-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="6aa52-112">Przykład 2: modyfikowanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="6aa52-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="6aa52-113">Pierwsze polecenie uzyskuje tabelę trasa o nazwie rtName i zapisuje ją w zmiennej $rt.</span><span class="sxs-lookup"><span data-stu-id="6aa52-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="6aa52-114">Drugie polecenie wyświetla wartość DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="6aa52-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="6aa52-115">Trzecie polecenie aktualizuje wartość DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="6aa52-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="6aa52-116">Czwarte polecenie aktualizuje tabelę routingu na serwerze.</span><span class="sxs-lookup"><span data-stu-id="6aa52-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="6aa52-117">Piąte polecenie pobiera zaktualizowaną tabelę routingu i zapisuje ją w zmiennej $rt.</span><span class="sxs-lookup"><span data-stu-id="6aa52-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="6aa52-118">W szóstym poleceniu jest wyświetlana wartość DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="6aa52-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="6aa52-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aa52-119">PARAMETERS</span></span>

### <span data-ttu-id="6aa52-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aa52-120">-AsJob</span></span>
<span data-ttu-id="6aa52-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6aa52-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6aa52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa52-122">-DefaultProfile</span></span>
<span data-ttu-id="6aa52-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa52-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa52-124">-Routeing</span><span class="sxs-lookup"><span data-stu-id="6aa52-124">-RouteTable</span></span>
<span data-ttu-id="6aa52-125">Określa obiekt tabeli tras reprezentujący stan, do którego powinna być ustawiona tabela tras.</span><span class="sxs-lookup"><span data-stu-id="6aa52-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa52-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aa52-126">-Confirm</span></span>
<span data-ttu-id="6aa52-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa52-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa52-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa52-128">-WhatIf</span></span>
<span data-ttu-id="6aa52-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa52-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6aa52-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6aa52-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa52-131">CommonParameters</span></span>
<span data-ttu-id="6aa52-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa52-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa52-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa52-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aa52-134">INPUTS</span></span>

### <span data-ttu-id="6aa52-135">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6aa52-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="6aa52-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aa52-136">OUTPUTS</span></span>

### <span data-ttu-id="6aa52-137">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6aa52-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="6aa52-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aa52-138">NOTES</span></span>

## <span data-ttu-id="6aa52-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aa52-139">RELATED LINKS</span></span>

[<span data-ttu-id="6aa52-140">Dodaj-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6aa52-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="6aa52-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6aa52-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="6aa52-142">Nowe — AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6aa52-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="6aa52-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="6aa52-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


