---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199786"
---
# <span data-ttu-id="2be8e-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="2be8e-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="2be8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be8e-102">SYNOPSIS</span></span>
<span data-ttu-id="2be8e-103">Usuwa regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="2be8e-103">Deletes a action rule</span></span>

## <span data-ttu-id="2be8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2be8e-104">SYNTAX</span></span>

### <span data-ttu-id="2be8e-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="2be8e-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2be8e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2be8e-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2be8e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2be8e-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2be8e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2be8e-108">DESCRIPTION</span></span>
<span data-ttu-id="2be8e-109">Polecenie cmdlet **Remove-AzActionRule** usuwa regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="2be8e-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="2be8e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2be8e-110">EXAMPLES</span></span>

### <span data-ttu-id="2be8e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2be8e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="2be8e-112">To polecenie cmdlet usuwa regułę akcji o nazwie Nazwa_akcji w teście-rg grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2be8e-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="2be8e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2be8e-113">PARAMETERS</span></span>

### <span data-ttu-id="2be8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be8e-114">-DefaultProfile</span></span>
<span data-ttu-id="2be8e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2be8e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be8e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2be8e-116">-InputObject</span></span>
<span data-ttu-id="2be8e-117">Zasób reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2be8e-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2be8e-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2be8e-118">-Name</span></span>
<span data-ttu-id="2be8e-119">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="2be8e-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2be8e-120">-PassThru</span></span>
<span data-ttu-id="2be8e-121">Funkcja PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2be8e-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2be8e-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2be8e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2be8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2be8e-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2be8e-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2be8e-125">-ResourceId</span></span>
<span data-ttu-id="2be8e-126">Pobierz regułę akcji według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="2be8e-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be8e-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2be8e-127">-Confirm</span></span>
<span data-ttu-id="2be8e-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2be8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be8e-129">-WhatIf</span></span>
<span data-ttu-id="2be8e-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be8e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be8e-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2be8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be8e-132">CommonParameters</span></span>
<span data-ttu-id="2be8e-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be8e-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2be8e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be8e-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2be8e-135">INPUTS</span></span>

### <span data-ttu-id="2be8e-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2be8e-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2be8e-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2be8e-137">OUTPUTS</span></span>

### <span data-ttu-id="2be8e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2be8e-138">System.Boolean</span></span>

## <span data-ttu-id="2be8e-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2be8e-139">NOTES</span></span>

## <span data-ttu-id="2be8e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2be8e-140">RELATED LINKS</span></span>
