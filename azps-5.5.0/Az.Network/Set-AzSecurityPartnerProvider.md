---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240563"
---
# <span data-ttu-id="eb3cf-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="eb3cf-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="eb3cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3cf-103">Umożliwia zapisanie zmodyfikowanego narzędzia Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="eb3cf-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="eb3cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb3cf-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb3cf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb3cf-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3cf-106">Polecenie **cmdlet Set-AzSecurityPartnerProvider** aktualizuje narzędzie Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="eb3cf-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="eb3cf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb3cf-107">EXAMPLES</span></span>

### <span data-ttu-id="eb3cf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb3cf-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="eb3cf-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb3cf-109">PARAMETERS</span></span>

### <span data-ttu-id="eb3cf-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="eb3cf-110">-AsJob</span></span>
<span data-ttu-id="eb3cf-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="eb3cf-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb3cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3cf-112">-DefaultProfile</span></span>
<span data-ttu-id="eb3cf-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3cf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb3cf-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="eb3cf-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="eb3cf-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="eb3cf-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="eb3cf-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb3cf-116">-Confirm</span></span>
<span data-ttu-id="eb3cf-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eb3cf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb3cf-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb3cf-118">-WhatIf</span></span>
<span data-ttu-id="eb3cf-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb3cf-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb3cf-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eb3cf-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb3cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3cf-121">CommonParameters</span></span>
<span data-ttu-id="eb3cf-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb3cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3cf-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb3cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3cf-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb3cf-124">INPUTS</span></span>

### <span data-ttu-id="eb3cf-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="eb3cf-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="eb3cf-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb3cf-126">OUTPUTS</span></span>

### <span data-ttu-id="eb3cf-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="eb3cf-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="eb3cf-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb3cf-128">NOTES</span></span>

## <span data-ttu-id="eb3cf-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb3cf-129">RELATED LINKS</span></span>
