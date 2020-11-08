---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062956"
---
# <span data-ttu-id="5b021-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="5b021-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="5b021-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b021-102">SYNOPSIS</span></span>
<span data-ttu-id="5b021-103">Wyświetla listę dostępnych konsorcjów dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5b021-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="5b021-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b021-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b021-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b021-105">DESCRIPTION</span></span>
<span data-ttu-id="5b021-106">Wyświetla listę dostępnych konsorcjów dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5b021-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="5b021-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b021-107">EXAMPLES</span></span>

### <span data-ttu-id="5b021-108">Przykład 1: Uzyskaj Blockchain konsorcjum.</span><span class="sxs-lookup"><span data-stu-id="5b021-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="5b021-109">To polecenie wyświetla listę konsorcjów w ramach abonamentu dla konkretnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5b021-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="5b021-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b021-110">PARAMETERS</span></span>

### <span data-ttu-id="5b021-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b021-111">-DefaultProfile</span></span>
<span data-ttu-id="5b021-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b021-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b021-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5b021-113">-Location</span></span>
<span data-ttu-id="5b021-114">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5b021-114">Location Name.</span></span>

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

### <span data-ttu-id="5b021-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5b021-115">-SubscriptionId</span></span>
<span data-ttu-id="5b021-116">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b021-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b021-117">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="5b021-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5b021-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b021-118">-Confirm</span></span>
<span data-ttu-id="5b021-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b021-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b021-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b021-120">-WhatIf</span></span>
<span data-ttu-id="5b021-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b021-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b021-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5b021-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b021-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b021-123">CommonParameters</span></span>
<span data-ttu-id="5b021-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b021-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b021-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b021-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b021-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b021-126">INPUTS</span></span>

## <span data-ttu-id="5b021-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b021-127">OUTPUTS</span></span>

### <span data-ttu-id="5b021-128">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="5b021-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="5b021-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b021-129">NOTES</span></span>

<span data-ttu-id="5b021-130">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5b021-130">ALIASES</span></span>

## <span data-ttu-id="5b021-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b021-131">RELATED LINKS</span></span>

