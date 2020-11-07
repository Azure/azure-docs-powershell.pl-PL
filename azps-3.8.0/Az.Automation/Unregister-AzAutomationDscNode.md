---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895477"
---
# <span data-ttu-id="e27d9-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e27d9-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="e27d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e27d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e27d9-103">Umożliwia usunięcie węzła DSC z zarządzania przez konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e27d9-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="e27d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e27d9-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e27d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e27d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e27d9-106">Polecenie cmdlet **Unregister-AzAutomationDscNode** umożliwia usunięcie węzła konfiguracji stanu żądanego (DSC) od zarządzania przez konto usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e27d9-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="e27d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e27d9-107">EXAMPLES</span></span>

### <span data-ttu-id="e27d9-108">Przykład 1: Usuwanie węzła usługi Azure DSC z zarządzania przez konto usługi Automation</span><span class="sxs-lookup"><span data-stu-id="e27d9-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="e27d9-109">To polecenie umożliwia usunięcie węzła DSC o określonym identyfikatorze GUID z zarządzania przez konto usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e27d9-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e27d9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e27d9-110">PARAMETERS</span></span>

### <span data-ttu-id="e27d9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e27d9-111">-AutomationAccountName</span></span>
<span data-ttu-id="e27d9-112">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="e27d9-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="e27d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27d9-113">-DefaultProfile</span></span>
<span data-ttu-id="e27d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e27d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e27d9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e27d9-115">-Force</span></span>
<span data-ttu-id="e27d9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e27d9-116">ps_force</span></span>

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

### <span data-ttu-id="e27d9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e27d9-117">-Id</span></span>
<span data-ttu-id="e27d9-118">Określa unikatowy identyfikator węzła DSC, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e27d9-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e27d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="e27d9-120">Określa nazwę grupy zasobów, w której ten polecenie cmdlet wyrejestrowuje węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="e27d9-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="e27d9-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e27d9-121">-Confirm</span></span>
<span data-ttu-id="e27d9-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e27d9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e27d9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e27d9-123">-WhatIf</span></span>
<span data-ttu-id="e27d9-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e27d9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e27d9-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e27d9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e27d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27d9-126">CommonParameters</span></span>
<span data-ttu-id="e27d9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e27d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27d9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e27d9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27d9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e27d9-129">INPUTS</span></span>

### <span data-ttu-id="e27d9-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e27d9-130">System.Guid</span></span>

### <span data-ttu-id="e27d9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e27d9-131">System.String</span></span>

## <span data-ttu-id="e27d9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e27d9-132">OUTPUTS</span></span>

### <span data-ttu-id="e27d9-133">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="e27d9-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="e27d9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e27d9-134">NOTES</span></span>

## <span data-ttu-id="e27d9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e27d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="e27d9-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e27d9-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="e27d9-137">Rejestr — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e27d9-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="e27d9-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e27d9-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


