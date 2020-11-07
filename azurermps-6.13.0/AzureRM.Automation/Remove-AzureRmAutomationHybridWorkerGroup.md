---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716794"
---
# <span data-ttu-id="cd422-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cd422-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="cd422-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd422-102">SYNOPSIS</span></span>
<span data-ttu-id="cd422-103">Usuwa grupę hybrydowych procesów roboczych z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cd422-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd422-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd422-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd422-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd422-105">DESCRIPTION</span></span>
<span data-ttu-id="cd422-106">Polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup usuwa grupę hybrydowego procesu roboczego z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cd422-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="cd422-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd422-107">EXAMPLES</span></span>

### <span data-ttu-id="cd422-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd422-108">Example 1</span></span>
<span data-ttu-id="cd422-109">To polecenie powoduje usunięcie hybrydowego procesu roboczego według nazwy.</span><span class="sxs-lookup"><span data-stu-id="cd422-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="cd422-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd422-110">PARAMETERS</span></span>

### <span data-ttu-id="cd422-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd422-111">-AutomationAccountName</span></span>
<span data-ttu-id="cd422-112">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cd422-112">The automation account name.</span></span>

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

### <span data-ttu-id="cd422-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd422-113">-DefaultProfile</span></span>
<span data-ttu-id="cd422-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd422-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd422-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd422-115">-Name</span></span>
<span data-ttu-id="cd422-116">Nazwa grupy hybrydowego procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="cd422-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="cd422-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd422-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd422-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd422-118">The resource group name.</span></span>

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

### <span data-ttu-id="cd422-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd422-119">-Confirm</span></span>
<span data-ttu-id="cd422-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd422-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd422-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd422-121">-WhatIf</span></span>
<span data-ttu-id="cd422-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd422-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd422-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd422-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd422-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd422-124">CommonParameters</span></span>
<span data-ttu-id="cd422-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd422-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd422-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd422-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd422-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd422-127">INPUTS</span></span>

### <span data-ttu-id="cd422-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cd422-128">System.String</span></span>

## <span data-ttu-id="cd422-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd422-129">OUTPUTS</span></span>

### <span data-ttu-id="cd422-130">System. void</span><span class="sxs-lookup"><span data-stu-id="cd422-130">System.Void</span></span>

## <span data-ttu-id="cd422-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd422-131">NOTES</span></span>

## <span data-ttu-id="cd422-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd422-132">RELATED LINKS</span></span>
