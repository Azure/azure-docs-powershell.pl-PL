---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 7dfd7e0cfab041e43deae8321732b935adc5366a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004641"
---
# <span data-ttu-id="3cbb3-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="3cbb3-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="3cbb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cbb3-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbb3-103">Kompiluje konfigurację dsC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="3cbb3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3cbb3-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cbb3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3cbb3-105">DESCRIPTION</span></span>
<span data-ttu-id="3cbb3-106">Polecenie **cmdlet Start-AzAutomationDscCompilationJob** kompiluje konfigurację APS Desired State Configuration (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="3cbb3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3cbb3-107">EXAMPLES</span></span>

### <span data-ttu-id="3cbb3-108">Przykład 1. Skompilowanie konfiguracji usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="3cbb3-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3cbb3-109">Pierwsze polecenie tworzy słownik parametrów i zapisuje je w $Params zmienną.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="3cbb3-110">Drugie polecenie kompiluje konfigurację dsC o nazwie Config01.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="3cbb3-111">To polecenie uwzględnia wartości w parametrach $Params dsc.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="3cbb3-112">Przykład 2. Skompilowanie konfiguracji usługi Azure DSC w automatyzacji za pomocą nowej wersji kompilacji konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="3cbb3-113">Podobnie jak w pierwszym przykładzie pierwsze polecenie tworzy słownik parametrów i przechowuje je w $Params danych.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="3cbb3-114">Drugie polecenie kompiluje konfigurację dsC o nazwie Config01.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="3cbb3-115">To polecenie uwzględnia wartości w parametrach $Params dsc.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="3cbb3-116">Nie zastępuje ona istniejącej wcześniej konfiguracji węzła, tworząc nową konfigurację węzła o nazwie Config01[<2 <NodeName>>].</span><span class="sxs-lookup"><span data-stu-id="3cbb3-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="3cbb3-117">Numer wersji jest zwiększany na podstawie istniejącego numeru wersji, który już istnieje.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="3cbb3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cbb3-118">PARAMETERS</span></span>

### <span data-ttu-id="3cbb3-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3cbb3-119">-AutomationAccountName</span></span>
<span data-ttu-id="3cbb3-120">Określa nazwę konta automatyzacji zawierającego konfigurację DSC kompilacyjną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="3cbb3-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="3cbb3-121">-ConfigurationData</span></span>
<span data-ttu-id="3cbb3-122">Określa słownik danych konfiguracyjnych dla konfiguracji dsc.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb3-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3cbb3-123">-ConfigurationName</span></span>
<span data-ttu-id="3cbb3-124">Określa nazwę konfiguracji dsc, która kompiluje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbb3-125">-DefaultProfile</span></span>
<span data-ttu-id="3cbb3-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3cbb3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cbb3-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="3cbb3-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="3cbb3-128">Tworzy nową wersję kompilacji konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-128">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="3cbb3-129">— Parametry</span><span class="sxs-lookup"><span data-stu-id="3cbb3-129">-Parameters</span></span>
<span data-ttu-id="3cbb3-130">Określa słownik parametrów używany przez to polecenie cmdlet do kompilowania konfiguracji dsC.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbb3-131">-ResourceGroupName</span></span>
<span data-ttu-id="3cbb3-132">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="3cbb3-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cbb3-133">-Confirm</span></span>
<span data-ttu-id="3cbb3-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cbb3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cbb3-135">-WhatIf</span></span>
<span data-ttu-id="3cbb3-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cbb3-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cbb3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbb3-138">CommonParameters</span></span>
<span data-ttu-id="3cbb3-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cbb3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbb3-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cbb3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbb3-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cbb3-141">INPUTS</span></span>

### <span data-ttu-id="3cbb3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3cbb3-142">System.String</span></span>

## <span data-ttu-id="3cbb3-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cbb3-143">OUTPUTS</span></span>

### <span data-ttu-id="3cbb3-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="3cbb3-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="3cbb3-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3cbb3-145">NOTES</span></span>

## <span data-ttu-id="3cbb3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cbb3-146">RELATED LINKS</span></span>

[<span data-ttu-id="3cbb3-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="3cbb3-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="3cbb3-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="3cbb3-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


