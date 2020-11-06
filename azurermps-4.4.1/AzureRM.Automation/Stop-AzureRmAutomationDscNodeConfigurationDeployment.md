---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552427"
---
# <span data-ttu-id="f69bc-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f69bc-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="f69bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f69bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f69bc-103">Zatrzymuje wdrożenie konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f69bc-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="f69bc-104">Zatrzymuje tylko bieżące zadanie wdrażania, ale nie przypisuje już przydzielonych konfiguracji węzłów.</span><span class="sxs-lookup"><span data-stu-id="f69bc-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f69bc-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f69bc-105">SYNTAX</span></span>

### <span data-ttu-id="f69bc-106">ByJobId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f69bc-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f69bc-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="f69bc-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f69bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f69bc-108">DESCRIPTION</span></span>
<span data-ttu-id="f69bc-109">Polecenie cmdlet **stop-AzureRmAutomationDscNodeConfigurationDeployment** zatrzymuje wdrażanie konfiguracji węzła konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f69bc-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="f69bc-110">Powoduje zatrzymanie przydzielenia konfiguracji węzła do grup węzłów, które pozostały do przypisania, ale nie powoduje oddzielenia już przypisanych węzłów.</span><span class="sxs-lookup"><span data-stu-id="f69bc-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="f69bc-111">Aby wyrejestrować zaplanowane zadanie, należy użyć [Wyrejestrowanie — AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) z JobScheduleId w celu oddzielenia istniejącego zaplanowanego zadania.</span><span class="sxs-lookup"><span data-stu-id="f69bc-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="f69bc-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f69bc-112">EXAMPLES</span></span>

### <span data-ttu-id="f69bc-113">Przykład 1: wdrażanie konfiguracji węzła usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="f69bc-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="f69bc-114">Powyższe polecenie zatrzymuje zadanie wdrożenia konfiguracji węzła DSC z przekazanym identyfikatorem jobId.</span><span class="sxs-lookup"><span data-stu-id="f69bc-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="f69bc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f69bc-115">PARAMETERS</span></span>

### <span data-ttu-id="f69bc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f69bc-116">-AutomationAccountName</span></span>
<span data-ttu-id="f69bc-117">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f69bc-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="f69bc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69bc-118">-ResourceGroupName</span></span>
<span data-ttu-id="f69bc-119">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="f69bc-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f69bc-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="f69bc-120">-JobId</span></span>
<span data-ttu-id="f69bc-121">Określa identyfikator zadania istniejącego zadania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f69bc-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="f69bc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f69bc-122">-PassThru</span></span>
<span data-ttu-id="f69bc-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f69bc-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f69bc-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f69bc-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f69bc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f69bc-125">-Force</span></span>
<span data-ttu-id="f69bc-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="f69bc-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f69bc-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f69bc-127">-Confirm</span></span>
<span data-ttu-id="f69bc-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f69bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f69bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69bc-129">-WhatIf</span></span>
<span data-ttu-id="f69bc-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f69bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f69bc-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f69bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f69bc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69bc-132">-DefaultProfile</span></span>
<span data-ttu-id="f69bc-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f69bc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f69bc-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f69bc-134">-InputObject</span></span>
<span data-ttu-id="f69bc-135">Obiekt wejściowy dla połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="f69bc-135">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f69bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69bc-136">CommonParameters</span></span>
<span data-ttu-id="f69bc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69bc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69bc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69bc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f69bc-139">INPUTS</span></span>

## <span data-ttu-id="f69bc-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f69bc-140">OUTPUTS</span></span>

## <span data-ttu-id="f69bc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f69bc-141">NOTES</span></span>

## <span data-ttu-id="f69bc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f69bc-142">RELATED LINKS</span></span>

[<span data-ttu-id="f69bc-143">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f69bc-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="f69bc-144">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69bc-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f69bc-145">Start — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f69bc-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f69bc-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f69bc-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f69bc-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="f69bc-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
