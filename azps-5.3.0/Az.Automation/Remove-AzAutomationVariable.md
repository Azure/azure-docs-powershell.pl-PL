---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502268"
---
# <span data-ttu-id="f205d-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f205d-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="f205d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f205d-102">SYNOPSIS</span></span>
<span data-ttu-id="f205d-103">Usuwa zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f205d-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="f205d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f205d-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f205d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f205d-105">DESCRIPTION</span></span>
<span data-ttu-id="f205d-106">Polecenie cmdlet **Remove-AzAutomationVariable** usuwa zmienną z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f205d-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="f205d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f205d-107">EXAMPLES</span></span>

### <span data-ttu-id="f205d-108">Przykład 1. Usuń zmienną</span><span class="sxs-lookup"><span data-stu-id="f205d-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f205d-109">To polecenie usuwa zmienną o nazwie StringVariable22 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f205d-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f205d-110">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="f205d-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f205d-111">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f205d-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f205d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f205d-112">PARAMETERS</span></span>

### <span data-ttu-id="f205d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f205d-113">-AutomationAccountName</span></span>
<span data-ttu-id="f205d-114">Określa nazwę konta automatyzacji zawierającego zmienną, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="f205d-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f205d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f205d-115">-DefaultProfile</span></span>
<span data-ttu-id="f205d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f205d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f205d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f205d-117">-Name</span></span>
<span data-ttu-id="f205d-118">Określa nazwę zmiennej, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="f205d-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f205d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f205d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f205d-120">Określa grupę zasobów, dla której to polecenie cmdlet usuwa zmienną.</span><span class="sxs-lookup"><span data-stu-id="f205d-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="f205d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f205d-121">-Confirm</span></span>
<span data-ttu-id="f205d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f205d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f205d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f205d-123">-WhatIf</span></span>
<span data-ttu-id="f205d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f205d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f205d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f205d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f205d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f205d-126">CommonParameters</span></span>
<span data-ttu-id="f205d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f205d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f205d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f205d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f205d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f205d-129">INPUTS</span></span>

### <span data-ttu-id="f205d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f205d-130">System.String</span></span>

## <span data-ttu-id="f205d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f205d-131">OUTPUTS</span></span>

### <span data-ttu-id="f205d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="f205d-132">System.Void</span></span>

## <span data-ttu-id="f205d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f205d-133">NOTES</span></span>

## <span data-ttu-id="f205d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f205d-134">RELATED LINKS</span></span>

[<span data-ttu-id="f205d-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f205d-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="f205d-136">Nowe — AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f205d-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="f205d-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f205d-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


