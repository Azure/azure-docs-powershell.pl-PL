---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199595"
---
# <span data-ttu-id="2aab5-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2aab5-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="2aab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aab5-102">SYNOPSIS</span></span>
<span data-ttu-id="2aab5-103">Usuwa węzeł dsc z zarządzania za pomocą konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2aab5-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="2aab5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2aab5-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2aab5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2aab5-105">DESCRIPTION</span></span>
<span data-ttu-id="2aab5-106">Polecenie cmdlet **Unregister-AzAutomationDscNode** usuwa węzeł APS Desired State Configuration (DSC) z zarządzania za pomocą konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2aab5-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="2aab5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2aab5-107">EXAMPLES</span></span>

### <span data-ttu-id="2aab5-108">Przykład 1. Usuwanie węzła dsc platformy Azure z zarządzania za pomocą konta automatyzacji</span><span class="sxs-lookup"><span data-stu-id="2aab5-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="2aab5-109">To polecenie usuwa węzeł DSC, który ma określony identyfikator GUID, z zarządzania przez konto automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2aab5-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2aab5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aab5-110">PARAMETERS</span></span>

### <span data-ttu-id="2aab5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2aab5-111">-AutomationAccountName</span></span>
<span data-ttu-id="2aab5-112">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="2aab5-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="2aab5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aab5-113">-DefaultProfile</span></span>
<span data-ttu-id="2aab5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2aab5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aab5-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2aab5-115">-Force</span></span>
<span data-ttu-id="2aab5-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="2aab5-116">ps_force</span></span>

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

### <span data-ttu-id="2aab5-117">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="2aab5-117">-Id</span></span>
<span data-ttu-id="2aab5-118">Określa unikatowy identyfikator węzła DSC, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aab5-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aab5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aab5-119">-ResourceGroupName</span></span>
<span data-ttu-id="2aab5-120">Określa nazwę grupy zasobów, w której to polecenie cmdlet wyrejestruje węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="2aab5-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="2aab5-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2aab5-121">-Confirm</span></span>
<span data-ttu-id="2aab5-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2aab5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aab5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aab5-123">-WhatIf</span></span>
<span data-ttu-id="2aab5-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aab5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aab5-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2aab5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aab5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aab5-126">CommonParameters</span></span>
<span data-ttu-id="2aab5-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aab5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aab5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aab5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aab5-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aab5-129">INPUTS</span></span>

### <span data-ttu-id="2aab5-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="2aab5-130">System.Guid</span></span>

### <span data-ttu-id="2aab5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2aab5-131">System.String</span></span>

## <span data-ttu-id="2aab5-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2aab5-132">OUTPUTS</span></span>

### <span data-ttu-id="2aab5-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="2aab5-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="2aab5-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2aab5-134">NOTES</span></span>

## <span data-ttu-id="2aab5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aab5-135">RELATED LINKS</span></span>

[<span data-ttu-id="2aab5-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2aab5-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="2aab5-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2aab5-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="2aab5-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2aab5-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


