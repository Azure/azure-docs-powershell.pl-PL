---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009857"
---
# <span data-ttu-id="0bacd-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="0bacd-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="0bacd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bacd-102">SYNOPSIS</span></span>
<span data-ttu-id="0bacd-103">Usuwa kontrolkę źródła azure automation.</span><span class="sxs-lookup"><span data-stu-id="0bacd-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="0bacd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0bacd-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bacd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0bacd-105">DESCRIPTION</span></span>
<span data-ttu-id="0bacd-106">Polecenie Remove-AzAutomationSourceControl cmdlet usuwa kontrolkę źródłową z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0bacd-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="0bacd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0bacd-107">EXAMPLES</span></span>

### <span data-ttu-id="0bacd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0bacd-108">Example 1</span></span>
<span data-ttu-id="0bacd-109">To polecenie usuwa kontrolkę źródła automatyzacji o nazwie VSTSNative z konta o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="0bacd-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="0bacd-110">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="0bacd-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="0bacd-111">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0bacd-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="0bacd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bacd-112">PARAMETERS</span></span>

### <span data-ttu-id="0bacd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0bacd-113">-AutomationAccountName</span></span>
<span data-ttu-id="0bacd-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0bacd-114">The automation account name.</span></span>

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

### <span data-ttu-id="0bacd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bacd-115">-DefaultProfile</span></span>
<span data-ttu-id="0bacd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bacd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bacd-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0bacd-117">-Name</span></span>
<span data-ttu-id="0bacd-118">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="0bacd-118">The source control name.</span></span>

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

### <span data-ttu-id="0bacd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bacd-119">-PassThru</span></span>
<span data-ttu-id="0bacd-120">Funkcja PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0bacd-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0bacd-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0bacd-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bacd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bacd-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bacd-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bacd-123">The resource group name.</span></span>

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

### <span data-ttu-id="0bacd-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bacd-124">-Confirm</span></span>
<span data-ttu-id="0bacd-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0bacd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bacd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bacd-126">-WhatIf</span></span>
<span data-ttu-id="0bacd-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bacd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bacd-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0bacd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bacd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bacd-129">CommonParameters</span></span>
<span data-ttu-id="0bacd-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bacd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bacd-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bacd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bacd-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bacd-132">INPUTS</span></span>

### <span data-ttu-id="0bacd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0bacd-133">System.String</span></span>

## <span data-ttu-id="0bacd-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bacd-134">OUTPUTS</span></span>

### <span data-ttu-id="0bacd-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="0bacd-135">System.Void</span></span>

### <span data-ttu-id="0bacd-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0bacd-136">System.Boolean</span></span>

## <span data-ttu-id="0bacd-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0bacd-137">NOTES</span></span>

## <span data-ttu-id="0bacd-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bacd-138">RELATED LINKS</span></span>
