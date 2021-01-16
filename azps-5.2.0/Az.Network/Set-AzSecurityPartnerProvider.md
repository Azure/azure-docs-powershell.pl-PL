---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357497"
---
# <span data-ttu-id="ab152-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab152-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ab152-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab152-102">SYNOPSIS</span></span>
<span data-ttu-id="ab152-103">Zapisuje zmodyfikowaną usługę Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="ab152-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="ab152-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab152-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab152-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab152-105">DESCRIPTION</span></span>
<span data-ttu-id="ab152-106">Polecenie cmdlet **Set-AzSecurityPartnerProvider** aktualizuje platformę Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab152-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ab152-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab152-107">EXAMPLES</span></span>

### <span data-ttu-id="ab152-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab152-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="ab152-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab152-109">PARAMETERS</span></span>

### <span data-ttu-id="ab152-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab152-110">-AsJob</span></span>
<span data-ttu-id="ab152-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ab152-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab152-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab152-112">-DefaultProfile</span></span>
<span data-ttu-id="ab152-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab152-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab152-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab152-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="ab152-115">SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab152-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="ab152-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab152-116">-Confirm</span></span>
<span data-ttu-id="ab152-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab152-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab152-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab152-118">-WhatIf</span></span>
<span data-ttu-id="ab152-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab152-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab152-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab152-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab152-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab152-121">CommonParameters</span></span>
<span data-ttu-id="ab152-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab152-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab152-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab152-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab152-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab152-124">INPUTS</span></span>

### <span data-ttu-id="ab152-125">Microsoft. Azure. Commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab152-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ab152-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab152-126">OUTPUTS</span></span>

### <span data-ttu-id="ab152-127">Microsoft. Azure. Commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ab152-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ab152-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab152-128">NOTES</span></span>

## <span data-ttu-id="ab152-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab152-129">RELATED LINKS</span></span>
