---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 3fb795f614e6ccd7c4e97470d89c6c8923fa9165
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009946"
---
# <span data-ttu-id="94782-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94782-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="94782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94782-102">SYNOPSIS</span></span>
<span data-ttu-id="94782-103">Usuwa poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="94782-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="94782-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94782-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94782-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="94782-105">DESCRIPTION</span></span>
<span data-ttu-id="94782-106">Polecenie **cmdlet Remove-AzAutomationCredential** usuwa poświadczenia z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94782-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="94782-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94782-107">EXAMPLES</span></span>

### <span data-ttu-id="94782-108">Przykład 1. Usuwanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="94782-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="94782-109">To polecenie usuwa poświadczenia o nazwie ContosoCredential z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="94782-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="94782-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94782-110">PARAMETERS</span></span>

### <span data-ttu-id="94782-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94782-111">-AutomationAccountName</span></span>
<span data-ttu-id="94782-112">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="94782-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="94782-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94782-113">-DefaultProfile</span></span>
<span data-ttu-id="94782-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="94782-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94782-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94782-115">-Name</span></span>
<span data-ttu-id="94782-116">Określa nazwę poświadczenia, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94782-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94782-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94782-117">-ResourceGroupName</span></span>
<span data-ttu-id="94782-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="94782-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="94782-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94782-119">-Confirm</span></span>
<span data-ttu-id="94782-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94782-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94782-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94782-121">-WhatIf</span></span>
<span data-ttu-id="94782-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94782-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94782-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94782-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94782-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94782-124">CommonParameters</span></span>
<span data-ttu-id="94782-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94782-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94782-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94782-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94782-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94782-127">INPUTS</span></span>

### <span data-ttu-id="94782-128">System.String</span><span class="sxs-lookup"><span data-stu-id="94782-128">System.String</span></span>

## <span data-ttu-id="94782-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94782-129">OUTPUTS</span></span>

### <span data-ttu-id="94782-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="94782-130">System.Void</span></span>

## <span data-ttu-id="94782-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94782-131">NOTES</span></span>

## <span data-ttu-id="94782-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94782-132">RELATED LINKS</span></span>

[<span data-ttu-id="94782-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94782-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="94782-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94782-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="94782-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94782-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


