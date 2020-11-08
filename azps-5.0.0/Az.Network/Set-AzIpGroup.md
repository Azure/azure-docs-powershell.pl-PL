---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232065"
---
# <span data-ttu-id="57ff3-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="57ff3-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="57ff3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="57ff3-103">Umożliwia zapisanie zmodyfikowanej zapory.</span><span class="sxs-lookup"><span data-stu-id="57ff3-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="57ff3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57ff3-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57ff3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="57ff3-106">Polecenie cmdlet **Set-AzIpGroup** aktualizuje platformę Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="57ff3-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="57ff3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57ff3-107">EXAMPLES</span></span>

### <span data-ttu-id="57ff3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57ff3-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="57ff3-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57ff3-109">PARAMETERS</span></span>

### <span data-ttu-id="57ff3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57ff3-110">-AsJob</span></span>
<span data-ttu-id="57ff3-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57ff3-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ff3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ff3-112">-DefaultProfile</span></span>
<span data-ttu-id="57ff3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57ff3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ff3-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="57ff3-114">-IpGroup</span></span>
<span data-ttu-id="57ff3-115">IpGroup</span><span class="sxs-lookup"><span data-stu-id="57ff3-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57ff3-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57ff3-116">-Confirm</span></span>
<span data-ttu-id="57ff3-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57ff3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ff3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ff3-118">-WhatIf</span></span>
<span data-ttu-id="57ff3-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57ff3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ff3-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57ff3-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ff3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ff3-121">CommonParameters</span></span>
<span data-ttu-id="57ff3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ff3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ff3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57ff3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ff3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ff3-124">INPUTS</span></span>

### <span data-ttu-id="57ff3-125">Microsoft. Azure. Commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="57ff3-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="57ff3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57ff3-126">OUTPUTS</span></span>

### <span data-ttu-id="57ff3-127">Microsoft. Azure. Commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="57ff3-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="57ff3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57ff3-128">NOTES</span></span>

## <span data-ttu-id="57ff3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57ff3-129">RELATED LINKS</span></span>
