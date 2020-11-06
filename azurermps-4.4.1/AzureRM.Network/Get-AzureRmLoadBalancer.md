---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 764d26c2b0b95b74277fc74dab03fe55d12261f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549959"
---
# <span data-ttu-id="c2076-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2076-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="c2076-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2076-102">SYNOPSIS</span></span>
<span data-ttu-id="c2076-103">Pobiera moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2076-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2076-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2076-104">SYNTAX</span></span>

### <span data-ttu-id="c2076-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="c2076-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2076-106">Większa</span><span class="sxs-lookup"><span data-stu-id="c2076-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2076-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2076-107">DESCRIPTION</span></span>
<span data-ttu-id="c2076-108">Polecenie cmdlet **Get-AzureRmLoadBalancer** pobiera jeden lub więcej modułów równoważenia obciążenia platformy Azure, które znajdują się w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2076-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="c2076-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2076-109">EXAMPLES</span></span>

### <span data-ttu-id="c2076-110">Przykład 1: uzyskiwanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c2076-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c2076-111">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="c2076-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="c2076-112">Aby można było uruchomić to polecenie cmdlet, musi istnieć moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2076-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="c2076-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2076-113">PARAMETERS</span></span>

### <span data-ttu-id="c2076-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c2076-114">-ExpandResource</span></span>
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

### <span data-ttu-id="c2076-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2076-115">-Name</span></span>
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

### <span data-ttu-id="c2076-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2076-116">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c2076-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2076-117">-DefaultProfile</span></span>
<span data-ttu-id="c2076-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2076-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2076-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2076-119">CommonParameters</span></span>
<span data-ttu-id="c2076-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2076-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2076-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2076-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2076-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2076-122">INPUTS</span></span>

## <span data-ttu-id="c2076-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2076-123">OUTPUTS</span></span>

### <span data-ttu-id="c2076-124">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2076-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c2076-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2076-125">NOTES</span></span>

## <span data-ttu-id="c2076-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2076-126">RELATED LINKS</span></span>

[<span data-ttu-id="c2076-127">Nowe — AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2076-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="c2076-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2076-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="c2076-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c2076-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


