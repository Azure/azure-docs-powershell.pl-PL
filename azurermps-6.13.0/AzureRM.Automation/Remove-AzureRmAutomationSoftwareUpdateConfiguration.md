---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541984"
---
# <span data-ttu-id="0169e-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0169e-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="0169e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0169e-102">SYNOPSIS</span></span>
<span data-ttu-id="0169e-103">Usuwa konfigurację aktualizacji oprogramowania Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0169e-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0169e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0169e-104">SYNTAX</span></span>

### <span data-ttu-id="0169e-105">BySucName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0169e-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0169e-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="0169e-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0169e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0169e-107">DESCRIPTION</span></span>
<span data-ttu-id="0169e-108">To polecenie cmdlet usunęło konfigurację aktualizacji oprogramowania Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0169e-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="0169e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0169e-109">EXAMPLES</span></span>

### <span data-ttu-id="0169e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0169e-110">Example 1</span></span>
<span data-ttu-id="0169e-111">W tym przykładzie pokazano, jak usunąć MyUpdateConfiguration ' z konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="0169e-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="0169e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0169e-112">PARAMETERS</span></span>

### <span data-ttu-id="0169e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0169e-113">-AutomationAccountName</span></span>
<span data-ttu-id="0169e-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0169e-114">The automation account name.</span></span>

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

### <span data-ttu-id="0169e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0169e-115">-DefaultProfile</span></span>
<span data-ttu-id="0169e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0169e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0169e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0169e-117">-Name</span></span>
<span data-ttu-id="0169e-118">Nazwa konfiguracji aktualizacji oprogramowania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0169e-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0169e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0169e-119">-PassThru</span></span>
<span data-ttu-id="0169e-120">PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0169e-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0169e-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0169e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0169e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0169e-122">-ResourceGroupName</span></span>
<span data-ttu-id="0169e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0169e-123">The resource group name.</span></span>

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

### <span data-ttu-id="0169e-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0169e-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="0169e-125">Konfiguracja aktualizacji oprogramowania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0169e-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0169e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0169e-126">-Confirm</span></span>
<span data-ttu-id="0169e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0169e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0169e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0169e-128">-WhatIf</span></span>
<span data-ttu-id="0169e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0169e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0169e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0169e-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0169e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0169e-131">CommonParameters</span></span>
<span data-ttu-id="0169e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0169e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0169e-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0169e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0169e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0169e-134">INPUTS</span></span>

### <span data-ttu-id="0169e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0169e-135">System.String</span></span>

### <span data-ttu-id="0169e-136">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0169e-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="0169e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0169e-137">OUTPUTS</span></span>

### <span data-ttu-id="0169e-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="0169e-138">System.Object</span></span>
## <span data-ttu-id="0169e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0169e-139">NOTES</span></span>

## <span data-ttu-id="0169e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0169e-140">RELATED LINKS</span></span>
