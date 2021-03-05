---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013226"
---
# <span data-ttu-id="857f5-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="857f5-101">New-AzHealthBot</span></span>

## <span data-ttu-id="857f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="857f5-102">SYNOPSIS</span></span>
<span data-ttu-id="857f5-103">Utwórz nowy robot HealthBot.</span><span class="sxs-lookup"><span data-stu-id="857f5-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="857f5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="857f5-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="857f5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="857f5-105">DESCRIPTION</span></span>
<span data-ttu-id="857f5-106">Utwórz nowy robot HealthBot.</span><span class="sxs-lookup"><span data-stu-id="857f5-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="857f5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="857f5-107">EXAMPLES</span></span>

### <span data-ttu-id="857f5-108">Przykład 1. Tworzenie nowego robota HealthBot</span><span class="sxs-lookup"><span data-stu-id="857f5-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="857f5-109">Domyślne tworzenie nowego robota HealthBot</span><span class="sxs-lookup"><span data-stu-id="857f5-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="857f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="857f5-110">PARAMETERS</span></span>

### <span data-ttu-id="857f5-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="857f5-111">-AsJob</span></span>
<span data-ttu-id="857f5-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="857f5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="857f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857f5-113">-DefaultProfile</span></span>
<span data-ttu-id="857f5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="857f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857f5-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="857f5-115">-Location</span></span>
<span data-ttu-id="857f5-116">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="857f5-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="857f5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="857f5-117">-Name</span></span>
<span data-ttu-id="857f5-118">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="857f5-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857f5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="857f5-119">-NoWait</span></span>
<span data-ttu-id="857f5-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="857f5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="857f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="857f5-122">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="857f5-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="857f5-123">- SKU</span><span class="sxs-lookup"><span data-stu-id="857f5-123">-Sku</span></span>
<span data-ttu-id="857f5-124">Nazwa sku HealthBot</span><span class="sxs-lookup"><span data-stu-id="857f5-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857f5-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="857f5-125">-SubscriptionId</span></span>
<span data-ttu-id="857f5-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="857f5-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857f5-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="857f5-127">-Tag</span></span>
<span data-ttu-id="857f5-128">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="857f5-128">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857f5-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="857f5-129">-Confirm</span></span>
<span data-ttu-id="857f5-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="857f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857f5-131">-WhatIf</span></span>
<span data-ttu-id="857f5-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857f5-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="857f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857f5-134">CommonParameters</span></span>
<span data-ttu-id="857f5-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857f5-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857f5-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857f5-137">INPUTS</span></span>

## <span data-ttu-id="857f5-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="857f5-138">OUTPUTS</span></span>

### <span data-ttu-id="857f5-139">Microsoft.Azure.PowerShell.Cmdlet.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="857f5-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="857f5-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="857f5-140">NOTES</span></span>

<span data-ttu-id="857f5-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="857f5-141">ALIASES</span></span>

## <span data-ttu-id="857f5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="857f5-142">RELATED LINKS</span></span>

