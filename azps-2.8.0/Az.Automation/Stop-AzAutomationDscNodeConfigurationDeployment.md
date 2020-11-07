---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 698f0354b9f67896c14b8bb19d3716fa9e9167c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706684"
---
# <span data-ttu-id="97c1c-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="97c1c-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="97c1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="97c1c-103">Zatrzymuje wdrożenie konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="97c1c-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="97c1c-104">Zatrzymuje tylko bieżące zadanie wdrażania, ale nie przypisuje już przydzielonych konfiguracji węzłów.</span><span class="sxs-lookup"><span data-stu-id="97c1c-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="97c1c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97c1c-105">SYNTAX</span></span>

### <span data-ttu-id="97c1c-106">ByJobId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="97c1c-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c1c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="97c1c-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c1c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="97c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="97c1c-109">Polecenie cmdlet **stop-AzAutomationDscNodeConfigurationDeployment** zatrzymuje wdrażanie konfiguracji węzła konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="97c1c-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="97c1c-110">Powoduje zatrzymanie przydzielenia konfiguracji węzła do grup węzłów, które pozostały do przypisania, ale nie powoduje oddzielenia już przypisanych węzłów.</span><span class="sxs-lookup"><span data-stu-id="97c1c-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="97c1c-111">Aby wyrejestrować zaplanowane zadanie, należy użyć [Wyrejestrowanie — AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) z JobScheduleId w celu oddzielenia istniejącego zaplanowanego zadania.</span><span class="sxs-lookup"><span data-stu-id="97c1c-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="97c1c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97c1c-112">EXAMPLES</span></span>

### <span data-ttu-id="97c1c-113">Przykład 1: wdrażanie konfiguracji węzła usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="97c1c-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="97c1c-114">Powyższe polecenie zatrzymuje zadanie wdrożenia konfiguracji węzła DSC z przekazanym identyfikatorem jobId.</span><span class="sxs-lookup"><span data-stu-id="97c1c-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="97c1c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97c1c-115">PARAMETERS</span></span>

### <span data-ttu-id="97c1c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97c1c-116">-AutomationAccountName</span></span>
<span data-ttu-id="97c1c-117">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą to polecenie cmdlet kompiluje</span><span class="sxs-lookup"><span data-stu-id="97c1c-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="97c1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c1c-118">-DefaultProfile</span></span>
<span data-ttu-id="97c1c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="97c1c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97c1c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="97c1c-120">-Force</span></span>
<span data-ttu-id="97c1c-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="97c1c-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c1c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="97c1c-122">-InputObject</span></span>
<span data-ttu-id="97c1c-123">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="97c1c-123">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c1c-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="97c1c-124">-JobId</span></span>
<span data-ttu-id="97c1c-125">Określa identyfikator zadania istniejącego zadania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="97c1c-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c1c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97c1c-126">-PassThru</span></span>
<span data-ttu-id="97c1c-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="97c1c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97c1c-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="97c1c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97c1c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c1c-129">-ResourceGroupName</span></span>
<span data-ttu-id="97c1c-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="97c1c-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="97c1c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97c1c-131">-Confirm</span></span>
<span data-ttu-id="97c1c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c1c-133">-WhatIf</span></span>
<span data-ttu-id="97c1c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c1c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97c1c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97c1c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c1c-136">CommonParameters</span></span>
<span data-ttu-id="97c1c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c1c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c1c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c1c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97c1c-139">INPUTS</span></span>

### <span data-ttu-id="97c1c-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="97c1c-140">System.Guid</span></span>

### <span data-ttu-id="97c1c-141">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="97c1c-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="97c1c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="97c1c-142">System.String</span></span>

## <span data-ttu-id="97c1c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97c1c-143">OUTPUTS</span></span>

### <span data-ttu-id="97c1c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97c1c-144">System.Boolean</span></span>

## <span data-ttu-id="97c1c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97c1c-145">NOTES</span></span>

## <span data-ttu-id="97c1c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97c1c-146">RELATED LINKS</span></span>

[<span data-ttu-id="97c1c-147">Start — AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="97c1c-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="97c1c-148">Import — AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c1c-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="97c1c-149">Start — AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="97c1c-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="97c1c-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="97c1c-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="97c1c-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="97c1c-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)