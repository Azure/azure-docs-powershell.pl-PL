---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: b9f23105b6fa84781ef1b0f0ba4be0e52e06ee08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706727"
---
# <span data-ttu-id="1c0f0-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1c0f0-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="1c0f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0f0-103">Usuwa grupę hybrydowych procesów roboczych z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="1c0f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c0f0-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c0f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c0f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1c0f0-106">Polecenie cmdlet Remove-AzAutomationHybridWorkerGroup usuwa grupę hybrydowego procesu roboczego z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="1c0f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c0f0-107">EXAMPLES</span></span>

### <span data-ttu-id="1c0f0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c0f0-108">Example 1</span></span>
<span data-ttu-id="1c0f0-109">To polecenie powoduje usunięcie hybrydowego procesu roboczego według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="1c0f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c0f0-110">PARAMETERS</span></span>

### <span data-ttu-id="1c0f0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1c0f0-111">-AutomationAccountName</span></span>
<span data-ttu-id="1c0f0-112">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-112">The automation account name.</span></span>

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

### <span data-ttu-id="1c0f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0f0-113">-DefaultProfile</span></span>
<span data-ttu-id="1c0f0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c0f0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c0f0-115">-Name</span></span>
<span data-ttu-id="1c0f0-116">Nazwa grupy hybrydowego procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="1c0f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c0f0-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-118">The resource group name.</span></span>

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

### <span data-ttu-id="1c0f0-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c0f0-119">-Confirm</span></span>
<span data-ttu-id="1c0f0-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0f0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0f0-121">-WhatIf</span></span>
<span data-ttu-id="1c0f0-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c0f0-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c0f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0f0-124">CommonParameters</span></span>
<span data-ttu-id="1c0f0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0f0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0f0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c0f0-127">INPUTS</span></span>

### <span data-ttu-id="1c0f0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1c0f0-128">System.String</span></span>

## <span data-ttu-id="1c0f0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c0f0-129">OUTPUTS</span></span>

### <span data-ttu-id="1c0f0-130">System. void</span><span class="sxs-lookup"><span data-stu-id="1c0f0-130">System.Void</span></span>

## <span data-ttu-id="1c0f0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c0f0-131">NOTES</span></span>

## <span data-ttu-id="1c0f0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c0f0-132">RELATED LINKS</span></span>
