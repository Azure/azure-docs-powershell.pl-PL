---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: 704ac762bdc7569fd5ad2c0c4912ebf9634e25ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718800"
---
# <span data-ttu-id="685d1-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="685d1-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="685d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="685d1-102">SYNOPSIS</span></span>
<span data-ttu-id="685d1-103">Usuwa trasę z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="685d1-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="685d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="685d1-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="685d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="685d1-105">DESCRIPTION</span></span>
<span data-ttu-id="685d1-106">Polecenie cmdlet **Remove-AzureRmRouteConfig** usuwa trasę z tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="685d1-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="685d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="685d1-107">EXAMPLES</span></span>

### <span data-ttu-id="685d1-108">Przykład 1: Usuwanie trasy</span><span class="sxs-lookup"><span data-stu-id="685d1-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
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

<span data-ttu-id="685d1-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="685d1-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="685d1-110">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="685d1-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="685d1-111">Bieżące polecenie cmdlet usuwa trasę o nazwie Route02 i przekazuje wynik do polecenia cmdlet **Set-AzureRmRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="685d1-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="685d1-112">Tabela nie zawiera już trasy o nazwie Route02.</span><span class="sxs-lookup"><span data-stu-id="685d1-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="685d1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="685d1-113">PARAMETERS</span></span>

### <span data-ttu-id="685d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685d1-114">-DefaultProfile</span></span>
<span data-ttu-id="685d1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="685d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685d1-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="685d1-116">-Name</span></span>
<span data-ttu-id="685d1-117">Określa nazwę trasy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685d1-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="685d1-118">-Routeing</span><span class="sxs-lookup"><span data-stu-id="685d1-118">-RouteTable</span></span>
<span data-ttu-id="685d1-119">Określa tabelę tras zawierającą trasę usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685d1-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="685d1-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="685d1-120">-Confirm</span></span>
<span data-ttu-id="685d1-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685d1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="685d1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="685d1-122">-WhatIf</span></span>
<span data-ttu-id="685d1-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685d1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="685d1-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="685d1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="685d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685d1-125">CommonParameters</span></span>
<span data-ttu-id="685d1-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="685d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685d1-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="685d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685d1-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="685d1-128">INPUTS</span></span>

### <span data-ttu-id="685d1-129">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="685d1-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="685d1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="685d1-130">OUTPUTS</span></span>

### <span data-ttu-id="685d1-131">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="685d1-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="685d1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="685d1-132">NOTES</span></span>

## <span data-ttu-id="685d1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="685d1-133">RELATED LINKS</span></span>

[<span data-ttu-id="685d1-134">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="685d1-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="685d1-135">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="685d1-135">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="685d1-136">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="685d1-136">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="685d1-137">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="685d1-137">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


