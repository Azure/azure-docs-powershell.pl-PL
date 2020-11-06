---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: e525580d7384eef6b7fa7518fc6ddc5707a010ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546196"
---
# <span data-ttu-id="989cf-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="989cf-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="989cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="989cf-102">SYNOPSIS</span></span>
<span data-ttu-id="989cf-103">Ustawia stan celu dla tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="989cf-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="989cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="989cf-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="989cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="989cf-105">DESCRIPTION</span></span>
<span data-ttu-id="989cf-106">Polecenie cmdlet **Set-AzureRmRouteTable** ustawia stan celu dla tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="989cf-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="989cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="989cf-107">EXAMPLES</span></span>

### <span data-ttu-id="989cf-108">Przykład 1. Dodaj trasę, a następnie ustaw stan celu w tabeli tras</span><span class="sxs-lookup"><span data-stu-id="989cf-108">Example 1: Add a route and then set the goal state of the route table</span></span>
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

<span data-ttu-id="989cf-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="989cf-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="989cf-110">Polecenie przekazuje tę tabelę do polecenia cmdlet Add-AzureRmRouteConfig przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="989cf-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="989cf-111">Polecenie **Add-AzureRmRouteConfig** dodaje trasę o nazwie Route07, a następnie przekazuje wynik do bieżącego polecenia cmdlet, co powoduje zaktualizowanie tabeli w celu odzwierciedlenia zmian.</span><span class="sxs-lookup"><span data-stu-id="989cf-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="989cf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="989cf-112">PARAMETERS</span></span>

### <span data-ttu-id="989cf-113">-Routeing</span><span class="sxs-lookup"><span data-stu-id="989cf-113">-RouteTable</span></span>
<span data-ttu-id="989cf-114">Określa obiekt tabeli tras reprezentujący stan celu, do którego to polecenie cmdlet ustawia tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="989cf-114">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

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

### <span data-ttu-id="989cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989cf-115">-DefaultProfile</span></span>
<span data-ttu-id="989cf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="989cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="989cf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989cf-117">CommonParameters</span></span>
<span data-ttu-id="989cf-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989cf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989cf-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="989cf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989cf-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="989cf-120">INPUTS</span></span>

### <span data-ttu-id="989cf-121">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="989cf-121">PSRouteTable</span></span>
<span data-ttu-id="989cf-122">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="989cf-122">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="989cf-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="989cf-123">OUTPUTS</span></span>

### <span data-ttu-id="989cf-124">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="989cf-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="989cf-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="989cf-125">NOTES</span></span>

## <span data-ttu-id="989cf-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="989cf-126">RELATED LINKS</span></span>

[<span data-ttu-id="989cf-127">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="989cf-127">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="989cf-128">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="989cf-128">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="989cf-129">Nowe — AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="989cf-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="989cf-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="989cf-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


