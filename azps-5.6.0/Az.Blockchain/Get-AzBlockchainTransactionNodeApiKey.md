---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: dbde273c1694f4622904ac00b261e902036c6e03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971457"
---
# <span data-ttu-id="b13bc-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="b13bc-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="b13bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b13bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b13bc-103">Lista kluczy interfejsu API węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b13bc-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="b13bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b13bc-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b13bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b13bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b13bc-106">Lista kluczy interfejsu API węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b13bc-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="b13bc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b13bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b13bc-108">Przykład 1. Klucze interfejsu Api listy dla węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="b13bc-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="b13bc-109">To polecenie zawiera listę kluczy interfejsu Api dla węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b13bc-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="b13bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b13bc-110">PARAMETERS</span></span>

### <span data-ttu-id="b13bc-111">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="b13bc-111">-BlockchainMemberName</span></span>
<span data-ttu-id="b13bc-112">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b13bc-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="b13bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13bc-113">-DefaultProfile</span></span>
<span data-ttu-id="b13bc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b13bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b13bc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13bc-115">-ResourceGroupName</span></span>
<span data-ttu-id="b13bc-116">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="b13bc-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b13bc-117">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b13bc-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b13bc-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b13bc-118">-SubscriptionId</span></span>
<span data-ttu-id="b13bc-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b13bc-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b13bc-120">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="b13bc-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b13bc-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="b13bc-121">-TransactionNodeName</span></span>
<span data-ttu-id="b13bc-122">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b13bc-122">Transaction node name.</span></span>

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

### <span data-ttu-id="b13bc-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b13bc-123">-Confirm</span></span>
<span data-ttu-id="b13bc-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b13bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13bc-125">-WhatIf</span></span>
<span data-ttu-id="b13bc-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13bc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13bc-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b13bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13bc-128">CommonParameters</span></span>
<span data-ttu-id="b13bc-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13bc-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b13bc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13bc-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b13bc-131">INPUTS</span></span>

## <span data-ttu-id="b13bc-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b13bc-132">OUTPUTS</span></span>

### <span data-ttu-id="b13bc-133">Microsoft.Azure.PowerShell.cmdlet.u7.models.api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="b13bc-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="b13bc-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b13bc-134">NOTES</span></span>

<span data-ttu-id="b13bc-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b13bc-135">ALIASES</span></span>

## <span data-ttu-id="b13bc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b13bc-136">RELATED LINKS</span></span>

