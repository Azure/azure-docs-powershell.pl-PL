---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319242"
---
# <span data-ttu-id="43021-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43021-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="43021-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43021-102">SYNOPSIS</span></span>
<span data-ttu-id="43021-103">Tworzy zasób tabeli routingu centrum wirtualnego, który jest elementem podrzędnym VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="43021-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="43021-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43021-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43021-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43021-105">DESCRIPTION</span></span>
<span data-ttu-id="43021-106">Zasób tabela routingu koncentratora wirtualnego zawiera listę tras oraz listę połączeń, do których można dołączyć i które są używane do kierowania ruchu w wirtualnym koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="43021-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="43021-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43021-107">EXAMPLES</span></span>

### <span data-ttu-id="43021-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43021-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="43021-109">Powyższe polecenie utworzy zasób tabeli routingu centrum wirtualnego na podstawie przekazanych do niego tras, a ten obiekt może być wykorzystywany do routowania ruchu w wirtualnym koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="43021-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="43021-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43021-110">PARAMETERS</span></span>

### <span data-ttu-id="43021-111">— Połączenie</span><span class="sxs-lookup"><span data-stu-id="43021-111">-Connection</span></span>
<span data-ttu-id="43021-112">Lista połączeń, do których jest dołączona ta tabela tras.</span><span class="sxs-lookup"><span data-stu-id="43021-112">List of connections this route table is attached to.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43021-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43021-113">-DefaultProfile</span></span>
<span data-ttu-id="43021-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43021-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43021-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43021-115">-Name</span></span>
<span data-ttu-id="43021-116">Nazwa tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="43021-116">Name of the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43021-117">-Route</span><span class="sxs-lookup"><span data-stu-id="43021-117">-Route</span></span>
<span data-ttu-id="43021-118">Lista tras koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="43021-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43021-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43021-119">CommonParameters</span></span>
<span data-ttu-id="43021-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43021-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43021-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43021-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43021-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43021-122">INPUTS</span></span>

### <span data-ttu-id="43021-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="43021-123">None</span></span>

## <span data-ttu-id="43021-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43021-124">OUTPUTS</span></span>

### <span data-ttu-id="43021-125">Microsoft. Azure. Commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="43021-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="43021-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43021-126">NOTES</span></span>

## <span data-ttu-id="43021-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43021-127">RELATED LINKS</span></span>
