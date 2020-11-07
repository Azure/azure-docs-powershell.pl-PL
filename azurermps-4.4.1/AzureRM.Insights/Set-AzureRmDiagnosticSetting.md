---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717837"
---
# <span data-ttu-id="41b6c-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="41b6c-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="41b6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="41b6c-103">Ustawia ustawienia dzienników i metryk dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="41b6c-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41b6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41b6c-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41b6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="41b6c-106">Polecenie cmdlet **Set-AzureRmDiagnosticSetting** włącza lub wyłącza każdą kategorię ziarno i dziennik dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="41b6c-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="41b6c-107">Dzienniki i metryki są przechowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="41b6c-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="41b6c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41b6c-108">EXAMPLES</span></span>

### <span data-ttu-id="41b6c-109">Przykład 1. Włączanie wszystkich metryk i dzienników dla zasobu</span><span class="sxs-lookup"><span data-stu-id="41b6c-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="41b6c-110">To polecenie umożliwia włączenie wszystkich dostępnych metryk i dzienników dla Resource01.</span><span class="sxs-lookup"><span data-stu-id="41b6c-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="41b6c-111">Przykład 2: wyłączenie wszystkich metryk i dzienników</span><span class="sxs-lookup"><span data-stu-id="41b6c-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="41b6c-112">To polecenie powoduje wyłączenie wszystkich dostępnych metryk i dzienników dla Resource01 zasobów.</span><span class="sxs-lookup"><span data-stu-id="41b6c-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="41b6c-113">Przykład 3: Włączanie wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="41b6c-113">Example 3: Enable multiple categories</span></span>
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

<span data-ttu-id="41b6c-114">To polecenie umożliwia włączenie Category1 i Category2.</span><span class="sxs-lookup"><span data-stu-id="41b6c-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="41b6c-115">Wszystkie timegrains i inne kategorie pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="41b6c-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="41b6c-116">Przykład 4: Włączanie ziarna czasu i wielu kategorii</span><span class="sxs-lookup"><span data-stu-id="41b6c-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="41b6c-117">To polecenie umożliwia włączenie tylko Category1, Category2 i ziarna PT1M.</span><span class="sxs-lookup"><span data-stu-id="41b6c-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="41b6c-118">Wszystkie pozostałe ziarno i kategorie są niezmienione.</span><span class="sxs-lookup"><span data-stu-id="41b6c-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="41b6c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41b6c-119">PARAMETERS</span></span>

### <span data-ttu-id="41b6c-120">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="41b6c-120">-Categories</span></span>
<span data-ttu-id="41b6c-121">Określa listę kategorii dziennika, które mają zostać włączone lub wyłączone, zgodnie z wartością *włączoną*.</span><span class="sxs-lookup"><span data-stu-id="41b6c-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="41b6c-122">Jeśli nie określisz kategorii, to polecenie będzie działać we wszystkich kategoriach.</span><span class="sxs-lookup"><span data-stu-id="41b6c-122">If you do not specify a category, this command operates on all categories.</span></span>

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

### <span data-ttu-id="41b6c-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="41b6c-123">-Enabled</span></span>
<span data-ttu-id="41b6c-124">Wskazuje, czy włączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="41b6c-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="41b6c-125">Określ $True, aby włączyć diagnostykę, lub $False, aby wyłączyć diagnostykę.</span><span class="sxs-lookup"><span data-stu-id="41b6c-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41b6c-126">-ResourceId</span></span>
<span data-ttu-id="41b6c-127">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="41b6c-127">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="41b6c-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="41b6c-128">-RetentionEnabled</span></span>
<span data-ttu-id="41b6c-129">Wskazuje, czy zachowywanie informacji diagnostycznych jest włączone.</span><span class="sxs-lookup"><span data-stu-id="41b6c-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="41b6c-130">-RetentionInDays</span></span>
<span data-ttu-id="41b6c-131">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="41b6c-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="41b6c-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="41b6c-133">-StorageAccountId</span></span>
<span data-ttu-id="41b6c-134">Określa identyfikator konta magazynu, w którym należy zapisać dane.</span><span class="sxs-lookup"><span data-stu-id="41b6c-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="41b6c-135">-Timegrains</span></span>
<span data-ttu-id="41b6c-136">Określa ziarno czasu, w którym można włączać lub wyłączać metryki w zależności od wartości *włączonego*.</span><span class="sxs-lookup"><span data-stu-id="41b6c-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="41b6c-137">Jeśli nie określisz ziarna, to polecenie będzie działać na wszystkich dostępnych ziarnach czasu.</span><span class="sxs-lookup"><span data-stu-id="41b6c-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="41b6c-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="41b6c-138">-WorkspaceId</span></span>
<span data-ttu-id="41b6c-139">Identyfikator obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="41b6c-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b6c-140">-DefaultProfile</span></span>
<span data-ttu-id="41b6c-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41b6c-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b6c-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="41b6c-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="41b6c-143">Identyfikator reguły centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="41b6c-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b6c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b6c-144">CommonParameters</span></span>
<span data-ttu-id="41b6c-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b6c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b6c-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b6c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b6c-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41b6c-147">INPUTS</span></span>

## <span data-ttu-id="41b6c-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41b6c-148">OUTPUTS</span></span>

### <span data-ttu-id="41b6c-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="41b6c-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="41b6c-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41b6c-150">NOTES</span></span>

## <span data-ttu-id="41b6c-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41b6c-151">RELATED LINKS</span></span>

[<span data-ttu-id="41b6c-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="41b6c-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


