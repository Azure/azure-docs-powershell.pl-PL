---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: 772fe33dab13c4c92a0e17fc09a6bf1d5aa04624
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897418"
---
# <span data-ttu-id="71e24-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="71e24-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="71e24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71e24-102">SYNOPSIS</span></span>
<span data-ttu-id="71e24-103">Ustawia ustawienia dzienników i metryk dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="71e24-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71e24-104">SYNTAX</span></span>

### <span data-ttu-id="71e24-105">OldSetDiagnosticSetting (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71e24-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e24-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="71e24-106">NewSetDiagnosticSetting</span></span>
```
Set-AzureRmDiagnosticSetting -InputObject <PSServiceDiagnosticSettings>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e24-107">Opis</span><span class="sxs-lookup"><span data-stu-id="71e24-107">DESCRIPTION</span></span>
<span data-ttu-id="71e24-108">Polecenie cmdlet **Set-AzureRmDiagnosticSetting** włącza lub wyłącza każdą kategorię ziarno i dziennik dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="71e24-108">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="71e24-109">Dzienniki i metryki są przechowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="71e24-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="71e24-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="71e24-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="71e24-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71e24-111">EXAMPLES</span></span>

### <span data-ttu-id="71e24-112">Przykład 1. Włączanie wszystkich metryk i dzienników dla zasobu</span><span class="sxs-lookup"><span data-stu-id="71e24-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="71e24-113">To polecenie umożliwia włączenie wszystkich dostępnych metryk i dzienników dla Resource01.</span><span class="sxs-lookup"><span data-stu-id="71e24-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="71e24-114">Przykład 2: wyłączenie wszystkich metryk i dzienników</span><span class="sxs-lookup"><span data-stu-id="71e24-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="71e24-115">To polecenie powoduje wyłączenie wszystkich dostępnych metryk i dzienników dla Resource01 zasobów.</span><span class="sxs-lookup"><span data-stu-id="71e24-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="71e24-116">Przykład 3: Włączanie/wyłączanie kategorii wielu metryk</span><span class="sxs-lookup"><span data-stu-id="71e24-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
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

<span data-ttu-id="71e24-117">To polecenie włącza metryki cateories o nazwie Category1 i Category2.</span><span class="sxs-lookup"><span data-stu-id="71e24-117">This command enables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="71e24-118">Wszystkie pozostałe kategorie pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="71e24-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="71e24-119">Przykład 4: Włączanie/wyłączanie wielu kategorii dziennika</span><span class="sxs-lookup"><span data-stu-id="71e24-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
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

<span data-ttu-id="71e24-120">To polecenie umożliwia włączenie Category1 i Category2.</span><span class="sxs-lookup"><span data-stu-id="71e24-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="71e24-121">Wszystkie pozostałe kategorie metryk i dzienniki pozostają bez zmian.</span><span class="sxs-lookup"><span data-stu-id="71e24-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="71e24-122">Przykład 4: Włączanie ziarna czasu i wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="71e24-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="71e24-123">To polecenie umożliwia włączenie tylko Category1, Category2 i ziarna PT1M.</span><span class="sxs-lookup"><span data-stu-id="71e24-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="71e24-124">Wszystkie pozostałe ziarno i kategorie są niezmienione.</span><span class="sxs-lookup"><span data-stu-id="71e24-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="71e24-125">Przykład 5: korzystanie z rurociągu</span><span class="sxs-lookup"><span data-stu-id="71e24-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "Resource01" | Set-AzureRmDiagnosticSetting
```

<span data-ttu-id="71e24-126">To polecenie używa potoku programu PowerShell w celu ustawienia ustawień diagnostycznych (nie dokonania zmiany).</span><span class="sxs-lookup"><span data-stu-id="71e24-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="71e24-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71e24-127">PARAMETERS</span></span>

### <span data-ttu-id="71e24-128">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="71e24-128">-Categories</span></span>
<span data-ttu-id="71e24-129">Określa listę kategorii dziennika, które mają zostać włączone lub wyłączone, zgodnie z wartością *włączoną*.</span><span class="sxs-lookup"><span data-stu-id="71e24-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="71e24-130">Jeśli nie podano żadnej kategorii, to polecenie będzie działać we wszystkich obsługiwanych kategoriach.</span><span class="sxs-lookup"><span data-stu-id="71e24-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Category

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e24-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e24-131">-DefaultProfile</span></span>
<span data-ttu-id="71e24-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="71e24-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e24-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="71e24-133">-Enabled</span></span>
<span data-ttu-id="71e24-134">Wskazuje, czy włączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="71e24-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="71e24-135">Określ $True, aby włączyć diagnostykę, lub $False, aby wyłączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="71e24-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="71e24-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="71e24-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="71e24-137">Identyfikator reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="71e24-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="71e24-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="71e24-138">-EventHubName</span></span>
<span data-ttu-id="71e24-139">Nazwa centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="71e24-139">The event hub name</span></span>

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

### <span data-ttu-id="71e24-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71e24-140">-InputObject</span></span>
<span data-ttu-id="71e24-141">Obiekt wejściowy (możliwy z potoku). Nazwa i identyfikator zasobu zostaną wyodrębnione z tego obiektu.</span><span class="sxs-lookup"><span data-stu-id="71e24-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="71e24-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="71e24-142">-MetricCategory</span></span>
<span data-ttu-id="71e24-143">Lista kategorii metrycznych.</span><span class="sxs-lookup"><span data-stu-id="71e24-143">The list of metric categories.</span></span> <span data-ttu-id="71e24-144">Jeśli nie podano żadnej kategorii, to polecenie będzie działać we wszystkich obsługiwanych kategoriach.</span><span class="sxs-lookup"><span data-stu-id="71e24-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="71e24-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71e24-145">-Name</span></span>
<span data-ttu-id="71e24-146">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="71e24-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="71e24-147">Wartość domyślna to **Usługa**.</span><span class="sxs-lookup"><span data-stu-id="71e24-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="71e24-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71e24-148">-ResourceId</span></span>
<span data-ttu-id="71e24-149">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="71e24-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="71e24-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="71e24-150">-RetentionEnabled</span></span>
<span data-ttu-id="71e24-151">Wskazuje, czy zachowywanie informacji diagnostycznych jest włączone.</span><span class="sxs-lookup"><span data-stu-id="71e24-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="71e24-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="71e24-152">-RetentionInDays</span></span>
<span data-ttu-id="71e24-153">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="71e24-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="71e24-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="71e24-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="71e24-155">Identyfikator reguły usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="71e24-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="71e24-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71e24-156">-StorageAccountId</span></span>
<span data-ttu-id="71e24-157">Określa identyfikator konta magazynu, w którym należy zapisać dane.</span><span class="sxs-lookup"><span data-stu-id="71e24-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="71e24-158">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="71e24-158">-Timegrains</span></span>
<span data-ttu-id="71e24-159">Określa ziarno czasu, w którym można włączać lub wyłączać metryki w zależności od wartości *włączonego*.</span><span class="sxs-lookup"><span data-stu-id="71e24-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="71e24-160">Jeśli nie określisz ziarna, to polecenie będzie działać na wszystkich dostępnych ziarnach czasu.</span><span class="sxs-lookup"><span data-stu-id="71e24-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Timegrain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e24-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="71e24-161">-WorkspaceId</span></span>
<span data-ttu-id="71e24-162">Identyfikator obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="71e24-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="71e24-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71e24-163">-Confirm</span></span>
<span data-ttu-id="71e24-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e24-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e24-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e24-165">-WhatIf</span></span>
<span data-ttu-id="71e24-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e24-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71e24-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71e24-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e24-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e24-168">CommonParameters</span></span>
<span data-ttu-id="71e24-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e24-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e24-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e24-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e24-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e24-171">INPUTS</span></span>

### <span data-ttu-id="71e24-172">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="71e24-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>
<span data-ttu-id="71e24-173">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71e24-173">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="71e24-174">System. String</span><span class="sxs-lookup"><span data-stu-id="71e24-174">System.String</span></span>

### <span data-ttu-id="71e24-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71e24-175">System.Boolean</span></span>

### <span data-ttu-id="71e24-176">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71e24-176">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="71e24-177">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71e24-177">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="71e24-178">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71e24-178">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="71e24-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71e24-179">OUTPUTS</span></span>

### <span data-ttu-id="71e24-180">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="71e24-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="71e24-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71e24-181">NOTES</span></span>

## <span data-ttu-id="71e24-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e24-182">RELATED LINKS</span></span>

<span data-ttu-id="71e24-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="71e24-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
