---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502067"
---
# <span data-ttu-id="2e0f7-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="2e0f7-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="2e0f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0f7-103">Wyświetlanie listy kluczy interfejsu API dla węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="2e0f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e0f7-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2e0f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e0f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2e0f7-106">Wyświetlanie listy kluczy interfejsu API dla węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="2e0f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e0f7-107">EXAMPLES</span></span>

### <span data-ttu-id="2e0f7-108">Przykład 1: Lista kluczy interfejsu API dla węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="2e0f7-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="2e0f7-109">To polecenie wyświetla listę kluczy interfejsu API dla węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="2e0f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e0f7-110">PARAMETERS</span></span>

### <span data-ttu-id="2e0f7-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="2e0f7-111">-BlockchainMemberName</span></span>
<span data-ttu-id="2e0f7-112">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="2e0f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0f7-113">-DefaultProfile</span></span>
<span data-ttu-id="2e0f7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e0f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e0f7-116">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2e0f7-117">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2e0f7-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2e0f7-118">-SubscriptionId</span></span>
<span data-ttu-id="2e0f7-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e0f7-120">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2e0f7-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="2e0f7-121">-TransactionNodeName</span></span>
<span data-ttu-id="2e0f7-122">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-122">Transaction node name.</span></span>

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

### <span data-ttu-id="2e0f7-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e0f7-123">-Confirm</span></span>
<span data-ttu-id="2e0f7-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e0f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e0f7-125">-WhatIf</span></span>
<span data-ttu-id="2e0f7-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e0f7-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e0f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0f7-128">CommonParameters</span></span>
<span data-ttu-id="2e0f7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e0f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0f7-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e0f7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0f7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e0f7-131">INPUTS</span></span>

## <span data-ttu-id="2e0f7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e0f7-132">OUTPUTS</span></span>

### <span data-ttu-id="2e0f7-133">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="2e0f7-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="2e0f7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e0f7-134">NOTES</span></span>

<span data-ttu-id="2e0f7-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2e0f7-135">ALIASES</span></span>

## <span data-ttu-id="2e0f7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e0f7-136">RELATED LINKS</span></span>

