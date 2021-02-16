---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179475"
---
# <span data-ttu-id="21637-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21637-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="21637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21637-102">SYNOPSIS</span></span>
<span data-ttu-id="21637-103">Usuwa trasę z tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="21637-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="21637-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21637-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21637-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="21637-105">DESCRIPTION</span></span>
<span data-ttu-id="21637-106">Polecenie **cmdlet Remove-AzRouteConfig** usuwa trasę z tabeli trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21637-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="21637-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21637-107">EXAMPLES</span></span>

### <span data-ttu-id="21637-108">Przykład 1. Usuwanie trasy</span><span class="sxs-lookup"><span data-stu-id="21637-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="21637-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="21637-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="21637-110">Polecenie przekazuje tabelę do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="21637-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="21637-111">Bieżące polecenie cmdlet usuwa trasę o nazwie Route02, a wynik przekazuje wynik do polecenia cmdlet **Set-AzRouteTable,** które aktualizuje tabelę w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="21637-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="21637-112">Tabela nie zawiera już trasy o nazwie Route02.</span><span class="sxs-lookup"><span data-stu-id="21637-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="21637-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21637-113">PARAMETERS</span></span>

### <span data-ttu-id="21637-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21637-114">-DefaultProfile</span></span>
<span data-ttu-id="21637-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21637-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21637-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21637-116">-Name</span></span>
<span data-ttu-id="21637-117">Określa nazwę trasy, która zostanie usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21637-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="21637-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="21637-118">-RouteTable</span></span>
<span data-ttu-id="21637-119">Określa tabelę trasy zawierającą trasę usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21637-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="21637-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21637-120">-Confirm</span></span>
<span data-ttu-id="21637-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="21637-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21637-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21637-122">-WhatIf</span></span>
<span data-ttu-id="21637-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21637-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21637-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="21637-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21637-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21637-125">CommonParameters</span></span>
<span data-ttu-id="21637-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21637-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21637-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21637-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21637-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21637-128">INPUTS</span></span>

### <span data-ttu-id="21637-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="21637-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="21637-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21637-130">OUTPUTS</span></span>

### <span data-ttu-id="21637-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="21637-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="21637-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21637-132">NOTES</span></span>

## <span data-ttu-id="21637-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21637-133">RELATED LINKS</span></span>

[<span data-ttu-id="21637-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21637-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="21637-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21637-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="21637-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21637-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="21637-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21637-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


