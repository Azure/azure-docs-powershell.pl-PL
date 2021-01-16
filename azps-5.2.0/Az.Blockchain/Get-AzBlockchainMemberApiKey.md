---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334021"
---
# <span data-ttu-id="2055f-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="2055f-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="2055f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2055f-102">SYNOPSIS</span></span>
<span data-ttu-id="2055f-103">Wyświetla listę kluczy interfejsu API elementu członkowskiego Blockchain.</span><span class="sxs-lookup"><span data-stu-id="2055f-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="2055f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2055f-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2055f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2055f-105">DESCRIPTION</span></span>
<span data-ttu-id="2055f-106">Wyświetla listę kluczy interfejsu API elementu członkowskiego Blockchain.</span><span class="sxs-lookup"><span data-stu-id="2055f-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="2055f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2055f-107">EXAMPLES</span></span>

### <span data-ttu-id="2055f-108">Przykład 1: Lista kluczy API Blockchain</span><span class="sxs-lookup"><span data-stu-id="2055f-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="2055f-109">To polecenie wyświetla listę kluczy interfejsu API dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="2055f-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="2055f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2055f-110">PARAMETERS</span></span>

### <span data-ttu-id="2055f-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="2055f-111">-BlockchainMemberName</span></span>
<span data-ttu-id="2055f-112">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="2055f-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="2055f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2055f-113">-DefaultProfile</span></span>
<span data-ttu-id="2055f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2055f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2055f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2055f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2055f-116">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="2055f-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2055f-117">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="2055f-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2055f-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2055f-118">-SubscriptionId</span></span>
<span data-ttu-id="2055f-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2055f-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2055f-120">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="2055f-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2055f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2055f-121">-Confirm</span></span>
<span data-ttu-id="2055f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2055f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2055f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2055f-123">-WhatIf</span></span>
<span data-ttu-id="2055f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2055f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2055f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2055f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2055f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2055f-126">CommonParameters</span></span>
<span data-ttu-id="2055f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2055f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2055f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2055f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2055f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2055f-129">INPUTS</span></span>

## <span data-ttu-id="2055f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2055f-130">OUTPUTS</span></span>

### <span data-ttu-id="2055f-131">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="2055f-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="2055f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2055f-132">NOTES</span></span>

<span data-ttu-id="2055f-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2055f-133">ALIASES</span></span>

## <span data-ttu-id="2055f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2055f-134">RELATED LINKS</span></span>

