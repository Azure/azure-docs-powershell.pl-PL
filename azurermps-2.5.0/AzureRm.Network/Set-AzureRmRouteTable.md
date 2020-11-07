---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 198b14e4aab131b3d6044c793c5f3a4ea030b322
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899063"
---
# <span data-ttu-id="087ea-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="087ea-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="087ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="087ea-102">SYNOPSIS</span></span>
<span data-ttu-id="087ea-103">Ustawia stan celu dla tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="087ea-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="087ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="087ea-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="087ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="087ea-105">DESCRIPTION</span></span>
<span data-ttu-id="087ea-106">Polecenie cmdlet **Set-AzureRmRouteTable** ustawia stan celu dla tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="087ea-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="087ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="087ea-107">EXAMPLES</span></span>

### <span data-ttu-id="087ea-108">Przykład 1. Dodaj trasę, a następnie ustaw stan celu w tabeli tras</span><span class="sxs-lookup"><span data-stu-id="087ea-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
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

<span data-ttu-id="087ea-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="087ea-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="087ea-110">Polecenie przekazuje tę tabelę do polecenia cmdlet Add-AzureRmRouteConfig przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="087ea-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="087ea-111">Polecenie **Add-AzureRmRouteConfig** dodaje trasę o nazwie Route07, a następnie przekazuje wynik do bieżącego polecenia cmdlet, co powoduje zaktualizowanie tabeli w celu odzwierciedlenia zmian.</span><span class="sxs-lookup"><span data-stu-id="087ea-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="087ea-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="087ea-112">PARAMETERS</span></span>

### <span data-ttu-id="087ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="087ea-113">-AsJob</span></span>
<span data-ttu-id="087ea-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="087ea-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087ea-115">-DefaultProfile</span></span>
<span data-ttu-id="087ea-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="087ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087ea-117">-Routeing</span><span class="sxs-lookup"><span data-stu-id="087ea-117">-RouteTable</span></span>
<span data-ttu-id="087ea-118">Określa obiekt tabeli tras reprezentujący stan celu, do którego to polecenie cmdlet ustawia tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="087ea-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="087ea-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="087ea-119">-Confirm</span></span>
<span data-ttu-id="087ea-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="087ea-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087ea-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="087ea-121">-WhatIf</span></span>
<span data-ttu-id="087ea-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="087ea-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="087ea-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="087ea-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087ea-124">CommonParameters</span></span>
<span data-ttu-id="087ea-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087ea-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="087ea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087ea-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="087ea-127">INPUTS</span></span>

### <span data-ttu-id="087ea-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="087ea-128">PSRouteTable</span></span>
<span data-ttu-id="087ea-129">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="087ea-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="087ea-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="087ea-130">OUTPUTS</span></span>

### <span data-ttu-id="087ea-131">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="087ea-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="087ea-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="087ea-132">NOTES</span></span>

## <span data-ttu-id="087ea-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="087ea-133">RELATED LINKS</span></span>

[<span data-ttu-id="087ea-134">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="087ea-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="087ea-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="087ea-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="087ea-136">Nowe — AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="087ea-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="087ea-137">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="087ea-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


