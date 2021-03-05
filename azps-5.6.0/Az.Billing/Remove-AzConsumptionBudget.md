---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 58a4b7be314489a847479692a08f495fcf4c7146
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983425"
---
# <span data-ttu-id="47259-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="47259-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="47259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47259-102">SYNOPSIS</span></span>
<span data-ttu-id="47259-103">Usuwanie budżetu z subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47259-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="47259-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47259-104">SYNTAX</span></span>

### <span data-ttu-id="47259-105">Subskrypcja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="47259-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47259-106">Piping</span><span class="sxs-lookup"><span data-stu-id="47259-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47259-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="47259-107">DESCRIPTION</span></span>
<span data-ttu-id="47259-108">Polecenie Remove-AzConsumptionBudget usuwa budżet z subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47259-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="47259-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47259-109">EXAMPLES</span></span>

### <span data-ttu-id="47259-110">Przykład 1. Usuwanie budżetu z nazwą budżetu na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="47259-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="47259-111">Przykład 2. Usuwanie budżetu z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="47259-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="47259-112">Przykład 3. Usuwanie budżetu za pośrednictwem sieci rurowych na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="47259-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="47259-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47259-113">PARAMETERS</span></span>

### <span data-ttu-id="47259-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47259-114">-DefaultProfile</span></span>
<span data-ttu-id="47259-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47259-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47259-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47259-116">-InputObject</span></span>
<span data-ttu-id="47259-117">Obiekt Budżet.</span><span class="sxs-lookup"><span data-stu-id="47259-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47259-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47259-118">-Name</span></span>
<span data-ttu-id="47259-119">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="47259-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47259-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47259-120">-PassThru</span></span>
<span data-ttu-id="47259-121">Polecenie cmdlet zwraca wartość prawda, jeśli budżet został pomyślnie usunięty.</span><span class="sxs-lookup"><span data-stu-id="47259-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="47259-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47259-122">-ResourceGroupName</span></span>
<span data-ttu-id="47259-123">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="47259-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47259-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47259-124">-Confirm</span></span>
<span data-ttu-id="47259-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="47259-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47259-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47259-126">-WhatIf</span></span>
<span data-ttu-id="47259-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47259-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47259-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="47259-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47259-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47259-129">CommonParameters</span></span>
<span data-ttu-id="47259-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47259-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47259-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47259-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47259-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47259-132">INPUTS</span></span>

### <span data-ttu-id="47259-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="47259-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="47259-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47259-134">OUTPUTS</span></span>

### <span data-ttu-id="47259-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47259-135">System.Boolean</span></span>

## <span data-ttu-id="47259-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47259-136">NOTES</span></span>

## <span data-ttu-id="47259-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47259-137">RELATED LINKS</span></span>
