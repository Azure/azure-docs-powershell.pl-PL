---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 466cb31bd5e05235085fbc4f9045cf201a806e11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526325"
---
# <span data-ttu-id="93a8b-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="93a8b-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="93a8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="93a8b-103">Zatrzymuje wdrożenie konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="93a8b-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="93a8b-104">Zatrzymuje tylko bieżące zadanie wdrażania, ale nie przypisuje już przydzielonych konfiguracji węzłów.</span><span class="sxs-lookup"><span data-stu-id="93a8b-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93a8b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93a8b-105">SYNTAX</span></span>

### <span data-ttu-id="93a8b-106">ByJobId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="93a8b-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93a8b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="93a8b-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93a8b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="93a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="93a8b-109">Polecenie cmdlet **stop-AzureRmAutomationDscNodeConfigurationDeployment** zatrzymuje wdrażanie konfiguracji węzła konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="93a8b-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="93a8b-110">Powoduje zatrzymanie przydzielenia konfiguracji węzła do grup węzłów, które pozostały do przypisania, ale nie powoduje oddzielenia już przypisanych węzłów.</span><span class="sxs-lookup"><span data-stu-id="93a8b-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="93a8b-111">Aby wyrejestrować zaplanowane zadanie, należy użyć [Wyrejestrowanie — AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) z JobScheduleId w celu oddzielenia istniejącego zaplanowanego zadania.</span><span class="sxs-lookup"><span data-stu-id="93a8b-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="93a8b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93a8b-112">EXAMPLES</span></span>

### <span data-ttu-id="93a8b-113">Przykład 1: wdrażanie konfiguracji węzła usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="93a8b-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="93a8b-114">Powyższe polecenie zatrzymuje zadanie wdrożenia konfiguracji węzła DSC z przekazanym identyfikatorem jobId.</span><span class="sxs-lookup"><span data-stu-id="93a8b-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="93a8b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93a8b-115">PARAMETERS</span></span>

### <span data-ttu-id="93a8b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93a8b-116">-AutomationAccountName</span></span>
<span data-ttu-id="93a8b-117">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą to polecenie cmdlet kompiluje</span><span class="sxs-lookup"><span data-stu-id="93a8b-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="93a8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a8b-118">-DefaultProfile</span></span>
<span data-ttu-id="93a8b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="93a8b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93a8b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="93a8b-120">-Force</span></span>
<span data-ttu-id="93a8b-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="93a8b-121">ps_force</span></span>

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

### <span data-ttu-id="93a8b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="93a8b-122">-InputObject</span></span>
<span data-ttu-id="93a8b-123">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="93a8b-123">Input object for Piping</span></span>

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

### <span data-ttu-id="93a8b-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="93a8b-124">-JobId</span></span>
<span data-ttu-id="93a8b-125">Określa identyfikator zadania istniejącego zadania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="93a8b-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="93a8b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93a8b-126">-PassThru</span></span>
<span data-ttu-id="93a8b-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="93a8b-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93a8b-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="93a8b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93a8b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a8b-129">-ResourceGroupName</span></span>
<span data-ttu-id="93a8b-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="93a8b-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="93a8b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93a8b-131">-Confirm</span></span>
<span data-ttu-id="93a8b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93a8b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93a8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a8b-133">-WhatIf</span></span>
<span data-ttu-id="93a8b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93a8b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a8b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93a8b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93a8b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a8b-136">CommonParameters</span></span>
<span data-ttu-id="93a8b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a8b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a8b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a8b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a8b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93a8b-139">INPUTS</span></span>

### <span data-ttu-id="93a8b-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="93a8b-140">System.Guid</span></span>

### <span data-ttu-id="93a8b-141">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="93a8b-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>
<span data-ttu-id="93a8b-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="93a8b-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="93a8b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="93a8b-143">System.String</span></span>

## <span data-ttu-id="93a8b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93a8b-144">OUTPUTS</span></span>

### <span data-ttu-id="93a8b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93a8b-145">System.Boolean</span></span>

## <span data-ttu-id="93a8b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93a8b-146">NOTES</span></span>

## <span data-ttu-id="93a8b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93a8b-147">RELATED LINKS</span></span>

[<span data-ttu-id="93a8b-148">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="93a8b-148">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="93a8b-149">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a8b-149">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="93a8b-150">Start — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="93a8b-150">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="93a8b-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="93a8b-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="93a8b-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="93a8b-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
