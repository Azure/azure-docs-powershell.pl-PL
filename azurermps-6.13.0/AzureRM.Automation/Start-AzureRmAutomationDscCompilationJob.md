---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: ffa84b2c5ec4ccfdc48cae4e68cbe562034f7e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717947"
---
# <span data-ttu-id="71874-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="71874-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="71874-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71874-102">SYNOPSIS</span></span>
<span data-ttu-id="71874-103">Kompiluje konfigurację DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="71874-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71874-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71874-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71874-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71874-105">DESCRIPTION</span></span>
<span data-ttu-id="71874-106">Polecenie cmdlet **Start-AzureRmAutomationDscCompilationJob** kompiluje konfigurację wymaganej konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="71874-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="71874-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71874-107">EXAMPLES</span></span>

### <span data-ttu-id="71874-108">Przykład 1: kompilowanie konfiguracji usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="71874-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71874-109">Pierwsze polecenie tworzy słownik parametrów i zapisuje je w zmiennej $Params.</span><span class="sxs-lookup"><span data-stu-id="71874-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="71874-110">Drugie polecenie kompiluje konfigurację DSC o nazwie Config01.</span><span class="sxs-lookup"><span data-stu-id="71874-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="71874-111">Polecenie uwzględnia wartości w $Params dla parametrów konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="71874-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="71874-112">Przykład 2: kompilowanie konfiguracji usługi Azure DSC w automatyzacji przy użyciu nowej wersji kompilacji konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="71874-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="71874-113">Podobnie jak w pierwszym przykładzie pierwsze polecenie tworzy słownik parametrów i zapisuje je w zmiennej $Params.</span><span class="sxs-lookup"><span data-stu-id="71874-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="71874-114">Drugie polecenie kompiluje konfigurację DSC o nazwie Config01.</span><span class="sxs-lookup"><span data-stu-id="71874-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="71874-115">Polecenie uwzględnia wartości w $Params dla parametrów konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="71874-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="71874-116">Nie zastępuje wcześniejszej istniejącej konfiguracji węzła, tworząc nową konfigurację węzła o nazwie Config01 [<2>]. <NodeName> ..</span><span class="sxs-lookup"><span data-stu-id="71874-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="71874-117">Numer wersji jest zwiększany na podstawie istniejącego już numeru wersji.</span><span class="sxs-lookup"><span data-stu-id="71874-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="71874-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71874-118">PARAMETERS</span></span>

### <span data-ttu-id="71874-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71874-119">-AutomationAccountName</span></span>
<span data-ttu-id="71874-120">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71874-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="71874-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="71874-121">-ConfigurationData</span></span>
<span data-ttu-id="71874-122">Określa słownik danych konfiguracji konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="71874-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

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

### <span data-ttu-id="71874-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="71874-123">-ConfigurationName</span></span>
<span data-ttu-id="71874-124">Określa nazwę konfiguracji DSC kompilowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71874-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="71874-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71874-125">-DefaultProfile</span></span>
<span data-ttu-id="71874-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="71874-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71874-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="71874-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="71874-128">Tworzy nową wersję kompilacji konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="71874-128">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="71874-129">— Parametry</span><span class="sxs-lookup"><span data-stu-id="71874-129">-Parameters</span></span>
<span data-ttu-id="71874-130">Określa słownik parametrów, których używa polecenie cmdlet do kompilowania konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="71874-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

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

### <span data-ttu-id="71874-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71874-131">-ResourceGroupName</span></span>
<span data-ttu-id="71874-132">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="71874-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="71874-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71874-133">-Confirm</span></span>
<span data-ttu-id="71874-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71874-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71874-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71874-135">-WhatIf</span></span>
<span data-ttu-id="71874-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71874-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71874-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71874-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71874-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71874-138">CommonParameters</span></span>
<span data-ttu-id="71874-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71874-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71874-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71874-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71874-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71874-141">INPUTS</span></span>

### <span data-ttu-id="71874-142">System. String</span><span class="sxs-lookup"><span data-stu-id="71874-142">System.String</span></span>

## <span data-ttu-id="71874-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71874-143">OUTPUTS</span></span>

### <span data-ttu-id="71874-144">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="71874-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="71874-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71874-145">NOTES</span></span>

## <span data-ttu-id="71874-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71874-146">RELATED LINKS</span></span>

[<span data-ttu-id="71874-147">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="71874-147">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="71874-148">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="71874-148">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


