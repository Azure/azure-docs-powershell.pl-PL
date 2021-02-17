---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239610"
---
# <span data-ttu-id="9a533-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9a533-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="9a533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a533-102">SYNOPSIS</span></span>
<span data-ttu-id="9a533-103">Usuwa konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9a533-103">Removes an Automation account.</span></span>

## <span data-ttu-id="9a533-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a533-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a533-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a533-105">DESCRIPTION</span></span>
<span data-ttu-id="9a533-106">Polecenie **cmdlet Remove-AzAutomationAccount** usuwa konto usługi Azure Automation z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a533-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="9a533-107">Aby uzyskać więcej informacji na temat kont automatyzacji, zobacz New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a533-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="9a533-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a533-108">EXAMPLES</span></span>

### <span data-ttu-id="9a533-109">Przykład 1. Usuwanie konta automatyzacji</span><span class="sxs-lookup"><span data-stu-id="9a533-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9a533-110">To polecenie usuwa konto automatyzacji o nazwie ContosoAutomationAccount bez monitowania o sprawdzanie poprawności użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9a533-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="9a533-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a533-111">PARAMETERS</span></span>

### <span data-ttu-id="9a533-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a533-112">-DefaultProfile</span></span>
<span data-ttu-id="9a533-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9a533-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a533-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9a533-114">-Force</span></span>
<span data-ttu-id="9a533-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="9a533-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a533-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9a533-116">-Name</span></span>
<span data-ttu-id="9a533-117">Określa nazwę konta automatyzacji, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a533-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a533-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a533-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a533-119">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9a533-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="9a533-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a533-120">-Confirm</span></span>
<span data-ttu-id="9a533-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a533-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a533-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a533-122">-WhatIf</span></span>
<span data-ttu-id="9a533-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a533-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a533-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a533-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a533-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a533-125">CommonParameters</span></span>
<span data-ttu-id="9a533-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a533-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a533-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a533-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a533-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a533-128">INPUTS</span></span>

### <span data-ttu-id="9a533-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9a533-129">System.String</span></span>

## <span data-ttu-id="9a533-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a533-130">OUTPUTS</span></span>

### <span data-ttu-id="9a533-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9a533-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="9a533-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a533-132">NOTES</span></span>

## <span data-ttu-id="9a533-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a533-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a533-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9a533-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="9a533-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9a533-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="9a533-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9a533-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


