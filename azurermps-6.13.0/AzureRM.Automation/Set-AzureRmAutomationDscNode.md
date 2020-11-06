---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: eaa1195e5cb853111b6e75efbff7e37bc8ff6881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524613"
---
# <span data-ttu-id="085a1-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="085a1-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="085a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="085a1-102">SYNOPSIS</span></span>
<span data-ttu-id="085a1-103">Modyfikuje konfigurację węzła, na którą jest zamapowany węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="085a1-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="085a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="085a1-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="085a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="085a1-105">DESCRIPTION</span></span>
<span data-ttu-id="085a1-106">Polecenie cmdlet **Set-AzureRmAutomationDscNode** powoduje zmodyfikowanie konfiguracji węzła APS (Konfiguracja stanu żądanego).</span><span class="sxs-lookup"><span data-stu-id="085a1-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="085a1-107">Usługa Azure Automation przechowuje konfigurację węzła DSC jako dokumentu konfiguracji Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="085a1-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="085a1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="085a1-108">EXAMPLES</span></span>

### <span data-ttu-id="085a1-109">Przykład 1: modyfikowanie mapowania konfiguracji węzła</span><span class="sxs-lookup"><span data-stu-id="085a1-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="085a1-110">To polecenie powoduje przypisanie konfiguracji węzła o nazwie contoso. NodeConfiguration01 do węzła o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="085a1-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="085a1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="085a1-111">PARAMETERS</span></span>

### <span data-ttu-id="085a1-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="085a1-112">-AutomationAccountName</span></span>
<span data-ttu-id="085a1-113">Określa nazwę konta automatyzacji zawierającego węzeł DSC, dla którego to polecenie cmdlet modyfikuje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="085a1-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="085a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085a1-114">-DefaultProfile</span></span>
<span data-ttu-id="085a1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="085a1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="085a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="085a1-116">-Force</span></span>
<span data-ttu-id="085a1-117">ps_force polecenie, które ma zostać uruchomione bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="085a1-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="085a1-118">-ID</span><span class="sxs-lookup"><span data-stu-id="085a1-118">-Id</span></span>
<span data-ttu-id="085a1-119">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet modyfikuje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="085a1-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="085a1-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="085a1-120">-NodeConfigurationName</span></span>
<span data-ttu-id="085a1-121">Określa nazwę konfiguracji węzła, w której ten aplet polecenia mapuje węzeł.</span><span class="sxs-lookup"><span data-stu-id="085a1-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="085a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="085a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="085a1-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet modyfikuje konfigurację węzła DSC.</span><span class="sxs-lookup"><span data-stu-id="085a1-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="085a1-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="085a1-124">-Confirm</span></span>
<span data-ttu-id="085a1-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="085a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="085a1-126">-WhatIf</span></span>
<span data-ttu-id="085a1-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="085a1-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="085a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="085a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085a1-129">CommonParameters</span></span>
<span data-ttu-id="085a1-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085a1-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="085a1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085a1-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="085a1-132">INPUTS</span></span>

### <span data-ttu-id="085a1-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="085a1-133">System.Guid</span></span>

### <span data-ttu-id="085a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="085a1-134">System.String</span></span>

## <span data-ttu-id="085a1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="085a1-135">OUTPUTS</span></span>

### <span data-ttu-id="085a1-136">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="085a1-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="085a1-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="085a1-137">NOTES</span></span>

## <span data-ttu-id="085a1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="085a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="085a1-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="085a1-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="085a1-140">Rejestr — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="085a1-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="085a1-141">Wyrejestrowanie — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="085a1-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


