---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: b1495f4b7473225697567ca3e9d87e98107ce001
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972753"
---
# <span data-ttu-id="7141c-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7141c-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7141c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7141c-102">SYNOPSIS</span></span>
<span data-ttu-id="7141c-103">Modyfikuje konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="7141c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7141c-104">SYNTAX</span></span>

### <span data-ttu-id="7141c-105">ByIntegrationAccountAndParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7141c-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="7141c-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="7141c-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="7141c-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="7141c-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="7141c-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="7141c-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="7141c-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7141c-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="7141c-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7141c-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="7141c-114">DESCRIPTION</span></span>
<span data-ttu-id="7141c-115">Polecenie **cmdlet Set-AzIntegrationAccountBatchConfiguration** modyfikuje konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="7141c-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7141c-116">EXAMPLES</span></span>

### <span data-ttu-id="7141c-117">Przykład 1. Modyfikowanie konfiguracji partii przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="7141c-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7141c-118">Zmodyfikuj konfigurację partii o nazwie "sampleBatchConfig" przy użyciu pliku lokalnego znajdującego się w ścieżce pliku zawartej w pliku "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="7141c-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="7141c-119">Przykład 2. Modyfikowanie konfiguracji partii przy użyciu ciągu JSON</span><span class="sxs-lookup"><span data-stu-id="7141c-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7141c-120">Zmodyfikuj konfigurację partii o nazwie "sampleBatchConfig" przy użyciu ciągu JSON zawartego w ciągu "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="7141c-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="7141c-121">Przykład 3. Modyfikowanie konfiguracji partii przy użyciu parametrów</span><span class="sxs-lookup"><span data-stu-id="7141c-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7141c-122">Zmodyfikuj konfigurację partii o nazwie "sampleBatchConfig", ręcznie podając wszystkie niezbędne parametry.</span><span class="sxs-lookup"><span data-stu-id="7141c-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="7141c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7141c-123">PARAMETERS</span></span>

### <span data-ttu-id="7141c-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="7141c-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="7141c-125">Definicja partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="7141c-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="7141c-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="7141c-127">Ścieżka pliku konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="7141c-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="7141c-128">-BatchGroupName</span></span>
<span data-ttu-id="7141c-129">Nazwa grupy konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="7141c-130">- BatchSize</span><span class="sxs-lookup"><span data-stu-id="7141c-130">-BatchSize</span></span>
<span data-ttu-id="7141c-131">Rozmiar partii partii konfiguracji konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="7141c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7141c-132">-DefaultProfile</span></span>
<span data-ttu-id="7141c-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7141c-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7141c-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7141c-134">-InputObject</span></span>
<span data-ttu-id="7141c-135">Konfiguracja partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="7141c-136">- MessageCount</span><span class="sxs-lookup"><span data-stu-id="7141c-136">-MessageCount</span></span>
<span data-ttu-id="7141c-137">Liczba komunikatów konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="7141c-138">— Metadane</span><span class="sxs-lookup"><span data-stu-id="7141c-138">-Metadata</span></span>
<span data-ttu-id="7141c-139">Metadane konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="7141c-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7141c-140">-Name</span></span>
<span data-ttu-id="7141c-141">Nazwa partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="7141c-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="7141c-142">-ParentName</span></span>
<span data-ttu-id="7141c-143">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-143">The integration account name.</span></span>

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

### <span data-ttu-id="7141c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7141c-144">-ResourceGroupName</span></span>
<span data-ttu-id="7141c-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7141c-145">The resource group name.</span></span>

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

### <span data-ttu-id="7141c-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7141c-146">-ResourceId</span></span>
<span data-ttu-id="7141c-147">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="7141c-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="7141c-148">-ScheduleFrequency</span></span>
<span data-ttu-id="7141c-149">Częstotliwość harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="7141c-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="7141c-150">-ScheduleInterval</span></span>
<span data-ttu-id="7141c-151">Interwał harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="7141c-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="7141c-152">-ScheduleStartTime</span></span>
<span data-ttu-id="7141c-153">Godzina rozpoczęcia harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="7141c-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="7141c-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="7141c-155">Strefa czasowa harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7141c-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="7141c-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7141c-156">-Confirm</span></span>
<span data-ttu-id="7141c-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7141c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7141c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7141c-158">-WhatIf</span></span>
<span data-ttu-id="7141c-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7141c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7141c-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7141c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7141c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7141c-161">CommonParameters</span></span>
<span data-ttu-id="7141c-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7141c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7141c-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7141c-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7141c-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7141c-164">INPUTS</span></span>

### <span data-ttu-id="7141c-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7141c-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="7141c-166">System.String</span><span class="sxs-lookup"><span data-stu-id="7141c-166">System.String</span></span>

## <span data-ttu-id="7141c-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7141c-167">OUTPUTS</span></span>

### <span data-ttu-id="7141c-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7141c-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7141c-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7141c-169">NOTES</span></span>

## <span data-ttu-id="7141c-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7141c-170">RELATED LINKS</span></span>
