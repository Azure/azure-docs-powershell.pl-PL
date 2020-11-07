---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: fe079282d85b5aea8ebedcf69504fbb0e3dab04b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892937"
---
# <span data-ttu-id="463dd-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="463dd-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="463dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="463dd-102">SYNOPSIS</span></span>
<span data-ttu-id="463dd-103">Usuwa trasę z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="463dd-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="463dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="463dd-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="463dd-105">DESCRIPTION</span></span>
<span data-ttu-id="463dd-106">Polecenie cmdlet **Remove-AzRouteConfig** usuwa trasę z tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="463dd-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="463dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="463dd-107">EXAMPLES</span></span>

### <span data-ttu-id="463dd-108">Przykład 1: Usuwanie trasy</span><span class="sxs-lookup"><span data-stu-id="463dd-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="463dd-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="463dd-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="463dd-110">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="463dd-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="463dd-111">Bieżące polecenie cmdlet usuwa trasę o nazwie Route02 i przekazuje wynik do polecenia cmdlet **Set-AzRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="463dd-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="463dd-112">Tabela nie zawiera już trasy o nazwie Route02.</span><span class="sxs-lookup"><span data-stu-id="463dd-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="463dd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="463dd-113">PARAMETERS</span></span>

### <span data-ttu-id="463dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463dd-114">-DefaultProfile</span></span>
<span data-ttu-id="463dd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="463dd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="463dd-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="463dd-116">-Name</span></span>
<span data-ttu-id="463dd-117">Określa nazwę trasy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463dd-117">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463dd-118">-Routeing</span><span class="sxs-lookup"><span data-stu-id="463dd-118">-RouteTable</span></span>
<span data-ttu-id="463dd-119">Określa tabelę tras zawierającą trasę usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463dd-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="463dd-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="463dd-120">-Confirm</span></span>
<span data-ttu-id="463dd-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463dd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463dd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463dd-122">-WhatIf</span></span>
<span data-ttu-id="463dd-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463dd-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="463dd-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="463dd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463dd-125">CommonParameters</span></span>
<span data-ttu-id="463dd-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463dd-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463dd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463dd-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="463dd-128">INPUTS</span></span>

### <span data-ttu-id="463dd-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="463dd-129">PSRouteTable</span></span>
<span data-ttu-id="463dd-130">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="463dd-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="463dd-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="463dd-131">OUTPUTS</span></span>

### <span data-ttu-id="463dd-132">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="463dd-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="463dd-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="463dd-133">NOTES</span></span>

## <span data-ttu-id="463dd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="463dd-134">RELATED LINKS</span></span>

[<span data-ttu-id="463dd-135">Dodaj-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="463dd-135">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="463dd-136">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="463dd-136">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="463dd-137">Nowe — AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="463dd-137">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="463dd-138">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="463dd-138">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


