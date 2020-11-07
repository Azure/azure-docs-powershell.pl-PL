---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890794"
---
# <span data-ttu-id="82ccb-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82ccb-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="82ccb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="82ccb-103">Pobiera moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="82ccb-103">Gets a load balancer.</span></span>

## <span data-ttu-id="82ccb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82ccb-104">SYNTAX</span></span>

### <span data-ttu-id="82ccb-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="82ccb-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82ccb-106">Większa</span><span class="sxs-lookup"><span data-stu-id="82ccb-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ccb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82ccb-107">DESCRIPTION</span></span>
<span data-ttu-id="82ccb-108">Polecenie cmdlet **Get-AzLoadBalancer** pobiera jeden lub więcej modułów równoważenia obciążenia platformy Azure, które znajdują się w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="82ccb-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="82ccb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82ccb-109">EXAMPLES</span></span>

### <span data-ttu-id="82ccb-110">Przykład 1: uzyskiwanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="82ccb-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="82ccb-111">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="82ccb-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="82ccb-112">Aby można było uruchomić to polecenie cmdlet, musi istnieć moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="82ccb-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="82ccb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82ccb-113">PARAMETERS</span></span>

### <span data-ttu-id="82ccb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ccb-114">-DefaultProfile</span></span>
<span data-ttu-id="82ccb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82ccb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ccb-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="82ccb-116">-ExpandResource</span></span>
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

### <span data-ttu-id="82ccb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82ccb-117">-Name</span></span>
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

### <span data-ttu-id="82ccb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ccb-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="82ccb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ccb-119">CommonParameters</span></span>
<span data-ttu-id="82ccb-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ccb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ccb-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ccb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ccb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82ccb-122">INPUTS</span></span>

## <span data-ttu-id="82ccb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82ccb-123">OUTPUTS</span></span>

### <span data-ttu-id="82ccb-124">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82ccb-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="82ccb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82ccb-125">NOTES</span></span>

## <span data-ttu-id="82ccb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82ccb-126">RELATED LINKS</span></span>

[<span data-ttu-id="82ccb-127">Nowe — AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82ccb-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="82ccb-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82ccb-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="82ccb-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82ccb-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


