---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526822"
---
# <span data-ttu-id="a8fb1-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a8fb1-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="a8fb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fb1-103">Ustawia ustawienia dzienników i metryk dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8fb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8fb1-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8fb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="a8fb1-106">Polecenie cmdlet **Set-AzureRmDiagnosticSetting** włącza lub wyłącza każdą kategorię ziarno i dziennik dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="a8fb1-107">Dzienniki i metryki są przechowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-107">The logs and metrics are stored in the specified storage account.</span></span>

<span data-ttu-id="a8fb1-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a8fb1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8fb1-109">EXAMPLES</span></span>

### <span data-ttu-id="a8fb1-110">Przykład 1. Włączanie wszystkich metryk i dzienników dla zasobu</span><span class="sxs-lookup"><span data-stu-id="a8fb1-110">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="a8fb1-111">To polecenie umożliwia włączenie wszystkich dostępnych metryk i dzienników dla Resource01.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-111">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="a8fb1-112">Przykład 2: wyłączenie wszystkich metryk i dzienników</span><span class="sxs-lookup"><span data-stu-id="a8fb1-112">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="a8fb1-113">To polecenie powoduje wyłączenie wszystkich dostępnych metryk i dzienników dla Resource01 zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-113">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="a8fb1-114">Przykład 3: Włączanie wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="a8fb1-114">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
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

<span data-ttu-id="a8fb1-115">To polecenie umożliwia włączenie Category1 i Category2.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-115">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="a8fb1-116">Wszystkie timegrains i inne kategorie pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-116">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="a8fb1-117">Przykład 4: Włączanie ziarna czasu i wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="a8fb1-117">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="a8fb1-118">To polecenie umożliwia włączenie tylko Category1, Category2 i ziarna PT1M.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-118">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="a8fb1-119">Wszystkie pozostałe ziarno i kategorie są niezmienione.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-119">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="a8fb1-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8fb1-120">PARAMETERS</span></span>

### <span data-ttu-id="a8fb1-121">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="a8fb1-121">-Categories</span></span>
<span data-ttu-id="a8fb1-122">Określa listę kategorii dziennika, które mają zostać włączone lub wyłączone, zgodnie z wartością *włączoną*.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-122">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="a8fb1-123">Jeśli nie określisz kategorii, to polecenie będzie działać we wszystkich kategoriach.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-123">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fb1-124">-DefaultProfile</span></span>
<span data-ttu-id="a8fb1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a8fb1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8fb1-126">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a8fb1-126">-Enabled</span></span>
<span data-ttu-id="a8fb1-127">Wskazuje, czy włączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-127">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="a8fb1-128">Określ $True, aby włączyć diagnostykę, lub $False, aby wyłączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-128">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-129">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="a8fb1-129">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="a8fb1-130">Reguła centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="a8fb1-130">The event hub rule i</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8fb1-131">-ResourceId</span></span>
<span data-ttu-id="a8fb1-132">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-132">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-133">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="a8fb1-133">-RetentionEnabled</span></span>
<span data-ttu-id="a8fb1-134">Wskazuje, czy zachowywanie informacji diagnostycznych jest włączone.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-134">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a8fb1-135">-RetentionInDays</span></span>
<span data-ttu-id="a8fb1-136">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-136">Specifies the retention policy, in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-137">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="a8fb1-137">-ServiceBusRuleId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a8fb1-138">-StorageAccountId</span></span>
<span data-ttu-id="a8fb1-139">Określa identyfikator konta magazynu, w którym należy zapisać dane.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-139">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-140">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="a8fb1-140">-Timegrains</span></span>
<span data-ttu-id="a8fb1-141">Określa ziarno czasu, w którym można włączać lub wyłączać metryki w zależności od wartości *włączonego*.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-141">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="a8fb1-142">Jeśli nie określisz ziarna, to polecenie będzie działać na wszystkich dostępnych ziarnach czasu.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-142">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-143">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a8fb1-143">-WorkspaceId</span></span>
<span data-ttu-id="a8fb1-144">Identyfikator obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a8fb1-144">The Id of the workspace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fb1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fb1-145">CommonParameters</span></span>
<span data-ttu-id="a8fb1-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fb1-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8fb1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fb1-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8fb1-148">INPUTS</span></span>

### <span data-ttu-id="a8fb1-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8fb1-149">None</span></span>
<span data-ttu-id="a8fb1-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a8fb1-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8fb1-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8fb1-151">OUTPUTS</span></span>

### <span data-ttu-id="a8fb1-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="a8fb1-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="a8fb1-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8fb1-153">NOTES</span></span>

## <span data-ttu-id="a8fb1-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8fb1-154">RELATED LINKS</span></span>

[<span data-ttu-id="a8fb1-155">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a8fb1-155">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


