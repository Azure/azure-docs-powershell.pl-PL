---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890686"
---
# <span data-ttu-id="21c88-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21c88-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="21c88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21c88-102">SYNOPSIS</span></span>
<span data-ttu-id="21c88-103">Pobiera trasy z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="21c88-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="21c88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21c88-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21c88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21c88-105">DESCRIPTION</span></span>
<span data-ttu-id="21c88-106">Polecenie cmdlet **Get-AzRouteConfig** pobiera trasy z tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21c88-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="21c88-107">Możesz określić trasę według nazwy.</span><span class="sxs-lookup"><span data-stu-id="21c88-107">You can specify a route by name.</span></span>

## <span data-ttu-id="21c88-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21c88-108">EXAMPLES</span></span>

### <span data-ttu-id="21c88-109">Przykład 1: pobieranie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="21c88-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="21c88-110">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="21c88-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="21c88-111">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="21c88-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="21c88-112">Bieżące polecenie cmdlet pobiera trasę o nazwie Route07 w tabeli tras o nazwie RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="21c88-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="21c88-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21c88-113">PARAMETERS</span></span>

### <span data-ttu-id="21c88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c88-114">-DefaultProfile</span></span>
<span data-ttu-id="21c88-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21c88-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21c88-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21c88-116">-Name</span></span>
<span data-ttu-id="21c88-117">Określa nazwę trasy pobieranej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c88-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="21c88-118">-Routeing</span><span class="sxs-lookup"><span data-stu-id="21c88-118">-RouteTable</span></span>
<span data-ttu-id="21c88-119">Określa tabelę tras, z której ten aplet polecenia pobiera trasy.</span><span class="sxs-lookup"><span data-stu-id="21c88-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="21c88-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c88-120">CommonParameters</span></span>
<span data-ttu-id="21c88-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c88-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c88-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c88-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c88-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21c88-123">INPUTS</span></span>

### <span data-ttu-id="21c88-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="21c88-124">PSRouteTable</span></span>
<span data-ttu-id="21c88-125">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="21c88-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="21c88-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21c88-126">OUTPUTS</span></span>

### <span data-ttu-id="21c88-127">Microsoft. Azure. Commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="21c88-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="21c88-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21c88-128">NOTES</span></span>

## <span data-ttu-id="21c88-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21c88-129">RELATED LINKS</span></span>

[<span data-ttu-id="21c88-130">Dodaj-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21c88-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="21c88-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="21c88-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="21c88-132">Nowe — AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21c88-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="21c88-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21c88-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="21c88-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="21c88-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


