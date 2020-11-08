---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219549"
---
# <span data-ttu-id="00d66-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="00d66-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="00d66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00d66-102">SYNOPSIS</span></span>
<span data-ttu-id="00d66-103">Pobiera efektywną tabelę tras dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="00d66-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="00d66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00d66-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00d66-105">DESCRIPTION</span></span>
<span data-ttu-id="00d66-106">Polecenie cmdlet **Get-AzEffectiveRouteTable** zwraca tabelę efektywnej trasy zastosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="00d66-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="00d66-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00d66-107">EXAMPLES</span></span>

### <span data-ttu-id="00d66-108">Przykład 1: uzyskiwanie efektywnej tabeli routingu na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="00d66-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="00d66-109">To polecenie pobiera efektywną tabelę tras skojarzoną z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="00d66-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="00d66-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00d66-110">PARAMETERS</span></span>

### <span data-ttu-id="00d66-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00d66-111">-AsJob</span></span>
<span data-ttu-id="00d66-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="00d66-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00d66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d66-113">-DefaultProfile</span></span>
<span data-ttu-id="00d66-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00d66-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d66-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="00d66-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="00d66-116">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="00d66-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="00d66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d66-117">-ResourceGroupName</span></span>
<span data-ttu-id="00d66-118">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="00d66-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="00d66-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d66-119">CommonParameters</span></span>
<span data-ttu-id="00d66-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d66-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d66-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00d66-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d66-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00d66-122">INPUTS</span></span>

### <span data-ttu-id="00d66-123">System. String</span><span class="sxs-lookup"><span data-stu-id="00d66-123">System.String</span></span>

## <span data-ttu-id="00d66-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00d66-124">OUTPUTS</span></span>

### <span data-ttu-id="00d66-125">Microsoft. Azure. Commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="00d66-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="00d66-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00d66-126">NOTES</span></span>

## <span data-ttu-id="00d66-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00d66-127">RELATED LINKS</span></span>

[<span data-ttu-id="00d66-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="00d66-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


