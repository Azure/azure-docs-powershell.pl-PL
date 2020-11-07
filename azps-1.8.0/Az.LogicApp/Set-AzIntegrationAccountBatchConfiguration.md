---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 40cd652a957d4e0a7565b573b288b333e4cebe33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867615"
---
# <span data-ttu-id="262a0-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="262a0-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="262a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="262a0-102">SYNOPSIS</span></span>
<span data-ttu-id="262a0-103">Modyfikuje konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="262a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="262a0-104">SYNTAX</span></span>

### <span data-ttu-id="262a0-105">ByIntegrationAccountAndParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="262a0-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="262a0-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="262a0-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="262a0-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="262a0-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="262a0-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="262a0-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="262a0-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262a0-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="262a0-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262a0-114">Opis</span><span class="sxs-lookup"><span data-stu-id="262a0-114">DESCRIPTION</span></span>
<span data-ttu-id="262a0-115">Polecenie cmdlet **Set-AzIntegrationAccountBatchConfiguration** modyfikuje konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="262a0-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="262a0-116">EXAMPLES</span></span>

### <span data-ttu-id="262a0-117">Przykład 1. modyfikowanie konfiguracji partii przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="262a0-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="262a0-118">Modyfikowanie konfiguracji wsadowej o nazwie "sampleBatchConfig" przy użyciu pliku lokalnego znajdującego się w ścieżce pliku znajdującej się w "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="262a0-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="262a0-119">Przykład 2: modyfikowanie konfiguracji partii przy użyciu ciągu JSON</span><span class="sxs-lookup"><span data-stu-id="262a0-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="262a0-120">Modyfikowanie konfiguracji wsadowej o nazwie "sampleBatchConfig" przy użyciu ciągu JSON zawartego w "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="262a0-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="262a0-121">Przykład 3: modyfikowanie konfiguracji partii przy użyciu parametrów</span><span class="sxs-lookup"><span data-stu-id="262a0-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="262a0-122">W celu zmodyfikowania konfiguracji wsadowej o nazwie "sampleBatchConfig" należy ręcznie podać wszystkie parametry nessecary.</span><span class="sxs-lookup"><span data-stu-id="262a0-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the nessecary parameters.</span></span>

## <span data-ttu-id="262a0-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="262a0-123">PARAMETERS</span></span>

### <span data-ttu-id="262a0-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="262a0-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="262a0-125">Definicja konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="262a0-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="262a0-127">Ścieżka pliku konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="262a0-128">-BatchGroupName</span></span>
<span data-ttu-id="262a0-129">Nazwa grupy konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="262a0-130">-BatchSize</span></span>
<span data-ttu-id="262a0-131">Rozmiar wsadu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262a0-132">-DefaultProfile</span></span>
<span data-ttu-id="262a0-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="262a0-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="262a0-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="262a0-134">-InputObject</span></span>
<span data-ttu-id="262a0-135">Konfiguracja partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="262a0-136">-MessageCount</span></span>
<span data-ttu-id="262a0-137">Licznik komunikatów konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="262a0-138">-Metadata</span></span>
<span data-ttu-id="262a0-139">Metadane konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="262a0-140">-Name</span></span>
<span data-ttu-id="262a0-141">Nazwa konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-142">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="262a0-142">-ParentName</span></span>
<span data-ttu-id="262a0-143">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262a0-144">-ResourceGroupName</span></span>
<span data-ttu-id="262a0-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="262a0-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="262a0-146">-ResourceId</span></span>
<span data-ttu-id="262a0-147">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="262a0-148">-ScheduleFrequency</span></span>
<span data-ttu-id="262a0-149">Częstotliwość harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="262a0-150">-ScheduleInterval</span></span>
<span data-ttu-id="262a0-151">Interwał harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="262a0-152">-ScheduleStartTime</span></span>
<span data-ttu-id="262a0-153">Harmonogram konfiguracji wsadowej konta integracji — czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="262a0-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="262a0-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="262a0-155">Strefa czasowa harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="262a0-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262a0-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="262a0-156">-Confirm</span></span>
<span data-ttu-id="262a0-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="262a0-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262a0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262a0-158">-WhatIf</span></span>
<span data-ttu-id="262a0-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="262a0-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="262a0-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="262a0-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262a0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262a0-161">CommonParameters</span></span>
<span data-ttu-id="262a0-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262a0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262a0-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262a0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262a0-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="262a0-164">INPUTS</span></span>

### <span data-ttu-id="262a0-165">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="262a0-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="262a0-166">System. String</span><span class="sxs-lookup"><span data-stu-id="262a0-166">System.String</span></span>

## <span data-ttu-id="262a0-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="262a0-167">OUTPUTS</span></span>

### <span data-ttu-id="262a0-168">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="262a0-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="262a0-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="262a0-169">NOTES</span></span>

## <span data-ttu-id="262a0-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="262a0-170">RELATED LINKS</span></span>
