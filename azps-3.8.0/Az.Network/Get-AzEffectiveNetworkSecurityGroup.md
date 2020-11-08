---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053835"
---
# <span data-ttu-id="0e0e0-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e0e0-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="0e0e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0e0-103">Pobiera skuteczną grupę zabezpieczeń sieci interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="0e0e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e0e0-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e0e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e0e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0e0e0-106">Polecenie cmdlet **Get-AzEffectiveNetworkSecurityGroup** zwraca skuteczną grupę zabezpieczeń sieci stosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="0e0e0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e0e0-107">EXAMPLES</span></span>

### <span data-ttu-id="0e0e0-108">Przykład 1: uzyskiwanie efektywnej grupy zabezpieczeń sieci na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="0e0e0-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="0e0e0-109">To polecenie pobiera wszystkie efektywne reguły zabezpieczeń sieci skojarzone z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie moja grupa.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="0e0e0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e0e0-110">PARAMETERS</span></span>

### <span data-ttu-id="0e0e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0e0-111">-DefaultProfile</span></span>
<span data-ttu-id="0e0e0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0e0-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0e0e0-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="0e0e0-114">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-114">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="0e0e0-116">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0e0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0e0-117">CommonParameters</span></span>
<span data-ttu-id="0e0e0-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e0e0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0e0-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e0e0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0e0-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e0e0-120">INPUTS</span></span>

### <span data-ttu-id="0e0e0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0e0e0-121">System.String</span></span>

## <span data-ttu-id="0e0e0-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e0e0-122">OUTPUTS</span></span>

### <span data-ttu-id="0e0e0-123">Microsoft. Azure. Commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0e0e0-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="0e0e0-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e0e0-124">NOTES</span></span>

## <span data-ttu-id="0e0e0-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e0e0-125">RELATED LINKS</span></span>

[<span data-ttu-id="0e0e0-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e0e0-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


