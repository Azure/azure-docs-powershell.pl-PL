---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: 077b1f18e18fbf47d8c89d02c44722c0a1561dac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954890"
---
# <span data-ttu-id="f3115-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="f3115-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="f3115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3115-102">SYNOPSIS</span></span>
<span data-ttu-id="f3115-103">Zawiera listę dostępnych przedsiębiorstw w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f3115-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="f3115-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3115-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3115-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3115-105">DESCRIPTION</span></span>
<span data-ttu-id="f3115-106">Zawiera listę dostępnych przedsiębiorstw w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f3115-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="f3115-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3115-107">EXAMPLES</span></span>

### <span data-ttu-id="f3115-108">Przykład 1. Uzyskaj więcej organizacji.</span><span class="sxs-lookup"><span data-stu-id="f3115-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="f3115-109">To polecenie wyświetla listę przedsiębiorstw w ramach subskrypcji dla określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f3115-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="f3115-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3115-110">PARAMETERS</span></span>

### <span data-ttu-id="f3115-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3115-111">-DefaultProfile</span></span>
<span data-ttu-id="f3115-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3115-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3115-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f3115-113">-Location</span></span>
<span data-ttu-id="f3115-114">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f3115-114">Location Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3115-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3115-115">-SubscriptionId</span></span>
<span data-ttu-id="f3115-116">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3115-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f3115-117">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f3115-117">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3115-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3115-118">-Confirm</span></span>
<span data-ttu-id="f3115-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f3115-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3115-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3115-120">-WhatIf</span></span>
<span data-ttu-id="f3115-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3115-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3115-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f3115-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3115-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3115-123">CommonParameters</span></span>
<span data-ttu-id="f3115-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3115-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3115-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3115-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3115-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3115-126">INPUTS</span></span>

## <span data-ttu-id="f3115-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3115-127">OUTPUTS</span></span>

### <span data-ttu-id="f3115-128">Microsoft.Azure.PowerShell.cmdlet.u7.models.api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="f3115-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="f3115-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3115-129">NOTES</span></span>

<span data-ttu-id="f3115-130">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f3115-130">ALIASES</span></span>

## <span data-ttu-id="f3115-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3115-131">RELATED LINKS</span></span>

