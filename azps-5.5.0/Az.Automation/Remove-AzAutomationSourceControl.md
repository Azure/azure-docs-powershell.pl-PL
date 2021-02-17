---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239507"
---
# <span data-ttu-id="85997-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="85997-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="85997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85997-102">SYNOPSIS</span></span>
<span data-ttu-id="85997-103">Usuwa kontrolkę źródła azure automation.</span><span class="sxs-lookup"><span data-stu-id="85997-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="85997-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85997-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85997-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="85997-105">DESCRIPTION</span></span>
<span data-ttu-id="85997-106">Polecenie Remove-AzAutomationSourceControl cmdlet usuwa kontrolkę źródłową z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="85997-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="85997-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85997-107">EXAMPLES</span></span>

### <span data-ttu-id="85997-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85997-108">Example 1</span></span>
<span data-ttu-id="85997-109">To polecenie usuwa kontrolkę źródła automatyzacji o nazwie VSTSNative z konta o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="85997-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="85997-110">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="85997-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="85997-111">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="85997-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="85997-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85997-112">PARAMETERS</span></span>

### <span data-ttu-id="85997-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="85997-113">-AutomationAccountName</span></span>
<span data-ttu-id="85997-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="85997-114">The automation account name.</span></span>

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

### <span data-ttu-id="85997-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85997-115">-DefaultProfile</span></span>
<span data-ttu-id="85997-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85997-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85997-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="85997-117">-Name</span></span>
<span data-ttu-id="85997-118">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="85997-118">The source control name.</span></span>

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

### <span data-ttu-id="85997-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85997-119">-PassThru</span></span>
<span data-ttu-id="85997-120">Funkcja PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="85997-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="85997-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="85997-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85997-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85997-122">-ResourceGroupName</span></span>
<span data-ttu-id="85997-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85997-123">The resource group name.</span></span>

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

### <span data-ttu-id="85997-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85997-124">-Confirm</span></span>
<span data-ttu-id="85997-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="85997-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85997-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85997-126">-WhatIf</span></span>
<span data-ttu-id="85997-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85997-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85997-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="85997-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85997-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85997-129">CommonParameters</span></span>
<span data-ttu-id="85997-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85997-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85997-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85997-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85997-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85997-132">INPUTS</span></span>

### <span data-ttu-id="85997-133">System.String</span><span class="sxs-lookup"><span data-stu-id="85997-133">System.String</span></span>

## <span data-ttu-id="85997-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85997-134">OUTPUTS</span></span>

### <span data-ttu-id="85997-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="85997-135">System.Void</span></span>

### <span data-ttu-id="85997-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85997-136">System.Boolean</span></span>

## <span data-ttu-id="85997-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85997-137">NOTES</span></span>

## <span data-ttu-id="85997-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85997-138">RELATED LINKS</span></span>
