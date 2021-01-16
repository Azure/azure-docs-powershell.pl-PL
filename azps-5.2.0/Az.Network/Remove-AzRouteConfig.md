---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348733"
---
# <span data-ttu-id="65a25-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65a25-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="65a25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65a25-102">SYNOPSIS</span></span>
<span data-ttu-id="65a25-103">Usuwa trasę z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="65a25-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="65a25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65a25-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65a25-105">DESCRIPTION</span></span>
<span data-ttu-id="65a25-106">Polecenie cmdlet **Remove-AzRouteConfig** usuwa trasę z tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65a25-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="65a25-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65a25-107">EXAMPLES</span></span>

### <span data-ttu-id="65a25-108">Przykład 1: Usuwanie trasy</span><span class="sxs-lookup"><span data-stu-id="65a25-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="65a25-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="65a25-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="65a25-110">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="65a25-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="65a25-111">Bieżące polecenie cmdlet usuwa trasę o nazwie Route02 i przekazuje wynik do polecenia cmdlet **Set-AzRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="65a25-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="65a25-112">Tabela nie zawiera już trasy o nazwie Route02.</span><span class="sxs-lookup"><span data-stu-id="65a25-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="65a25-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65a25-113">PARAMETERS</span></span>

### <span data-ttu-id="65a25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a25-114">-DefaultProfile</span></span>
<span data-ttu-id="65a25-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65a25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a25-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65a25-116">-Name</span></span>
<span data-ttu-id="65a25-117">Określa nazwę trasy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a25-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="65a25-118">-Routeing</span><span class="sxs-lookup"><span data-stu-id="65a25-118">-RouteTable</span></span>
<span data-ttu-id="65a25-119">Określa tabelę tras zawierającą trasę usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a25-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="65a25-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65a25-120">-Confirm</span></span>
<span data-ttu-id="65a25-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a25-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a25-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a25-122">-WhatIf</span></span>
<span data-ttu-id="65a25-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a25-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65a25-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65a25-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a25-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a25-125">CommonParameters</span></span>
<span data-ttu-id="65a25-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a25-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a25-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a25-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a25-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a25-128">INPUTS</span></span>

### <span data-ttu-id="65a25-129">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="65a25-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="65a25-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65a25-130">OUTPUTS</span></span>

### <span data-ttu-id="65a25-131">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="65a25-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="65a25-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65a25-132">NOTES</span></span>

## <span data-ttu-id="65a25-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65a25-133">RELATED LINKS</span></span>

[<span data-ttu-id="65a25-134">Dodaj-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65a25-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="65a25-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65a25-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="65a25-136">Nowe — AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65a25-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="65a25-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65a25-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


