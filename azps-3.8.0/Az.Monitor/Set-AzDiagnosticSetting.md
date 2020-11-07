---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 554a754d8d7e6000556b2141807d2b6fe86cc230
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894241"
---
# <span data-ttu-id="892ea-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="892ea-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="892ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="892ea-102">SYNOPSIS</span></span>
<span data-ttu-id="892ea-103">Ustawia ustawienia dzienników i metryk dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="892ea-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="892ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="892ea-104">SYNTAX</span></span>

### <span data-ttu-id="892ea-105">OldSetDiagnosticSetting (domyślny)</span><span class="sxs-lookup"><span data-stu-id="892ea-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-ExportToResourceSpecific] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="892ea-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="892ea-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="892ea-107">Opis</span><span class="sxs-lookup"><span data-stu-id="892ea-107">DESCRIPTION</span></span>
<span data-ttu-id="892ea-108">Polecenie cmdlet **Set-AzDiagnosticSetting** włącza lub wyłącza każdą kategorię ziarno i dziennik dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="892ea-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="892ea-109">Dzienniki i metryki są przechowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="892ea-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="892ea-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="892ea-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="892ea-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="892ea-111">EXAMPLES</span></span>

### <span data-ttu-id="892ea-112">Przykład 1. Włączanie wszystkich metryk i dzienników dla zasobu</span><span class="sxs-lookup"><span data-stu-id="892ea-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="892ea-113">To polecenie umożliwia włączenie wszystkich dostępnych metryk i dzienników dla Resource01.</span><span class="sxs-lookup"><span data-stu-id="892ea-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="892ea-114">Przykład 2: wyłączenie wszystkich metryk i dzienników</span><span class="sxs-lookup"><span data-stu-id="892ea-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="892ea-115">To polecenie powoduje wyłączenie wszystkich dostępnych metryk i dzienników dla Resource01 zasobów.</span><span class="sxs-lookup"><span data-stu-id="892ea-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="892ea-116">Przykład 3: Włączanie/wyłączanie kategorii wielu metryk</span><span class="sxs-lookup"><span data-stu-id="892ea-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="892ea-117">To polecenie wyłącza kategorie metryk o nazwie Category1 oraz Category2.</span><span class="sxs-lookup"><span data-stu-id="892ea-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="892ea-118">Wszystkie pozostałe kategorie pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="892ea-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="892ea-119">Przykład 4: Włączanie/wyłączanie wielu kategorii dziennika</span><span class="sxs-lookup"><span data-stu-id="892ea-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="892ea-120">To polecenie umożliwia włączenie Category1 i Category2.</span><span class="sxs-lookup"><span data-stu-id="892ea-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="892ea-121">Wszystkie pozostałe kategorie metryk i dzienniki pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="892ea-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="892ea-122">Przykład 4: Włączanie ziarna czasu i wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="892ea-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="892ea-123">To polecenie umożliwia włączenie tylko Category1, Category2 i ziarna PT1M.</span><span class="sxs-lookup"><span data-stu-id="892ea-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="892ea-124">Wszystkie pozostałe ziarno i kategorie są niezmienione.</span><span class="sxs-lookup"><span data-stu-id="892ea-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="892ea-125">Przykład 5: korzystanie z rurociągu</span><span class="sxs-lookup"><span data-stu-id="892ea-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="892ea-126">To polecenie używa potoku programu PowerShell do ustawiania (bez zmiany) ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="892ea-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="892ea-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="892ea-127">PARAMETERS</span></span>

### <span data-ttu-id="892ea-128">-Category</span><span class="sxs-lookup"><span data-stu-id="892ea-128">-Category</span></span>
<span data-ttu-id="892ea-129">Określa listę kategorii dziennika, które mają zostać włączone lub wyłączone, zgodnie z wartością *włączoną*.</span><span class="sxs-lookup"><span data-stu-id="892ea-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="892ea-130">Jeśli nie podano żadnej kategorii, to polecenie będzie działać we wszystkich obsługiwanych kategoriach.</span><span class="sxs-lookup"><span data-stu-id="892ea-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892ea-131">-DefaultProfile</span></span>
<span data-ttu-id="892ea-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="892ea-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="892ea-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="892ea-133">-Enabled</span></span>
<span data-ttu-id="892ea-134">Wskazuje, czy włączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="892ea-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="892ea-135">Określ $True, aby włączyć diagnostykę, lub $False, aby wyłączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="892ea-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="892ea-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="892ea-137">Identyfikator reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="892ea-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="892ea-138">-EventHubName</span></span>
<span data-ttu-id="892ea-139">Nazwa centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="892ea-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-140">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="892ea-140">-ExportToResourceSpecific</span></span>
<span data-ttu-id="892ea-141">Flaga wskazująca, że eksport do elementu LA musi zostać wykonany w tabeli określonego zasobu, vel</span><span class="sxs-lookup"><span data-stu-id="892ea-141">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="892ea-142">tabela schematów dedykowana lub stała, w przeciwieństwie do **domyślnej** tabeli schematu dynamicznego o nazwie **AzureDiagnostics**.</span><span class="sxs-lookup"><span data-stu-id="892ea-142">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="892ea-143">Ten argument obowiązuje tylko wtedy, gdy podany jest również argument **-workspaceId** .</span><span class="sxs-lookup"><span data-stu-id="892ea-143">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="892ea-144">-InputObject</span></span>
<span data-ttu-id="892ea-145">Obiekt wejściowy (możliwy z potoku). Nazwa i identyfikator zasobu zostaną wyodrębnione z tego obiektu.</span><span class="sxs-lookup"><span data-stu-id="892ea-145">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-146">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="892ea-146">-MetricCategory</span></span>
<span data-ttu-id="892ea-147">Lista kategorii metrycznych.</span><span class="sxs-lookup"><span data-stu-id="892ea-147">The list of metric categories.</span></span> <span data-ttu-id="892ea-148">Jeśli nie podano żadnej kategorii, to polecenie będzie działać we wszystkich obsługiwanych kategoriach.</span><span class="sxs-lookup"><span data-stu-id="892ea-148">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="892ea-149">-Name</span></span>
<span data-ttu-id="892ea-150">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="892ea-150">The name of the diagnostic setting.</span></span> <span data-ttu-id="892ea-151">Wartość domyślna to **Usługa**.</span><span class="sxs-lookup"><span data-stu-id="892ea-151">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="892ea-152">-ResourceId</span></span>
<span data-ttu-id="892ea-153">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="892ea-153">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-154">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="892ea-154">-RetentionEnabled</span></span>
<span data-ttu-id="892ea-155">Wskazuje, czy zachowywanie informacji diagnostycznych jest włączone.</span><span class="sxs-lookup"><span data-stu-id="892ea-155">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-156">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="892ea-156">-RetentionInDays</span></span>
<span data-ttu-id="892ea-157">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="892ea-157">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-158">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="892ea-158">-ServiceBusRuleId</span></span>
<span data-ttu-id="892ea-159">Identyfikator reguły usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="892ea-159">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-160">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="892ea-160">-StorageAccountId</span></span>
<span data-ttu-id="892ea-161">Określa identyfikator konta magazynu, w którym należy zapisać dane.</span><span class="sxs-lookup"><span data-stu-id="892ea-161">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-162">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="892ea-162">-Timegrain</span></span>
<span data-ttu-id="892ea-163">Określa ziarno czasu, w którym można włączać lub wyłączać metryki w zależności od wartości *włączonego*.</span><span class="sxs-lookup"><span data-stu-id="892ea-163">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="892ea-164">Jeśli nie określisz ziarna, to polecenie będzie działać na wszystkich dostępnych ziarnach czasu.</span><span class="sxs-lookup"><span data-stu-id="892ea-164">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-165">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="892ea-165">-WorkspaceId</span></span>
<span data-ttu-id="892ea-166">Identyfikator obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="892ea-166">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="892ea-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="892ea-167">-Confirm</span></span>
<span data-ttu-id="892ea-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="892ea-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="892ea-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="892ea-169">-WhatIf</span></span>
<span data-ttu-id="892ea-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="892ea-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="892ea-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="892ea-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="892ea-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892ea-172">CommonParameters</span></span>
<span data-ttu-id="892ea-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892ea-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892ea-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="892ea-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892ea-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="892ea-175">INPUTS</span></span>

### <span data-ttu-id="892ea-176">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="892ea-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="892ea-177">System. String</span><span class="sxs-lookup"><span data-stu-id="892ea-177">System.String</span></span>

### <span data-ttu-id="892ea-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="892ea-178">System.Boolean</span></span>

### <span data-ttu-id="892ea-179">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="892ea-179">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="892ea-180">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="892ea-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="892ea-181">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="892ea-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="892ea-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="892ea-182">OUTPUTS</span></span>

### <span data-ttu-id="892ea-183">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="892ea-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="892ea-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="892ea-184">NOTES</span></span>

## <span data-ttu-id="892ea-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="892ea-185">RELATED LINKS</span></span>

<span data-ttu-id="892ea-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="892ea-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
