---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551323"
---
# <span data-ttu-id="7b3a3-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="7b3a3-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="7b3a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3a3-103">Usuwanie budżetu z subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b3a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b3a3-104">SYNTAX</span></span>

### <span data-ttu-id="7b3a3-105">Abonament (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7b3a3-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b3a3-106">Instalacja</span><span class="sxs-lookup"><span data-stu-id="7b3a3-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b3a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7b3a3-107">DESCRIPTION</span></span>
<span data-ttu-id="7b3a3-108">Polecenie cmdlet Remove-AzureRmConsumptionBudget powoduje usunięcie budżetu z subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="7b3a3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b3a3-109">EXAMPLES</span></span>

### <span data-ttu-id="7b3a3-110">Przykład 1: Usuwanie budżetu z nazwą budżetu na poziomie abonamentu</span><span class="sxs-lookup"><span data-stu-id="7b3a3-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="7b3a3-111">Przykład 2: Usuwanie budżetu z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7b3a3-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="7b3a3-112">Przykład 3: Usuwanie budżetu za pomocą połączeń rurowych na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7b3a3-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="7b3a3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b3a3-113">PARAMETERS</span></span>

### <span data-ttu-id="7b3a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3a3-114">-DefaultProfile</span></span>
<span data-ttu-id="7b3a3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3a3-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b3a3-116">-InputObject</span></span>
<span data-ttu-id="7b3a3-117">Obiekt budżetu.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-117">Budget object.</span></span>

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

### <span data-ttu-id="7b3a3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b3a3-118">-Name</span></span>
<span data-ttu-id="7b3a3-119">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-119">Name of a budget.</span></span>

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

### <span data-ttu-id="7b3a3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b3a3-120">-PassThru</span></span>
<span data-ttu-id="7b3a3-121">Polecenie cmdlet zwraca wartość PRAWDA, Jeśli budżet został pomyślnie usunięty.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="7b3a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b3a3-123">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="7b3a3-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b3a3-124">-Confirm</span></span>
<span data-ttu-id="7b3a3-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b3a3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b3a3-126">-WhatIf</span></span>
<span data-ttu-id="7b3a3-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b3a3-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b3a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3a3-129">CommonParameters</span></span>
<span data-ttu-id="7b3a3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3a3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3a3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3a3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b3a3-132">INPUTS</span></span>

### <span data-ttu-id="7b3a3-133">Microsoft. Azure. Commands.. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="7b3a3-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="7b3a3-134">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b3a3-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7b3a3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b3a3-135">OUTPUTS</span></span>

### <span data-ttu-id="7b3a3-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b3a3-136">System.Boolean</span></span>

## <span data-ttu-id="7b3a3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b3a3-137">NOTES</span></span>

## <span data-ttu-id="7b3a3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b3a3-138">RELATED LINKS</span></span>
