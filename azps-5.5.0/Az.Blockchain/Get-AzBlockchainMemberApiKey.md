---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177962"
---
# <span data-ttu-id="18ffb-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="18ffb-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="18ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="18ffb-103">Wyświetla listę kluczy interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="18ffb-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="18ffb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="18ffb-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18ffb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="18ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="18ffb-106">Wyświetla listę kluczy interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="18ffb-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="18ffb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="18ffb-107">EXAMPLES</span></span>

### <span data-ttu-id="18ffb-108">Przykład 1. Lista kluczy interfejsu API</span><span class="sxs-lookup"><span data-stu-id="18ffb-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="18ffb-109">To polecenie zawiera listę kluczy interfejsu Api dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="18ffb-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="18ffb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18ffb-110">PARAMETERS</span></span>

### <span data-ttu-id="18ffb-111">-Nawiązywane NazwyMemberów</span><span class="sxs-lookup"><span data-stu-id="18ffb-111">-BlockchainMemberName</span></span>
<span data-ttu-id="18ffb-112">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18ffb-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="18ffb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ffb-113">-DefaultProfile</span></span>
<span data-ttu-id="18ffb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="18ffb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18ffb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ffb-115">-ResourceGroupName</span></span>
<span data-ttu-id="18ffb-116">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="18ffb-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="18ffb-117">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="18ffb-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="18ffb-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18ffb-118">-SubscriptionId</span></span>
<span data-ttu-id="18ffb-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18ffb-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="18ffb-120">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="18ffb-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="18ffb-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18ffb-121">-Confirm</span></span>
<span data-ttu-id="18ffb-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="18ffb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ffb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ffb-123">-WhatIf</span></span>
<span data-ttu-id="18ffb-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ffb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18ffb-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="18ffb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ffb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ffb-126">CommonParameters</span></span>
<span data-ttu-id="18ffb-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ffb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ffb-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18ffb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ffb-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18ffb-129">INPUTS</span></span>

## <span data-ttu-id="18ffb-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18ffb-130">OUTPUTS</span></span>

### <span data-ttu-id="18ffb-131">Microsoft.Azure.PowerShell.cmdlet.u20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="18ffb-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="18ffb-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="18ffb-132">NOTES</span></span>

<span data-ttu-id="18ffb-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="18ffb-133">ALIASES</span></span>

## <span data-ttu-id="18ffb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18ffb-134">RELATED LINKS</span></span>

