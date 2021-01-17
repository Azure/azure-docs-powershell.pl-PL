---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371156"
---
# <span data-ttu-id="54cb9-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="54cb9-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="54cb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="54cb9-103">Usuwanie budżetu z subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54cb9-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="54cb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54cb9-104">SYNTAX</span></span>

### <span data-ttu-id="54cb9-105">Abonament (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="54cb9-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54cb9-106">Instalacja</span><span class="sxs-lookup"><span data-stu-id="54cb9-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54cb9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="54cb9-107">DESCRIPTION</span></span>
<span data-ttu-id="54cb9-108">Polecenie cmdlet Remove-AzConsumptionBudget powoduje usunięcie budżetu z subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54cb9-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="54cb9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="54cb9-110">Przykład 1: Usuwanie budżetu z nazwą budżetu na poziomie abonamentu</span><span class="sxs-lookup"><span data-stu-id="54cb9-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="54cb9-111">Przykład 2: Usuwanie budżetu z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="54cb9-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="54cb9-112">Przykład 3: Usuwanie budżetu za pomocą połączeń rurowych na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="54cb9-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="54cb9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54cb9-113">PARAMETERS</span></span>

### <span data-ttu-id="54cb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cb9-114">-DefaultProfile</span></span>
<span data-ttu-id="54cb9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54cb9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54cb9-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54cb9-116">-InputObject</span></span>
<span data-ttu-id="54cb9-117">Obiekt budżetu.</span><span class="sxs-lookup"><span data-stu-id="54cb9-117">Budget object.</span></span>

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

### <span data-ttu-id="54cb9-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54cb9-118">-Name</span></span>
<span data-ttu-id="54cb9-119">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="54cb9-119">Name of a budget.</span></span>

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

### <span data-ttu-id="54cb9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54cb9-120">-PassThru</span></span>
<span data-ttu-id="54cb9-121">Polecenie cmdlet zwraca wartość PRAWDA, Jeśli budżet został pomyślnie usunięty.</span><span class="sxs-lookup"><span data-stu-id="54cb9-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="54cb9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cb9-122">-ResourceGroupName</span></span>
<span data-ttu-id="54cb9-123">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="54cb9-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="54cb9-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54cb9-124">-Confirm</span></span>
<span data-ttu-id="54cb9-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54cb9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54cb9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54cb9-126">-WhatIf</span></span>
<span data-ttu-id="54cb9-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54cb9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54cb9-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="54cb9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54cb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cb9-129">CommonParameters</span></span>
<span data-ttu-id="54cb9-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54cb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cb9-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54cb9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cb9-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54cb9-132">INPUTS</span></span>

### <span data-ttu-id="54cb9-133">Microsoft. Azure. Commands.. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="54cb9-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="54cb9-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54cb9-134">OUTPUTS</span></span>

### <span data-ttu-id="54cb9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54cb9-135">System.Boolean</span></span>

## <span data-ttu-id="54cb9-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54cb9-136">NOTES</span></span>

## <span data-ttu-id="54cb9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54cb9-137">RELATED LINKS</span></span>
