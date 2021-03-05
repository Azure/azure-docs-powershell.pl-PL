---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: 46dee36dccc4a6e73620732df18059f64ccb6587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004746"
---
# <span data-ttu-id="3af9a-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3af9a-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="3af9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3af9a-103">Usuwa zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3af9a-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="3af9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3af9a-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af9a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3af9a-105">DESCRIPTION</span></span>
<span data-ttu-id="3af9a-106">Polecenie **cmdlet Remove-AzAutomationVariable** usuwa zmienną z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3af9a-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="3af9a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3af9a-107">EXAMPLES</span></span>

### <span data-ttu-id="3af9a-108">Przykład 1. Usuwanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="3af9a-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3af9a-109">To polecenie usuwa zmienną o nazwie StringVariable22 z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3af9a-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="3af9a-110">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="3af9a-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3af9a-111">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3af9a-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3af9a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3af9a-112">PARAMETERS</span></span>

### <span data-ttu-id="3af9a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3af9a-113">-AutomationAccountName</span></span>
<span data-ttu-id="3af9a-114">Określa nazwę konta automatyzacji zawierającego zmienną usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af9a-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3af9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af9a-115">-DefaultProfile</span></span>
<span data-ttu-id="3af9a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3af9a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3af9a-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3af9a-117">-Name</span></span>
<span data-ttu-id="3af9a-118">Określa nazwę zmiennej usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af9a-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3af9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3af9a-120">Określa grupę zasobów, dla której to polecenie cmdlet usuwa zmienną.</span><span class="sxs-lookup"><span data-stu-id="3af9a-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="3af9a-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3af9a-121">-Confirm</span></span>
<span data-ttu-id="3af9a-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3af9a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af9a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af9a-123">-WhatIf</span></span>
<span data-ttu-id="3af9a-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af9a-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3af9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af9a-126">CommonParameters</span></span>
<span data-ttu-id="3af9a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af9a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af9a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af9a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3af9a-129">INPUTS</span></span>

### <span data-ttu-id="3af9a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3af9a-130">System.String</span></span>

## <span data-ttu-id="3af9a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3af9a-131">OUTPUTS</span></span>

### <span data-ttu-id="3af9a-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="3af9a-132">System.Void</span></span>

## <span data-ttu-id="3af9a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3af9a-133">NOTES</span></span>

## <span data-ttu-id="3af9a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3af9a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3af9a-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3af9a-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="3af9a-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3af9a-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="3af9a-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3af9a-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


