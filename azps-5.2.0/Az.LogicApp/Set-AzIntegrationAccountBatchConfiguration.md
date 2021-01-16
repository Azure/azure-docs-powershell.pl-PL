---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358295"
---
# <span data-ttu-id="7b94e-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b94e-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7b94e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b94e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b94e-103">Modyfikuje konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="7b94e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b94e-104">SYNTAX</span></span>

### <span data-ttu-id="7b94e-105">ByIntegrationAccountAndParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b94e-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="7b94e-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="7b94e-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="7b94e-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="7b94e-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="7b94e-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="7b94e-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="7b94e-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b94e-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="7b94e-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b94e-114">Opis</span><span class="sxs-lookup"><span data-stu-id="7b94e-114">DESCRIPTION</span></span>
<span data-ttu-id="7b94e-115">Polecenie cmdlet **Set-AzIntegrationAccountBatchConfiguration** modyfikuje konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="7b94e-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b94e-116">EXAMPLES</span></span>

### <span data-ttu-id="7b94e-117">Przykład 1. modyfikowanie konfiguracji partii przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="7b94e-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7b94e-118">Modyfikowanie konfiguracji wsadowej o nazwie "sampleBatchConfig" przy użyciu pliku lokalnego znajdującego się w ścieżce pliku znajdującej się w "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="7b94e-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="7b94e-119">Przykład 2: modyfikowanie konfiguracji partii przy użyciu ciągu JSON</span><span class="sxs-lookup"><span data-stu-id="7b94e-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7b94e-120">Modyfikowanie konfiguracji wsadowej o nazwie "sampleBatchConfig" przy użyciu ciągu JSON zawartego w "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="7b94e-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="7b94e-121">Przykład 3: modyfikowanie konfiguracji partii przy użyciu parametrów</span><span class="sxs-lookup"><span data-stu-id="7b94e-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7b94e-122">Modyfikowanie konfiguracji wsadowej o nazwie "sampleBatchConfig" przez ręczne podanie wszystkich niezbędnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="7b94e-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="7b94e-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b94e-123">PARAMETERS</span></span>

### <span data-ttu-id="7b94e-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="7b94e-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="7b94e-125">Definicja konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="7b94e-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="7b94e-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="7b94e-127">Ścieżka pliku konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="7b94e-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="7b94e-128">-BatchGroupName</span></span>
<span data-ttu-id="7b94e-129">Nazwa grupy konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="7b94e-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="7b94e-130">-BatchSize</span></span>
<span data-ttu-id="7b94e-131">Rozmiar wsadu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="7b94e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b94e-132">-DefaultProfile</span></span>
<span data-ttu-id="7b94e-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b94e-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b94e-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b94e-134">-InputObject</span></span>
<span data-ttu-id="7b94e-135">Konfiguracja partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="7b94e-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="7b94e-136">-MessageCount</span></span>
<span data-ttu-id="7b94e-137">Licznik komunikatów konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="7b94e-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7b94e-138">-Metadata</span></span>
<span data-ttu-id="7b94e-139">Metadane konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="7b94e-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b94e-140">-Name</span></span>
<span data-ttu-id="7b94e-141">Nazwa konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="7b94e-142">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="7b94e-142">-ParentName</span></span>
<span data-ttu-id="7b94e-143">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-143">The integration account name.</span></span>

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

### <span data-ttu-id="7b94e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b94e-144">-ResourceGroupName</span></span>
<span data-ttu-id="7b94e-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b94e-145">The resource group name.</span></span>

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

### <span data-ttu-id="7b94e-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b94e-146">-ResourceId</span></span>
<span data-ttu-id="7b94e-147">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="7b94e-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="7b94e-148">-ScheduleFrequency</span></span>
<span data-ttu-id="7b94e-149">Częstotliwość harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="7b94e-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="7b94e-150">-ScheduleInterval</span></span>
<span data-ttu-id="7b94e-151">Interwał harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="7b94e-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="7b94e-152">-ScheduleStartTime</span></span>
<span data-ttu-id="7b94e-153">Harmonogram konfiguracji wsadowej konta integracji — czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="7b94e-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="7b94e-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="7b94e-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="7b94e-155">Strefa czasowa harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b94e-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="7b94e-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b94e-156">-Confirm</span></span>
<span data-ttu-id="7b94e-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b94e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b94e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b94e-158">-WhatIf</span></span>
<span data-ttu-id="7b94e-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b94e-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b94e-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b94e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b94e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b94e-161">CommonParameters</span></span>
<span data-ttu-id="7b94e-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b94e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b94e-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b94e-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b94e-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b94e-164">INPUTS</span></span>

### <span data-ttu-id="7b94e-165">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b94e-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="7b94e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="7b94e-166">System.String</span></span>

## <span data-ttu-id="7b94e-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b94e-167">OUTPUTS</span></span>

### <span data-ttu-id="7b94e-168">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b94e-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7b94e-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b94e-169">NOTES</span></span>

## <span data-ttu-id="7b94e-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b94e-170">RELATED LINKS</span></span>
