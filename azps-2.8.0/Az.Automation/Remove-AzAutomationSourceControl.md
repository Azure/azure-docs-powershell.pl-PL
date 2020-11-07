---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706723"
---
# <span data-ttu-id="5510c-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="5510c-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="5510c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5510c-102">SYNOPSIS</span></span>
<span data-ttu-id="5510c-103">Usuwa kontrolę źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5510c-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="5510c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5510c-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5510c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5510c-105">DESCRIPTION</span></span>
<span data-ttu-id="5510c-106">Polecenie cmdlet Remove-AzAutomationSourceControl usuwa kontrolę źródła z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5510c-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="5510c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5510c-107">EXAMPLES</span></span>

### <span data-ttu-id="5510c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5510c-108">Example 1</span></span>
<span data-ttu-id="5510c-109">To polecenie usuwa kontrolkę źródła automatyzacji o nazwie VSTSNative na koncie o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="5510c-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="5510c-110">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="5510c-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="5510c-111">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5510c-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="5510c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5510c-112">PARAMETERS</span></span>

### <span data-ttu-id="5510c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5510c-113">-AutomationAccountName</span></span>
<span data-ttu-id="5510c-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5510c-114">The automation account name.</span></span>

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

### <span data-ttu-id="5510c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5510c-115">-DefaultProfile</span></span>
<span data-ttu-id="5510c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5510c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5510c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5510c-117">-Name</span></span>
<span data-ttu-id="5510c-118">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="5510c-118">The source control name.</span></span>

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

### <span data-ttu-id="5510c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5510c-119">-PassThru</span></span>
<span data-ttu-id="5510c-120">PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5510c-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5510c-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5510c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5510c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5510c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5510c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5510c-123">The resource group name.</span></span>

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

### <span data-ttu-id="5510c-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5510c-124">-Confirm</span></span>
<span data-ttu-id="5510c-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5510c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5510c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5510c-126">-WhatIf</span></span>
<span data-ttu-id="5510c-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5510c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5510c-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5510c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5510c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5510c-129">CommonParameters</span></span>
<span data-ttu-id="5510c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5510c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5510c-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5510c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5510c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5510c-132">INPUTS</span></span>

### <span data-ttu-id="5510c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5510c-133">System.String</span></span>

## <span data-ttu-id="5510c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5510c-134">OUTPUTS</span></span>

### <span data-ttu-id="5510c-135">System. void</span><span class="sxs-lookup"><span data-stu-id="5510c-135">System.Void</span></span>

### <span data-ttu-id="5510c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5510c-136">System.Boolean</span></span>

## <span data-ttu-id="5510c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5510c-137">NOTES</span></span>

## <span data-ttu-id="5510c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5510c-138">RELATED LINKS</span></span>
