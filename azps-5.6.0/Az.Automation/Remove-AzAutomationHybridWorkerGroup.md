---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 35ef4a5629726b33a8d9099da78134e6a0bac8b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009937"
---
# <span data-ttu-id="5421c-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="5421c-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="5421c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5421c-102">SYNOPSIS</span></span>
<span data-ttu-id="5421c-103">Usuwa grupę pracowników hybrydowych z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5421c-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="5421c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5421c-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5421c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5421c-105">DESCRIPTION</span></span>
<span data-ttu-id="5421c-106">Polecenie Remove-AzAutomationHybridWorkerGroup cmdlet usuwa grupę pracowników hybrydowych z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5421c-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="5421c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5421c-107">EXAMPLES</span></span>

### <span data-ttu-id="5421c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5421c-108">Example 1</span></span>
<span data-ttu-id="5421c-109">To polecenie usuwa pracownika hybrydowego według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="5421c-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="5421c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5421c-110">PARAMETERS</span></span>

### <span data-ttu-id="5421c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5421c-111">-AutomationAccountName</span></span>
<span data-ttu-id="5421c-112">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5421c-112">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5421c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5421c-113">-DefaultProfile</span></span>
<span data-ttu-id="5421c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5421c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5421c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5421c-115">-Name</span></span>
<span data-ttu-id="5421c-116">Nazwa hybrydowej grupy pracowników.</span><span class="sxs-lookup"><span data-stu-id="5421c-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5421c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5421c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5421c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5421c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5421c-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5421c-119">-Confirm</span></span>
<span data-ttu-id="5421c-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5421c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5421c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5421c-121">-WhatIf</span></span>
<span data-ttu-id="5421c-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5421c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5421c-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5421c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5421c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5421c-124">CommonParameters</span></span>
<span data-ttu-id="5421c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5421c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5421c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5421c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5421c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5421c-127">INPUTS</span></span>

### <span data-ttu-id="5421c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5421c-128">System.String</span></span>

## <span data-ttu-id="5421c-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5421c-129">OUTPUTS</span></span>

### <span data-ttu-id="5421c-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5421c-130">System.Void</span></span>

## <span data-ttu-id="5421c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5421c-131">NOTES</span></span>

## <span data-ttu-id="5421c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5421c-132">RELATED LINKS</span></span>
