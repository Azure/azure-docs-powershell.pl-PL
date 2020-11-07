---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 17106fed79fdec90bad6615560553dcdb5d46703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718056"
---
# <span data-ttu-id="e72ff-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e72ff-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="e72ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e72ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e72ff-103">Zatrzymuje wdrożenie konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e72ff-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="e72ff-104">Zatrzymuje tylko bieżące zadanie wdrażania, ale nie przypisuje już przydzielonych konfiguracji węzłów.</span><span class="sxs-lookup"><span data-stu-id="e72ff-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e72ff-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e72ff-105">SYNTAX</span></span>

### <span data-ttu-id="e72ff-106">ByJobId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e72ff-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72ff-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e72ff-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e72ff-108">DESCRIPTION</span></span>
<span data-ttu-id="e72ff-109">Polecenie cmdlet **stop-AzureRmAutomationDscNodeConfigurationDeployment** zatrzymuje wdrażanie konfiguracji węzła konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e72ff-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="e72ff-110">Powoduje zatrzymanie przydzielenia konfiguracji węzła do grup węzłów, które pozostały do przypisania, ale nie powoduje oddzielenia już przypisanych węzłów.</span><span class="sxs-lookup"><span data-stu-id="e72ff-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="e72ff-111">Aby wyrejestrować zaplanowane zadanie, należy użyć [Wyrejestrowanie — AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) z JobScheduleId w celu oddzielenia istniejącego zaplanowanego zadania.</span><span class="sxs-lookup"><span data-stu-id="e72ff-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="e72ff-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e72ff-112">EXAMPLES</span></span>

### <span data-ttu-id="e72ff-113">Przykład 1: wdrażanie konfiguracji węzła usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="e72ff-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e72ff-114">Powyższe polecenie zatrzymuje zadanie wdrożenia konfiguracji węzła DSC z przekazanym identyfikatorem jobId.</span><span class="sxs-lookup"><span data-stu-id="e72ff-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="e72ff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e72ff-115">PARAMETERS</span></span>

### <span data-ttu-id="e72ff-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e72ff-116">-AutomationAccountName</span></span>
<span data-ttu-id="e72ff-117">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą to polecenie cmdlet kompiluje</span><span class="sxs-lookup"><span data-stu-id="e72ff-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72ff-118">-DefaultProfile</span></span>
<span data-ttu-id="e72ff-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e72ff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e72ff-120">-Force</span></span>
<span data-ttu-id="e72ff-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="e72ff-121">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e72ff-122">-InputObject</span></span>
<span data-ttu-id="e72ff-123">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="e72ff-123">Input object for Piping</span></span>

```yaml
Type: NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="e72ff-124">-JobId</span></span>
<span data-ttu-id="e72ff-125">Określa identyfikator zadania istniejącego zadania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e72ff-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e72ff-126">-PassThru</span></span>
<span data-ttu-id="e72ff-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e72ff-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e72ff-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e72ff-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="e72ff-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="e72ff-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e72ff-131">-Confirm</span></span>
<span data-ttu-id="e72ff-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72ff-133">-WhatIf</span></span>
<span data-ttu-id="e72ff-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72ff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e72ff-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e72ff-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72ff-136">CommonParameters</span></span>
<span data-ttu-id="e72ff-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72ff-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72ff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72ff-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e72ff-139">INPUTS</span></span>

### <span data-ttu-id="e72ff-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e72ff-140">None</span></span>
<span data-ttu-id="e72ff-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e72ff-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e72ff-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e72ff-142">OUTPUTS</span></span>

## <span data-ttu-id="e72ff-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e72ff-143">NOTES</span></span>

## <span data-ttu-id="e72ff-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e72ff-144">RELATED LINKS</span></span>

[<span data-ttu-id="e72ff-145">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e72ff-145">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="e72ff-146">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e72ff-146">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="e72ff-147">Start — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e72ff-147">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e72ff-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e72ff-148">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e72ff-149">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="e72ff-149">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
