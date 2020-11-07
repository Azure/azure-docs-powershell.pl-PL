---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890673"
---
# <span data-ttu-id="f0d33-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0d33-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="f0d33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0d33-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d33-103">Pobiera tabele tras.</span><span class="sxs-lookup"><span data-stu-id="f0d33-103">Gets route tables.</span></span>

## <span data-ttu-id="f0d33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0d33-104">SYNTAX</span></span>

### <span data-ttu-id="f0d33-105">Większa</span><span class="sxs-lookup"><span data-stu-id="f0d33-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d33-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="f0d33-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d33-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f0d33-107">DESCRIPTION</span></span>
<span data-ttu-id="f0d33-108">Polecenie cmdlet **Get-AzRouteTable** pobiera tabele tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d33-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="f0d33-109">Możesz skorzystać z jednej tabeli routingu lub pobrać wszystkie tabele tras w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f0d33-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="f0d33-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0d33-110">EXAMPLES</span></span>

### <span data-ttu-id="f0d33-111">Przykład 1: pobieranie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="f0d33-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="f0d33-112">To polecenie pobiera tabelę tras o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f0d33-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f0d33-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0d33-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d33-114">-DefaultProfile</span></span>
<span data-ttu-id="f0d33-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d33-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d33-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f0d33-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d33-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f0d33-117">-Name</span></span>
<span data-ttu-id="f0d33-118">Określa nazwę tabeli routingu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d33-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d33-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0d33-120">Określa nazwę grupy zasobów zawierającej tabele tras, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d33-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d33-121">CommonParameters</span></span>
<span data-ttu-id="f0d33-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d33-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d33-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d33-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0d33-124">INPUTS</span></span>

## <span data-ttu-id="f0d33-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0d33-125">OUTPUTS</span></span>

### <span data-ttu-id="f0d33-126">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0d33-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f0d33-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0d33-127">NOTES</span></span>

## <span data-ttu-id="f0d33-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0d33-128">RELATED LINKS</span></span>

[<span data-ttu-id="f0d33-129">Nowe — AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0d33-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="f0d33-130">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0d33-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="f0d33-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0d33-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


