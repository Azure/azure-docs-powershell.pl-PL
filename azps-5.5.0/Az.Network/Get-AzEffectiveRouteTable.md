---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191963"
---
# <span data-ttu-id="e4d1f-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4d1f-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="e4d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d1f-103">Pobiera skuteczną tabelę tras w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="e4d1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4d1f-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4d1f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="e4d1f-106">Polecenie **cmdlet Get-AzEffectiveRouteTable** zwraca efektywną tabelę trasy, która jest stosowana w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="e4d1f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4d1f-107">EXAMPLES</span></span>

### <span data-ttu-id="e4d1f-108">Przykład 1. Uzyskiwanie efektywnej tabeli tras w interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="e4d1f-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e4d1f-109">To polecenie pobiera efektywną tabelę tras skojarzoną z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e4d1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4d1f-110">PARAMETERS</span></span>

### <span data-ttu-id="e4d1f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e4d1f-111">-AsJob</span></span>
<span data-ttu-id="e4d1f-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e4d1f-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d1f-113">-DefaultProfile</span></span>
<span data-ttu-id="e4d1f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4d1f-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e4d1f-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="e4d1f-116">Określono nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="e4d1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4d1f-118">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="e4d1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d1f-119">CommonParameters</span></span>
<span data-ttu-id="e4d1f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d1f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4d1f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d1f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4d1f-122">INPUTS</span></span>

### <span data-ttu-id="e4d1f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e4d1f-123">System.String</span></span>

## <span data-ttu-id="e4d1f-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4d1f-124">OUTPUTS</span></span>

### <span data-ttu-id="e4d1f-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="e4d1f-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="e4d1f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4d1f-126">NOTES</span></span>

## <span data-ttu-id="e4d1f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4d1f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e4d1f-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4d1f-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


