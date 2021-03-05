---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967921"
---
# <span data-ttu-id="10a18-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10a18-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="10a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a18-102">SYNOPSIS</span></span>
<span data-ttu-id="10a18-103">Pobiera skuteczną grupę zabezpieczeń sieciowych interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10a18-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="10a18-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10a18-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10a18-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="10a18-105">DESCRIPTION</span></span>
<span data-ttu-id="10a18-106">Polecenie **cmdlet Get-AzEffectiveNetworkSecurityGroup** zwraca efektywną grupę zabezpieczeń sieciową, która jest stosowana w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="10a18-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="10a18-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10a18-107">EXAMPLES</span></span>

### <span data-ttu-id="10a18-108">Przykład 1. Uzyskiwanie efektywnej grupy zabezpieczeń sieciowych w interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="10a18-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="10a18-109">To polecenie pobiera wszystkie skuteczne reguły zabezpieczeń sieci skojarzone z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="10a18-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="10a18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10a18-110">PARAMETERS</span></span>

### <span data-ttu-id="10a18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a18-111">-DefaultProfile</span></span>
<span data-ttu-id="10a18-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10a18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a18-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="10a18-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="10a18-114">Określono nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10a18-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="10a18-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a18-115">-ResourceGroupName</span></span>
<span data-ttu-id="10a18-116">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10a18-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="10a18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a18-117">CommonParameters</span></span>
<span data-ttu-id="10a18-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a18-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10a18-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a18-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10a18-120">INPUTS</span></span>

### <span data-ttu-id="10a18-121">System.String</span><span class="sxs-lookup"><span data-stu-id="10a18-121">System.String</span></span>

## <span data-ttu-id="10a18-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10a18-122">OUTPUTS</span></span>

### <span data-ttu-id="10a18-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10a18-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="10a18-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10a18-124">NOTES</span></span>

## <span data-ttu-id="10a18-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10a18-125">RELATED LINKS</span></span>

[<span data-ttu-id="10a18-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="10a18-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


