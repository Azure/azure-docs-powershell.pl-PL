---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191970"
---
# <span data-ttu-id="985a8-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="985a8-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="985a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985a8-102">SYNOPSIS</span></span>
<span data-ttu-id="985a8-103">Pobiera skuteczną grupę zabezpieczeń sieciowych interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="985a8-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="985a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="985a8-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="985a8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="985a8-105">DESCRIPTION</span></span>
<span data-ttu-id="985a8-106">Polecenie **cmdlet Get-AzEffectiveNetworkSecurityGroup** zwraca skuteczną grupę zabezpieczeń sieciową, która jest stosowana w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="985a8-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="985a8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="985a8-107">EXAMPLES</span></span>

### <span data-ttu-id="985a8-108">Przykład 1. Uzyskiwanie efektywnej grupy zabezpieczeń sieciowych w interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="985a8-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="985a8-109">To polecenie pobiera wszystkie skuteczne reguły zabezpieczeń sieciowych skojarzone z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="985a8-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="985a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="985a8-110">PARAMETERS</span></span>

### <span data-ttu-id="985a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985a8-111">-DefaultProfile</span></span>
<span data-ttu-id="985a8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="985a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="985a8-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="985a8-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="985a8-114">Określono nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="985a8-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="985a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="985a8-116">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="985a8-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="985a8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985a8-117">CommonParameters</span></span>
<span data-ttu-id="985a8-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985a8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985a8-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="985a8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985a8-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="985a8-120">INPUTS</span></span>

### <span data-ttu-id="985a8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="985a8-121">System.String</span></span>

## <span data-ttu-id="985a8-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="985a8-122">OUTPUTS</span></span>

### <span data-ttu-id="985a8-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="985a8-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="985a8-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="985a8-124">NOTES</span></span>

## <span data-ttu-id="985a8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="985a8-125">RELATED LINKS</span></span>

[<span data-ttu-id="985a8-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="985a8-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


