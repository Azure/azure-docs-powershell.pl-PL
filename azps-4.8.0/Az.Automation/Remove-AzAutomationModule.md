---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064323"
---
# <span data-ttu-id="d094d-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d094d-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="d094d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d094d-102">SYNOPSIS</span></span>
<span data-ttu-id="d094d-103">Umożliwia usunięcie modułu z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d094d-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="d094d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d094d-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d094d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d094d-105">DESCRIPTION</span></span>
<span data-ttu-id="d094d-106">Polecenie cmdlet **Remove-AzAutomationModule** umożliwia usunięcie modułu z konta usługi Automation w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d094d-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="d094d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d094d-107">EXAMPLES</span></span>

### <span data-ttu-id="d094d-108">Przykład 1: usuwanie modułu</span><span class="sxs-lookup"><span data-stu-id="d094d-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d094d-109">To polecenie umożliwia usunięcie modułu o nazwie ContosoModule z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d094d-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d094d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d094d-110">PARAMETERS</span></span>

### <span data-ttu-id="d094d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d094d-111">-AutomationAccountName</span></span>
<span data-ttu-id="d094d-112">Określa nazwę konta automatyzacji, na podstawie którego ten aplet polecenia usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="d094d-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="d094d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d094d-113">-DefaultProfile</span></span>
<span data-ttu-id="d094d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d094d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d094d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d094d-115">-Force</span></span>
<span data-ttu-id="d094d-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d094d-116">ps_force</span></span>

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

### <span data-ttu-id="d094d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d094d-117">-Name</span></span>
<span data-ttu-id="d094d-118">Określa nazwę modułu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d094d-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d094d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d094d-119">-ResourceGroupName</span></span>
<span data-ttu-id="d094d-120">Określa nazwę grupy zasobów, w której ten aplet polecenia usunie moduł.</span><span class="sxs-lookup"><span data-stu-id="d094d-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="d094d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d094d-121">-Confirm</span></span>
<span data-ttu-id="d094d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d094d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d094d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d094d-123">-WhatIf</span></span>
<span data-ttu-id="d094d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d094d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d094d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d094d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d094d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d094d-126">CommonParameters</span></span>
<span data-ttu-id="d094d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d094d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d094d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d094d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d094d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d094d-129">INPUTS</span></span>

### <span data-ttu-id="d094d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d094d-130">System.String</span></span>

## <span data-ttu-id="d094d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d094d-131">OUTPUTS</span></span>

### <span data-ttu-id="d094d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="d094d-132">System.Void</span></span>

## <span data-ttu-id="d094d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d094d-133">NOTES</span></span>

## <span data-ttu-id="d094d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d094d-134">RELATED LINKS</span></span>

[<span data-ttu-id="d094d-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d094d-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="d094d-136">Nowe — AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d094d-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="d094d-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d094d-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


