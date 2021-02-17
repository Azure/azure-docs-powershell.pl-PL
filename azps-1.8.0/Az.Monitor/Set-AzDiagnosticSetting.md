---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 6f78e11fc6a5ef5cca2148258db9effd044b8c25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402817"
---
# <span data-ttu-id="8ce77-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8ce77-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="8ce77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ce77-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce77-103">Ustawia ustawienia dzienników i metryk dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="8ce77-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="8ce77-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ce77-104">SYNTAX</span></span>

### <span data-ttu-id="8ce77-105">OldSetDiagnosticSetting (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8ce77-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ce77-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8ce77-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce77-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ce77-107">DESCRIPTION</span></span>
<span data-ttu-id="8ce77-108">Polecenie **cmdlet Set-AzDiagnosticSetting** włącza lub wyłącza każdą kategorię czasową i kategorię dziennika dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="8ce77-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="8ce77-109">Dzienniki i metryki są przechowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="8ce77-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="8ce77-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="8ce77-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8ce77-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ce77-111">EXAMPLES</span></span>

### <span data-ttu-id="8ce77-112">Przykład 1. Włączanie wszystkich metryk i dzienników dla zasobu</span><span class="sxs-lookup"><span data-stu-id="8ce77-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="8ce77-113">To polecenie udostępnia wszystkie dostępne metryki i dzienniki dla zasobu Resource01.</span><span class="sxs-lookup"><span data-stu-id="8ce77-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="8ce77-114">Przykład 2. Wyłączanie wszystkich metryk i dzienników</span><span class="sxs-lookup"><span data-stu-id="8ce77-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="8ce77-115">To polecenie wyłącza wszystkie dostępne metryki i dzienniki dla zasobu Resource01.</span><span class="sxs-lookup"><span data-stu-id="8ce77-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="8ce77-116">Przykład 3. Włączanie/wyłączanie wielu kategorii metryk</span><span class="sxs-lookup"><span data-stu-id="8ce77-116">Example 3: Enable/disable multiple metrics categories</span></span>
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

<span data-ttu-id="8ce77-117">To polecenie wyłącza kategorie metryk o nazwach Kategoria1 i Kategoria2.</span><span class="sxs-lookup"><span data-stu-id="8ce77-117">This command disables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="8ce77-118">Wszystkie pozostałe kategorie pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="8ce77-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="8ce77-119">Przykład 4. Włączanie/wyłączanie wielu kategorii dziennika</span><span class="sxs-lookup"><span data-stu-id="8ce77-119">Example 4: Enable/disable multiple log categories</span></span>
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

<span data-ttu-id="8ce77-120">To polecenie umożliwia włączenie kategorii Kategoria1 i Kategoria2.</span><span class="sxs-lookup"><span data-stu-id="8ce77-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="8ce77-121">Wszystkie pozostałe metryki i kategorie dzienników pozostają takie same.</span><span class="sxs-lookup"><span data-stu-id="8ce77-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="8ce77-122">Przykład 4. Włączanie odsłoń czasu i wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="8ce77-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="8ce77-123">To polecenie włącza tylko kategorię Category1, Category2 i time grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="8ce77-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="8ce77-124">Wszystkie pozostałe kategorie i kategorie czasu pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="8ce77-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="8ce77-125">Przykład 5. Korzystanie z potoku</span><span class="sxs-lookup"><span data-stu-id="8ce77-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="8ce77-126">To polecenie używa potoku programu PowerShell do ustawienia ustawienia diagnostycznego (bez zmian).</span><span class="sxs-lookup"><span data-stu-id="8ce77-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="8ce77-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ce77-127">PARAMETERS</span></span>

### <span data-ttu-id="8ce77-128">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="8ce77-128">-Category</span></span>
<span data-ttu-id="8ce77-129">Określa listę kategorii dziennika do włączenia lub wyłączenia zgodnie z *wartością* Włączone.</span><span class="sxs-lookup"><span data-stu-id="8ce77-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="8ce77-130">Jeśli nie zostanie określona żadna kategoria, to polecenie będzie działać na wszystkich obsługiwanych kategoriach.</span><span class="sxs-lookup"><span data-stu-id="8ce77-130">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="8ce77-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce77-131">-DefaultProfile</span></span>
<span data-ttu-id="8ce77-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8ce77-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ce77-133">— włączone</span><span class="sxs-lookup"><span data-stu-id="8ce77-133">-Enabled</span></span>
<span data-ttu-id="8ce77-134">Wskazuje, czy włączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="8ce77-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="8ce77-135">Określ $True, aby włączyć diagnostykę, lub określ, $False wyłączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="8ce77-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="8ce77-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="8ce77-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="8ce77-137">Identyfikator reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="8ce77-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="8ce77-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8ce77-138">-EventHubName</span></span>
<span data-ttu-id="8ce77-139">Nazwa centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="8ce77-139">The event hub name</span></span>

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

### <span data-ttu-id="8ce77-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ce77-140">-InputObject</span></span>
<span data-ttu-id="8ce77-141">Obiekt wejściowy (możliwe z potoku). Nazwa i identyfikator zasobu zostaną wyodrębnione z tego obiektu.</span><span class="sxs-lookup"><span data-stu-id="8ce77-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="8ce77-142">- MetricCategory</span><span class="sxs-lookup"><span data-stu-id="8ce77-142">-MetricCategory</span></span>
<span data-ttu-id="8ce77-143">Lista kategorii metrycznych.</span><span class="sxs-lookup"><span data-stu-id="8ce77-143">The list of metric categories.</span></span>
<span data-ttu-id="8ce77-144">Jeśli nie zostanie określona żadna kategoria, to polecenie będzie działać na wszystkich obsługiwanych kategoriach.</span><span class="sxs-lookup"><span data-stu-id="8ce77-144">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="8ce77-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ce77-145">-Name</span></span>
<span data-ttu-id="8ce77-146">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="8ce77-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="8ce77-147">Wartość domyślna to **usługa.**</span><span class="sxs-lookup"><span data-stu-id="8ce77-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="8ce77-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ce77-148">-ResourceId</span></span>
<span data-ttu-id="8ce77-149">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8ce77-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="8ce77-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="8ce77-150">-RetentionEnabled</span></span>
<span data-ttu-id="8ce77-151">Wskazuje, czy jest włączone przechowywanie informacji diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="8ce77-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="8ce77-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8ce77-152">-RetentionInDays</span></span>
<span data-ttu-id="8ce77-153">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="8ce77-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="8ce77-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="8ce77-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="8ce77-155">Identyfikator reguły autobusu usługowego.</span><span class="sxs-lookup"><span data-stu-id="8ce77-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="8ce77-156">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8ce77-156">-StorageAccountId</span></span>
<span data-ttu-id="8ce77-157">Określa identyfikator konta magazynu, na którym mają być zapisywanie danych.</span><span class="sxs-lookup"><span data-stu-id="8ce77-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="8ce77-158">- Timegrain</span><span class="sxs-lookup"><span data-stu-id="8ce77-158">-Timegrain</span></span>
<span data-ttu-id="8ce77-159">Określa czas, który należy włączyć lub wyłączyć dla metryk, zgodnie z wartością *Włączone.*</span><span class="sxs-lookup"><span data-stu-id="8ce77-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="8ce77-160">Jeśli nie zostanie określony czasowy, to polecenie będzie dotyczyć wszystkich dostępnych okresów.</span><span class="sxs-lookup"><span data-stu-id="8ce77-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="8ce77-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="8ce77-161">-WorkspaceId</span></span>
<span data-ttu-id="8ce77-162">Identyfikator zasobu obszaru roboczego analizy dziennika do wysyłania dzienników/metryk do</span><span class="sxs-lookup"><span data-stu-id="8ce77-162">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="8ce77-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ce77-163">-Confirm</span></span>
<span data-ttu-id="8ce77-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ce77-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce77-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce77-165">-WhatIf</span></span>
<span data-ttu-id="8ce77-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce77-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ce77-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8ce77-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce77-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce77-168">CommonParameters</span></span>
<span data-ttu-id="8ce77-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce77-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce77-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce77-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce77-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ce77-171">INPUTS</span></span>

### <span data-ttu-id="8ce77-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8ce77-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="8ce77-173">System.String</span><span class="sxs-lookup"><span data-stu-id="8ce77-173">System.String</span></span>

### <span data-ttu-id="8ce77-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ce77-174">System.Boolean</span></span>

### <span data-ttu-id="8ce77-175">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ce77-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ce77-176">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ce77-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ce77-177">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ce77-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8ce77-178">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ce77-178">OUTPUTS</span></span>

### <span data-ttu-id="8ce77-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8ce77-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="8ce77-180">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ce77-180">NOTES</span></span>

## <span data-ttu-id="8ce77-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ce77-181">RELATED LINKS</span></span>

<span data-ttu-id="8ce77-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="8ce77-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
