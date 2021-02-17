---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182851"
---
# <span data-ttu-id="4a5e1-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="4a5e1-101">Update-AzSubscription</span></span>

## <span data-ttu-id="4a5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5e1-103">Aktualizacje subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4a5e1-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="4a5e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a5e1-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a5e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="4a5e1-106">Polecenie **cmdlet Update-AzSubscription** aktualizuje subskrypcję platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4a5e1-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="4a5e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="4a5e1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a5e1-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="4a5e1-109">Aktualizuje subskrypcję</span><span class="sxs-lookup"><span data-stu-id="4a5e1-109">Updates the subscription</span></span>

## <span data-ttu-id="4a5e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a5e1-110">PARAMETERS</span></span>

### <span data-ttu-id="4a5e1-111">— akcja</span><span class="sxs-lookup"><span data-stu-id="4a5e1-111">-Action</span></span>
<span data-ttu-id="4a5e1-112">Akcja do wykonania w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4a5e1-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="4a5e1-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4a5e1-113">-AsJob</span></span>
<span data-ttu-id="4a5e1-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4a5e1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a5e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5e1-115">-DefaultProfile</span></span>
<span data-ttu-id="4a5e1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a5e1-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4a5e1-117">-Name</span></span>
<span data-ttu-id="4a5e1-118">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4a5e1-118">Name of the subscription</span></span>

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

### <span data-ttu-id="4a5e1-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a5e1-119">-SubscriptionId</span></span>
<span data-ttu-id="4a5e1-120">Identyfikator subskrypcji do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="4a5e1-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="4a5e1-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a5e1-121">-Confirm</span></span>
<span data-ttu-id="4a5e1-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4a5e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5e1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5e1-123">-WhatIf</span></span>
<span data-ttu-id="4a5e1-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a5e1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a5e1-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4a5e1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a5e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5e1-126">CommonParameters</span></span>
<span data-ttu-id="4a5e1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a5e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5e1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a5e1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5e1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a5e1-129">INPUTS</span></span>

### <span data-ttu-id="4a5e1-130">Brak</span><span class="sxs-lookup"><span data-stu-id="4a5e1-130">None</span></span>

## <span data-ttu-id="4a5e1-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a5e1-131">OUTPUTS</span></span>

### <span data-ttu-id="4a5e1-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="4a5e1-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="4a5e1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a5e1-133">NOTES</span></span>

## <span data-ttu-id="4a5e1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a5e1-134">RELATED LINKS</span></span>
