---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 264ec3d845c5604237ca5975584866e5201f35d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867692"
---
# <span data-ttu-id="9a17f-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a17f-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9a17f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a17f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a17f-103">Umożliwia utworzenie konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="9a17f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a17f-104">SYNTAX</span></span>

### <span data-ttu-id="9a17f-105">ByIntegrationAccountAndParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9a17f-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="9a17f-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="9a17f-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="9a17f-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="9a17f-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="9a17f-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="9a17f-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="9a17f-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a17f-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="9a17f-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a17f-114">Opis</span><span class="sxs-lookup"><span data-stu-id="9a17f-114">DESCRIPTION</span></span>
<span data-ttu-id="9a17f-115">Polecenie cmdlet **Get-AzIntegrationAccountBatchConfiguration** tworzy nową konfigurację partii na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="9a17f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a17f-116">EXAMPLES</span></span>

### <span data-ttu-id="9a17f-117">Przykład 1: Tworzenie nowej konfiguracji wsadowej przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="9a17f-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="9a17f-118">Tworzy nową konfigurację partii przy użyciu pliku lokalnego znajdującego się w ścieżce pliku znajdującej się w "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="9a17f-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="9a17f-119">Przykład 2: Tworzenie nowej konfiguracji wsadowej przy użyciu ciągu JSON</span><span class="sxs-lookup"><span data-stu-id="9a17f-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="9a17f-120">Tworzy nową konfigurację partii przy użyciu ciągu JSON zawartego w "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="9a17f-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="9a17f-121">Przykład 3: Tworzenie nowej konfiguracji wsadowej przy użyciu parametrów</span><span class="sxs-lookup"><span data-stu-id="9a17f-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="9a17f-122">Tworzy nową konfigurację partii, ręcznie dostarczając wszystkie parametry nessecary.</span><span class="sxs-lookup"><span data-stu-id="9a17f-122">Creates a new batch configuration by manually providing all of the nessecary parameters.</span></span>

## <span data-ttu-id="9a17f-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a17f-123">PARAMETERS</span></span>

### <span data-ttu-id="9a17f-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="9a17f-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="9a17f-125">Definicja konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="9a17f-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="9a17f-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="9a17f-127">Ścieżka pliku konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="9a17f-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="9a17f-128">-BatchGroupName</span></span>
<span data-ttu-id="9a17f-129">Nazwa grupy konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="9a17f-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="9a17f-130">-BatchSize</span></span>
<span data-ttu-id="9a17f-131">Rozmiar wsadu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="9a17f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a17f-132">-DefaultProfile</span></span>
<span data-ttu-id="9a17f-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a17f-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a17f-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="9a17f-134">-MessageCount</span></span>
<span data-ttu-id="9a17f-135">Licznik komunikatów konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="9a17f-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9a17f-136">-Metadata</span></span>
<span data-ttu-id="9a17f-137">Metadane konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="9a17f-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a17f-138">-Name</span></span>
<span data-ttu-id="9a17f-139">Nazwa konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="9a17f-140">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="9a17f-140">-ParentName</span></span>
<span data-ttu-id="9a17f-141">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-141">The integration account name.</span></span>

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

### <span data-ttu-id="9a17f-142">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="9a17f-142">-ParentObject</span></span>
<span data-ttu-id="9a17f-143">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-143">An integration account object.</span></span>

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

### <span data-ttu-id="9a17f-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9a17f-144">-ParentResourceId</span></span>
<span data-ttu-id="9a17f-145">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="9a17f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a17f-146">-ResourceGroupName</span></span>
<span data-ttu-id="9a17f-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a17f-147">The resource group name.</span></span>

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

### <span data-ttu-id="9a17f-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="9a17f-148">-ScheduleFrequency</span></span>
<span data-ttu-id="9a17f-149">Częstotliwość harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="9a17f-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="9a17f-150">-ScheduleInterval</span></span>
<span data-ttu-id="9a17f-151">Interwał harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="9a17f-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="9a17f-152">-ScheduleStartTime</span></span>
<span data-ttu-id="9a17f-153">Harmonogram konfiguracji wsadowej konta integracji — czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="9a17f-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="9a17f-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="9a17f-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="9a17f-155">Strefa czasowa harmonogramu konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9a17f-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="9a17f-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a17f-156">-Confirm</span></span>
<span data-ttu-id="9a17f-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a17f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a17f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a17f-158">-WhatIf</span></span>
<span data-ttu-id="9a17f-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a17f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a17f-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a17f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a17f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a17f-161">CommonParameters</span></span>
<span data-ttu-id="9a17f-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a17f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a17f-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a17f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a17f-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a17f-164">INPUTS</span></span>

### <span data-ttu-id="9a17f-165">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9a17f-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="9a17f-166">System. String</span><span class="sxs-lookup"><span data-stu-id="9a17f-166">System.String</span></span>

## <span data-ttu-id="9a17f-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a17f-167">OUTPUTS</span></span>

### <span data-ttu-id="9a17f-168">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a17f-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9a17f-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a17f-169">NOTES</span></span>

## <span data-ttu-id="9a17f-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a17f-170">RELATED LINKS</span></span>
