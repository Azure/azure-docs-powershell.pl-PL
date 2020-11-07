---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: dbd70f70ec234b381f55995b9e4d31a52fe1d623
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551408"
---
# <span data-ttu-id="cd664-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd664-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="cd664-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd664-102">SYNOPSIS</span></span>
<span data-ttu-id="cd664-103">Umożliwia usunięcie węzła DSC z zarządzania przez konto automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cd664-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd664-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd664-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd664-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd664-105">DESCRIPTION</span></span>
<span data-ttu-id="cd664-106">Polecenie cmdlet **Unregister-AzureRmAutomationDscNode** umożliwia usunięcie węzła konfiguracji stanu żądanego (DSC) od zarządzania przez konto usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cd664-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="cd664-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd664-107">EXAMPLES</span></span>

### <span data-ttu-id="cd664-108">Przykład 1: Usuwanie węzła usługi Azure DSC z zarządzania przez konto usługi Automation</span><span class="sxs-lookup"><span data-stu-id="cd664-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="cd664-109">To polecenie umożliwia usunięcie węzła DSC o określonym identyfikatorze GUID z zarządzania przez konto usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cd664-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cd664-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd664-110">PARAMETERS</span></span>

### <span data-ttu-id="cd664-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd664-111">-AutomationAccountName</span></span>
<span data-ttu-id="cd664-112">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="cd664-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="cd664-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd664-113">-DefaultProfile</span></span>
<span data-ttu-id="cd664-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd664-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd664-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd664-115">-Force</span></span>
<span data-ttu-id="cd664-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="cd664-116">ps_force</span></span>

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

### <span data-ttu-id="cd664-117">-ID</span><span class="sxs-lookup"><span data-stu-id="cd664-117">-Id</span></span>
<span data-ttu-id="cd664-118">Określa unikatowy identyfikator węzła DSC, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd664-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd664-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd664-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd664-120">Określa nazwę grupy zasobów, w której ten polecenie cmdlet wyrejestrowuje węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="cd664-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="cd664-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd664-121">-Confirm</span></span>
<span data-ttu-id="cd664-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd664-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd664-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd664-123">-WhatIf</span></span>
<span data-ttu-id="cd664-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd664-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd664-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd664-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd664-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd664-126">CommonParameters</span></span>
<span data-ttu-id="cd664-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd664-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd664-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd664-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd664-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd664-129">INPUTS</span></span>

### <span data-ttu-id="cd664-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cd664-130">System.Guid</span></span>

### <span data-ttu-id="cd664-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cd664-131">System.String</span></span>

## <span data-ttu-id="cd664-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd664-132">OUTPUTS</span></span>

### <span data-ttu-id="cd664-133">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="cd664-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="cd664-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd664-134">NOTES</span></span>

## <span data-ttu-id="cd664-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd664-135">RELATED LINKS</span></span>

[<span data-ttu-id="cd664-136">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd664-136">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="cd664-137">Rejestr — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd664-137">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="cd664-138">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cd664-138">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

