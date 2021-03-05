---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 0a9ed100121c0f6610bcb019571fd1779f28dff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010305"
---
# <span data-ttu-id="a161f-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a161f-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="a161f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a161f-102">SYNOPSIS</span></span>
<span data-ttu-id="a161f-103">Umożliwia zapisanie zmodyfikowanego narzędzia Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="a161f-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="a161f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a161f-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a161f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a161f-105">DESCRIPTION</span></span>
<span data-ttu-id="a161f-106">Polecenie **cmdlet Set-AzSecurityPartnerProvider** aktualizuje narzędzie Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a161f-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="a161f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a161f-107">EXAMPLES</span></span>

### <span data-ttu-id="a161f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a161f-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="a161f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a161f-109">PARAMETERS</span></span>

### <span data-ttu-id="a161f-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a161f-110">-AsJob</span></span>
<span data-ttu-id="a161f-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a161f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a161f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a161f-112">-DefaultProfile</span></span>
<span data-ttu-id="a161f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a161f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a161f-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a161f-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="a161f-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a161f-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a161f-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a161f-116">-Confirm</span></span>
<span data-ttu-id="a161f-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a161f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a161f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a161f-118">-WhatIf</span></span>
<span data-ttu-id="a161f-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a161f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a161f-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a161f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a161f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a161f-121">CommonParameters</span></span>
<span data-ttu-id="a161f-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a161f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a161f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a161f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a161f-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a161f-124">INPUTS</span></span>

### <span data-ttu-id="a161f-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a161f-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="a161f-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a161f-126">OUTPUTS</span></span>

### <span data-ttu-id="a161f-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a161f-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="a161f-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a161f-128">NOTES</span></span>

## <span data-ttu-id="a161f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a161f-129">RELATED LINKS</span></span>
