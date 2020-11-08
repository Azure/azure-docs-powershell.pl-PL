---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053890"
---
# <span data-ttu-id="7ac8e-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7ac8e-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="7ac8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ac8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac8e-103">Umożliwia usunięcie modułu z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="7ac8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ac8e-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ac8e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ac8e-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac8e-106">Polecenie cmdlet **Remove-AzAutomationModule** umożliwia usunięcie modułu z konta usługi Automation w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="7ac8e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ac8e-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac8e-108">Przykład 1: usuwanie modułu</span><span class="sxs-lookup"><span data-stu-id="7ac8e-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ac8e-109">To polecenie umożliwia usunięcie modułu o nazwie ContosoModule z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7ac8e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ac8e-110">PARAMETERS</span></span>

### <span data-ttu-id="7ac8e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ac8e-111">-AutomationAccountName</span></span>
<span data-ttu-id="7ac8e-112">Określa nazwę konta automatyzacji, na podstawie którego ten aplet polecenia usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="7ac8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac8e-113">-DefaultProfile</span></span>
<span data-ttu-id="7ac8e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7ac8e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ac8e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7ac8e-115">-Force</span></span>
<span data-ttu-id="7ac8e-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7ac8e-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac8e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ac8e-117">-Name</span></span>
<span data-ttu-id="7ac8e-118">Określa nazwę modułu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7ac8e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac8e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ac8e-120">Określa nazwę grupy zasobów, w której ten aplet polecenia usunie moduł.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="7ac8e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ac8e-121">-Confirm</span></span>
<span data-ttu-id="7ac8e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac8e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac8e-123">-WhatIf</span></span>
<span data-ttu-id="7ac8e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac8e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac8e-126">CommonParameters</span></span>
<span data-ttu-id="7ac8e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac8e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac8e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac8e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac8e-129">INPUTS</span></span>

### <span data-ttu-id="7ac8e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ac8e-130">System.String</span></span>

## <span data-ttu-id="7ac8e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ac8e-131">OUTPUTS</span></span>

### <span data-ttu-id="7ac8e-132">System. void</span><span class="sxs-lookup"><span data-stu-id="7ac8e-132">System.Void</span></span>

## <span data-ttu-id="7ac8e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ac8e-133">NOTES</span></span>

## <span data-ttu-id="7ac8e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac8e-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ac8e-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7ac8e-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="7ac8e-136">Nowe — AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7ac8e-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="7ac8e-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7ac8e-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


