---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 711d9848188cbdbaaeac9313680fd9fd70cb1f34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528062"
---
# <span data-ttu-id="72bea-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="72bea-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="72bea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72bea-102">SYNOPSIS</span></span>
<span data-ttu-id="72bea-103">Pobiera tabele tras.</span><span class="sxs-lookup"><span data-stu-id="72bea-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72bea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72bea-104">SYNTAX</span></span>

### <span data-ttu-id="72bea-105">Większa</span><span class="sxs-lookup"><span data-stu-id="72bea-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72bea-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="72bea-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72bea-107">Opis</span><span class="sxs-lookup"><span data-stu-id="72bea-107">DESCRIPTION</span></span>
<span data-ttu-id="72bea-108">Polecenie cmdlet **Get-AzureRmRouteTable** pobiera tabele tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72bea-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="72bea-109">Możesz skorzystać z jednej tabeli routingu lub pobrać wszystkie tabele tras w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="72bea-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="72bea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72bea-110">EXAMPLES</span></span>

### <span data-ttu-id="72bea-111">Przykład 1: pobieranie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="72bea-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="72bea-112">To polecenie pobiera tabelę tras o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="72bea-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="72bea-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72bea-113">PARAMETERS</span></span>

### <span data-ttu-id="72bea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bea-114">-DefaultProfile</span></span>
<span data-ttu-id="72bea-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72bea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72bea-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="72bea-116">-ExpandResource</span></span>
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

### <span data-ttu-id="72bea-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72bea-117">-Name</span></span>
<span data-ttu-id="72bea-118">Określa nazwę tabeli routingu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72bea-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="72bea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72bea-119">-ResourceGroupName</span></span>
<span data-ttu-id="72bea-120">Określa nazwę grupy zasobów zawierającej tabele tras, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72bea-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="72bea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bea-121">CommonParameters</span></span>
<span data-ttu-id="72bea-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72bea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bea-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72bea-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bea-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72bea-124">INPUTS</span></span>

### <span data-ttu-id="72bea-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="72bea-125">None</span></span>
<span data-ttu-id="72bea-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="72bea-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72bea-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72bea-127">OUTPUTS</span></span>

### <span data-ttu-id="72bea-128">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="72bea-128">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="72bea-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72bea-129">NOTES</span></span>

## <span data-ttu-id="72bea-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72bea-130">RELATED LINKS</span></span>

[<span data-ttu-id="72bea-131">Nowe — AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="72bea-131">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="72bea-132">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="72bea-132">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="72bea-133">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="72bea-133">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

