---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 8e5b34d82639ac91afd07f4c2cdc8729e6d213b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008826"
---
# <span data-ttu-id="73258-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73258-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="73258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73258-102">SYNOPSIS</span></span>
<span data-ttu-id="73258-103">Tworzy konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="73258-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73258-104">SYNTAX</span></span>

### <span data-ttu-id="73258-105">ByIntegrationAccountAndParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="73258-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="73258-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="73258-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="73258-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="73258-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="73258-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="73258-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="73258-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73258-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="73258-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73258-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="73258-114">DESCRIPTION</span></span>
<span data-ttu-id="73258-115">Polecenie **cmdlet Get-AzIntegrationAccountBatchConfiguration** tworzy nową konfigurację partii na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="73258-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73258-116">EXAMPLES</span></span>

### <span data-ttu-id="73258-117">Przykład 1. Tworzenie nowej konfiguracji partii przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="73258-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="73258-118">Tworzy nową konfigurację partii przy użyciu pliku lokalnego znajdującego się w ścieżce pliku zawartej w pliku "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="73258-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="73258-119">Przykład 2. Tworzenie nowej konfiguracji partii przy użyciu ciągu JSON</span><span class="sxs-lookup"><span data-stu-id="73258-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="73258-120">Tworzy nową konfigurację partii przy użyciu ciągu JSON zawartego w ciągu "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="73258-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="73258-121">Przykład 3. Tworzenie nowej konfiguracji partii przy użyciu parametrów</span><span class="sxs-lookup"><span data-stu-id="73258-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="73258-122">Tworzy nową konfigurację partii, ręcznie podając wszystkie niezbędne parametry.</span><span class="sxs-lookup"><span data-stu-id="73258-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="73258-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73258-123">PARAMETERS</span></span>

### <span data-ttu-id="73258-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="73258-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="73258-125">Definicja partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="73258-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="73258-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="73258-127">Ścieżka pliku konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="73258-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="73258-128">-BatchGroupName</span></span>
<span data-ttu-id="73258-129">Nazwa grupy konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="73258-130">- BatchSize</span><span class="sxs-lookup"><span data-stu-id="73258-130">-BatchSize</span></span>
<span data-ttu-id="73258-131">Rozmiar partii partii konfiguracji konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="73258-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73258-132">-DefaultProfile</span></span>
<span data-ttu-id="73258-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73258-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73258-134">- MessageCount</span><span class="sxs-lookup"><span data-stu-id="73258-134">-MessageCount</span></span>
<span data-ttu-id="73258-135">Liczba komunikatów konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="73258-136">— Metadane</span><span class="sxs-lookup"><span data-stu-id="73258-136">-Metadata</span></span>
<span data-ttu-id="73258-137">Metadane konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="73258-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73258-138">-Name</span></span>
<span data-ttu-id="73258-139">Nazwa partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73258-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="73258-140">-ParentName</span></span>
<span data-ttu-id="73258-141">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-141">The integration account name.</span></span>

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

### <span data-ttu-id="73258-142">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="73258-142">-ParentObject</span></span>
<span data-ttu-id="73258-143">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73258-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73258-144">-ParentResourceId</span></span>
<span data-ttu-id="73258-145">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="73258-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73258-146">-ResourceGroupName</span></span>
<span data-ttu-id="73258-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73258-147">The resource group name.</span></span>

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

### <span data-ttu-id="73258-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="73258-148">-ScheduleFrequency</span></span>
<span data-ttu-id="73258-149">Częstotliwość harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="73258-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="73258-150">-ScheduleInterval</span></span>
<span data-ttu-id="73258-151">Interwał harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="73258-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="73258-152">-ScheduleStartTime</span></span>
<span data-ttu-id="73258-153">Godzina rozpoczęcia harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="73258-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="73258-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="73258-155">Strefa czasowa harmonogramu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="73258-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="73258-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73258-156">-Confirm</span></span>
<span data-ttu-id="73258-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73258-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73258-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73258-158">-WhatIf</span></span>
<span data-ttu-id="73258-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73258-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73258-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="73258-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73258-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73258-161">CommonParameters</span></span>
<span data-ttu-id="73258-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73258-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73258-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73258-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73258-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73258-164">INPUTS</span></span>

### <span data-ttu-id="73258-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="73258-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="73258-166">System.String</span><span class="sxs-lookup"><span data-stu-id="73258-166">System.String</span></span>

## <span data-ttu-id="73258-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73258-167">OUTPUTS</span></span>

### <span data-ttu-id="73258-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73258-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="73258-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73258-169">NOTES</span></span>

## <span data-ttu-id="73258-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73258-170">RELATED LINKS</span></span>
