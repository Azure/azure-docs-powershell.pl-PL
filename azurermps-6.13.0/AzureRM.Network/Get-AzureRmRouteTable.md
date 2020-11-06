---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 04e50033a304918eb37d28c2ef5ea5328d5744c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545080"
---
# <span data-ttu-id="839fb-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="839fb-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="839fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="839fb-102">SYNOPSIS</span></span>
<span data-ttu-id="839fb-103">Pobiera tabele tras.</span><span class="sxs-lookup"><span data-stu-id="839fb-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="839fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="839fb-104">SYNTAX</span></span>

### <span data-ttu-id="839fb-105">NOEXPAND (domyślne)</span><span class="sxs-lookup"><span data-stu-id="839fb-105">NoExpand (Default)</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="839fb-106">Większa</span><span class="sxs-lookup"><span data-stu-id="839fb-106">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="839fb-107">DESCRIPTION</span></span>
<span data-ttu-id="839fb-108">Polecenie cmdlet **Get-AzureRmRouteTable** pobiera tabele tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="839fb-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="839fb-109">Możesz skorzystać z jednej tabeli routingu lub pobrać wszystkie tabele tras w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="839fb-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="839fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="839fb-110">EXAMPLES</span></span>

### <span data-ttu-id="839fb-111">Przykład 1: pobieranie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="839fb-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="839fb-112">To polecenie pobiera tabelę tras o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="839fb-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="839fb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="839fb-113">PARAMETERS</span></span>

### <span data-ttu-id="839fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839fb-114">-DefaultProfile</span></span>
<span data-ttu-id="839fb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="839fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839fb-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="839fb-116">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839fb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="839fb-117">-Name</span></span>
<span data-ttu-id="839fb-118">Określa nazwę tabeli routingu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="839fb-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="839fb-120">Określa nazwę grupy zasobów zawierającej tabele tras, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="839fb-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839fb-121">CommonParameters</span></span>
<span data-ttu-id="839fb-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="839fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839fb-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839fb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839fb-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="839fb-124">INPUTS</span></span>

### <span data-ttu-id="839fb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="839fb-125">System.String</span></span>

## <span data-ttu-id="839fb-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="839fb-126">OUTPUTS</span></span>

### <span data-ttu-id="839fb-127">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="839fb-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="839fb-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="839fb-128">NOTES</span></span>

## <span data-ttu-id="839fb-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="839fb-129">RELATED LINKS</span></span>

[<span data-ttu-id="839fb-130">Nowe — AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="839fb-130">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="839fb-131">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="839fb-131">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="839fb-132">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="839fb-132">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


