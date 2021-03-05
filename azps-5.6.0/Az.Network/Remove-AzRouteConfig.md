---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: e48da3a5f300d39051a9d1b07e9789855ed7dca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996122"
---
# <span data-ttu-id="1400c-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1400c-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="1400c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1400c-102">SYNOPSIS</span></span>
<span data-ttu-id="1400c-103">Usuwa trasę z tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="1400c-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="1400c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1400c-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1400c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1400c-105">DESCRIPTION</span></span>
<span data-ttu-id="1400c-106">Polecenie **cmdlet Remove-AzRouteConfig** usuwa trasę z tabeli trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1400c-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="1400c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1400c-107">EXAMPLES</span></span>

### <span data-ttu-id="1400c-108">Przykład 1. Usuwanie trasy</span><span class="sxs-lookup"><span data-stu-id="1400c-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="1400c-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="1400c-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="1400c-110">Polecenie przekazuje tabelę do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1400c-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1400c-111">Bieżące polecenie cmdlet usuwa trasę o nazwie Route02, a wynik przekazuje wynik do polecenia cmdlet **Set-AzRouteTable,** które aktualizuje tabelę w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="1400c-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="1400c-112">Tabela nie zawiera już trasy o nazwie Route02.</span><span class="sxs-lookup"><span data-stu-id="1400c-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="1400c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1400c-113">PARAMETERS</span></span>

### <span data-ttu-id="1400c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1400c-114">-DefaultProfile</span></span>
<span data-ttu-id="1400c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1400c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1400c-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1400c-116">-Name</span></span>
<span data-ttu-id="1400c-117">Określa nazwę trasy, która zostanie usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1400c-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1400c-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1400c-118">-RouteTable</span></span>
<span data-ttu-id="1400c-119">Określa tabelę trasy zawierającą trasę usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1400c-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1400c-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1400c-120">-Confirm</span></span>
<span data-ttu-id="1400c-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1400c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1400c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1400c-122">-WhatIf</span></span>
<span data-ttu-id="1400c-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1400c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1400c-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1400c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1400c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1400c-125">CommonParameters</span></span>
<span data-ttu-id="1400c-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1400c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1400c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1400c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1400c-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1400c-128">INPUTS</span></span>

### <span data-ttu-id="1400c-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1400c-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1400c-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1400c-130">OUTPUTS</span></span>

### <span data-ttu-id="1400c-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1400c-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1400c-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1400c-132">NOTES</span></span>

## <span data-ttu-id="1400c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1400c-133">RELATED LINKS</span></span>

[<span data-ttu-id="1400c-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1400c-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="1400c-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1400c-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="1400c-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1400c-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="1400c-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1400c-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


