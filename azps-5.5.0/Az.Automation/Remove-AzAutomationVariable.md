---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199618"
---
# <span data-ttu-id="db527-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="db527-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="db527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db527-102">SYNOPSIS</span></span>
<span data-ttu-id="db527-103">Usuwa zmienną automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="db527-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="db527-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="db527-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db527-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="db527-105">DESCRIPTION</span></span>
<span data-ttu-id="db527-106">Polecenie **cmdlet Remove-AzAutomationVariable** usuwa zmienną z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db527-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="db527-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="db527-107">EXAMPLES</span></span>

### <span data-ttu-id="db527-108">Przykład 1. Usuwanie zmiennej</span><span class="sxs-lookup"><span data-stu-id="db527-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="db527-109">To polecenie usuwa zmienną o nazwie StringVariable22 z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="db527-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="db527-110">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="db527-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="db527-111">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="db527-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="db527-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db527-112">PARAMETERS</span></span>

### <span data-ttu-id="db527-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db527-113">-AutomationAccountName</span></span>
<span data-ttu-id="db527-114">Określa nazwę konta automatyzacji zawierającego zmienną usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db527-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="db527-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db527-115">-DefaultProfile</span></span>
<span data-ttu-id="db527-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="db527-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db527-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="db527-117">-Name</span></span>
<span data-ttu-id="db527-118">Określa nazwę zmiennej usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db527-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="db527-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db527-119">-ResourceGroupName</span></span>
<span data-ttu-id="db527-120">Określa grupę zasobów, dla której to polecenie cmdlet usuwa zmienną.</span><span class="sxs-lookup"><span data-stu-id="db527-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="db527-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db527-121">-Confirm</span></span>
<span data-ttu-id="db527-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="db527-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db527-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db527-123">-WhatIf</span></span>
<span data-ttu-id="db527-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db527-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db527-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="db527-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db527-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db527-126">CommonParameters</span></span>
<span data-ttu-id="db527-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db527-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db527-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db527-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db527-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db527-129">INPUTS</span></span>

### <span data-ttu-id="db527-130">System.String</span><span class="sxs-lookup"><span data-stu-id="db527-130">System.String</span></span>

## <span data-ttu-id="db527-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db527-131">OUTPUTS</span></span>

### <span data-ttu-id="db527-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="db527-132">System.Void</span></span>

## <span data-ttu-id="db527-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="db527-133">NOTES</span></span>

## <span data-ttu-id="db527-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db527-134">RELATED LINKS</span></span>

[<span data-ttu-id="db527-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="db527-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="db527-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="db527-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="db527-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="db527-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


