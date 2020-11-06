---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f00a1d0c67d7bb395a328e01915f5bb0334d3d83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528077"
---
# <span data-ttu-id="420ad-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="420ad-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="420ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="420ad-102">SYNOPSIS</span></span>
<span data-ttu-id="420ad-103">Pobiera trasy z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="420ad-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="420ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="420ad-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="420ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="420ad-105">DESCRIPTION</span></span>
<span data-ttu-id="420ad-106">Polecenie cmdlet **Get-AzureRmRouteConfig** pobiera trasy z tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="420ad-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="420ad-107">Możesz określić trasę według nazwy.</span><span class="sxs-lookup"><span data-stu-id="420ad-107">You can specify a route by name.</span></span>

## <span data-ttu-id="420ad-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="420ad-108">EXAMPLES</span></span>

### <span data-ttu-id="420ad-109">Przykład 1: pobieranie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="420ad-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="420ad-110">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="420ad-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="420ad-111">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="420ad-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="420ad-112">Bieżące polecenie cmdlet pobiera trasę o nazwie Route07 w tabeli tras o nazwie RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="420ad-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="420ad-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="420ad-113">PARAMETERS</span></span>

### <span data-ttu-id="420ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420ad-114">-DefaultProfile</span></span>
<span data-ttu-id="420ad-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="420ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="420ad-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="420ad-116">-Name</span></span>
<span data-ttu-id="420ad-117">Określa nazwę trasy pobieranej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="420ad-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="420ad-118">-Routeing</span><span class="sxs-lookup"><span data-stu-id="420ad-118">-RouteTable</span></span>
<span data-ttu-id="420ad-119">Określa tabelę tras, z której ten aplet polecenia pobiera trasy.</span><span class="sxs-lookup"><span data-stu-id="420ad-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="420ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420ad-120">CommonParameters</span></span>
<span data-ttu-id="420ad-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="420ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420ad-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420ad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420ad-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="420ad-123">INPUTS</span></span>

### <span data-ttu-id="420ad-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="420ad-124">PSRouteTable</span></span>
<span data-ttu-id="420ad-125">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="420ad-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="420ad-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="420ad-126">OUTPUTS</span></span>

### <span data-ttu-id="420ad-127">Microsoft. Azure. Commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="420ad-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="420ad-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="420ad-128">NOTES</span></span>

## <span data-ttu-id="420ad-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="420ad-129">RELATED LINKS</span></span>

[<span data-ttu-id="420ad-130">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="420ad-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="420ad-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="420ad-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="420ad-132">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="420ad-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="420ad-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="420ad-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="420ad-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="420ad-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


