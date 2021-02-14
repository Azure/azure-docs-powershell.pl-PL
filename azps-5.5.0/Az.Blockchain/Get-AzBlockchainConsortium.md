---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181970"
---
# <span data-ttu-id="c260b-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="c260b-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="c260b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c260b-102">SYNOPSIS</span></span>
<span data-ttu-id="c260b-103">Zawiera listę dostępnych przedsiębiorstw w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c260b-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="c260b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c260b-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c260b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c260b-105">DESCRIPTION</span></span>
<span data-ttu-id="c260b-106">Zawiera listę dostępnych przedsiębiorstw w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c260b-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="c260b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c260b-107">EXAMPLES</span></span>

### <span data-ttu-id="c260b-108">Przykład 1. Uzyskaj więcej organizacji.</span><span class="sxs-lookup"><span data-stu-id="c260b-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="c260b-109">To polecenie wyświetla listę organizacji w ramach subskrypcji dla określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c260b-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="c260b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c260b-110">PARAMETERS</span></span>

### <span data-ttu-id="c260b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c260b-111">-DefaultProfile</span></span>
<span data-ttu-id="c260b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c260b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c260b-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c260b-113">-Location</span></span>
<span data-ttu-id="c260b-114">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c260b-114">Location Name.</span></span>

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

### <span data-ttu-id="c260b-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c260b-115">-SubscriptionId</span></span>
<span data-ttu-id="c260b-116">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c260b-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c260b-117">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="c260b-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c260b-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c260b-118">-Confirm</span></span>
<span data-ttu-id="c260b-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c260b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c260b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c260b-120">-WhatIf</span></span>
<span data-ttu-id="c260b-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c260b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c260b-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c260b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c260b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c260b-123">CommonParameters</span></span>
<span data-ttu-id="c260b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c260b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c260b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c260b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c260b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c260b-126">INPUTS</span></span>

## <span data-ttu-id="c260b-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c260b-127">OUTPUTS</span></span>

### <span data-ttu-id="c260b-128">Microsoft.Azure.PowerShell.cmdlet.u20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="c260b-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="c260b-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c260b-129">NOTES</span></span>

<span data-ttu-id="c260b-130">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c260b-130">ALIASES</span></span>

## <span data-ttu-id="c260b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c260b-131">RELATED LINKS</span></span>

