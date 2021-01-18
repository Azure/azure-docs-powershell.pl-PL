---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502668"
---
# <span data-ttu-id="e9e23-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="e9e23-101">Update-AzSubscription</span></span>

## <span data-ttu-id="e9e23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9e23-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e23-103">Aktualizuje subskrypcję platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e9e23-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="e9e23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9e23-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9e23-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e23-106">Polecenie cmdlet **Update-AzSubscription** aktualizuje subskrypcję platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e9e23-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="e9e23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9e23-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e23-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9e23-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="e9e23-109">Aktualizuje subskrypcję</span><span class="sxs-lookup"><span data-stu-id="e9e23-109">Updates the subscription</span></span>

## <span data-ttu-id="e9e23-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9e23-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e23-111">-Action</span><span class="sxs-lookup"><span data-stu-id="e9e23-111">-Action</span></span>
<span data-ttu-id="e9e23-112">Akcja do wykonania w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e9e23-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="e9e23-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9e23-113">-AsJob</span></span>
<span data-ttu-id="e9e23-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e9e23-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e23-115">-DefaultProfile</span></span>
<span data-ttu-id="e9e23-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e23-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9e23-117">-Name</span></span>
<span data-ttu-id="e9e23-118">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e9e23-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e23-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e9e23-119">-SubscriptionId</span></span>
<span data-ttu-id="e9e23-120">Identyfikator subskrypcji do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="e9e23-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="e9e23-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9e23-121">-Confirm</span></span>
<span data-ttu-id="e9e23-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e23-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e23-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e23-123">-WhatIf</span></span>
<span data-ttu-id="e9e23-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e23-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e23-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9e23-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e23-126">CommonParameters</span></span>
<span data-ttu-id="e9e23-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e23-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9e23-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e23-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9e23-129">INPUTS</span></span>

### <span data-ttu-id="e9e23-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e9e23-130">None</span></span>

## <span data-ttu-id="e9e23-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9e23-131">OUTPUTS</span></span>

### <span data-ttu-id="e9e23-132">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="e9e23-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="e9e23-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9e23-133">NOTES</span></span>

## <span data-ttu-id="e9e23-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9e23-134">RELATED LINKS</span></span>
