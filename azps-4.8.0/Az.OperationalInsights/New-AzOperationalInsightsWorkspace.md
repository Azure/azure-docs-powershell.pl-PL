---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8515bf4085fcd03d87aa15c3da649fe318b94966
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405010"
---
# <span data-ttu-id="68df3-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="68df3-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="68df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68df3-102">SYNOPSIS</span></span>
<span data-ttu-id="68df3-103">Tworzy obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="68df3-103">Creates a workspace.</span></span>

## <span data-ttu-id="68df3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68df3-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68df3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="68df3-105">DESCRIPTION</span></span>
<span data-ttu-id="68df3-106">Polecenie **cmdlet New-AzOperationalInsightsWorkspace** tworzy obszar roboczy w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="68df3-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="68df3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68df3-107">EXAMPLES</span></span>

### <span data-ttu-id="68df3-108">Przykład 1. Tworzenie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="68df3-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="68df3-109">To polecenie tworzy standardowy obszar roboczy SKU o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68df3-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="68df3-110">Przykład 2. Tworzenie obszaru roboczego i łączenie go z istniejącym kontem</span><span class="sxs-lookup"><span data-stu-id="68df3-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="68df3-111">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsLinkTargets w celu uzyskania celów docelowych linku do konta w szczegółowych informacjach operacyjnych, a następnie przechowuje je w $OILinkTargets danych.</span><span class="sxs-lookup"><span data-stu-id="68df3-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="68df3-112">Drugie polecenie przekazuje pierwszy element docelowy linku do konta w $OILinkTargets do polecenia cmdlet **New-AzOperationalInsightsWorkspace** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="68df3-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="68df3-113">Polecenie tworzy standardowy obszar roboczy SKU o nazwie MyWorkspace, który jest połączony z pierwszym kontem szczegółowych informacji operacyjnych w programie $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="68df3-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="68df3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68df3-114">PARAMETERS</span></span>

### <span data-ttu-id="68df3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68df3-115">-DefaultProfile</span></span>
<span data-ttu-id="68df3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="68df3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68df3-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="68df3-117">-Force</span></span>
<span data-ttu-id="68df3-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="68df3-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="68df3-119">-Location</span></span>
<span data-ttu-id="68df3-120">Określa lokalizację, w której ma być tworzyć obszar roboczy, na przykład Wschód Stany Zjednoczone lub Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="68df3-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="68df3-121">-Name</span></span>
<span data-ttu-id="68df3-122">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68df3-122">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="68df3-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="68df3-124">Typ dostępu sieciowego do uzyskiwania dostępu do obszaru roboczego ingestion.</span><span class="sxs-lookup"><span data-stu-id="68df3-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="68df3-125">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="68df3-125">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="68df3-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="68df3-127">Typ dostępu sieciowego do uzyskiwania dostępu do zapytania obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68df3-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="68df3-128">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="68df3-128">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68df3-129">-ResourceGroupName</span></span>
<span data-ttu-id="68df3-130">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="68df3-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="68df3-131">Obszar roboczy zostanie utworzony w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="68df3-131">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="68df3-132">-RetentionInDays</span></span>
<span data-ttu-id="68df3-133">Przechowywanie danych obszaru roboczego w dniach.</span><span class="sxs-lookup"><span data-stu-id="68df3-133">The workspace data retention in days.</span></span> <span data-ttu-id="68df3-134">730 dni to maksimum dozwolone dla wszystkich pozostałych jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="68df3-134">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-135">- SKU</span><span class="sxs-lookup"><span data-stu-id="68df3-135">-Sku</span></span>
<span data-ttu-id="68df3-136">Określa warstwę usługi obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68df3-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="68df3-137">Aby uzyskać więcej informacji dotyczących wartości, której należy użyć, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers sprawdź.</span><span class="sxs-lookup"><span data-stu-id="68df3-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="68df3-138">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="68df3-138">Valid values are:</span></span>
- <span data-ttu-id="68df3-139">bezpłatnie</span><span class="sxs-lookup"><span data-stu-id="68df3-139">free</span></span>
- <span data-ttu-id="68df3-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="68df3-140">pergb2018</span></span>
- <span data-ttu-id="68df3-141">pernode</span><span class="sxs-lookup"><span data-stu-id="68df3-141">pernode</span></span>
- <span data-ttu-id="68df3-142">premium</span><span class="sxs-lookup"><span data-stu-id="68df3-142">premium</span></span>
- <span data-ttu-id="68df3-143">autonomiczny</span><span class="sxs-lookup"><span data-stu-id="68df3-143">standalone</span></span>
- <span data-ttu-id="68df3-144">standardowy</span><span class="sxs-lookup"><span data-stu-id="68df3-144">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-145">— Tag</span><span class="sxs-lookup"><span data-stu-id="68df3-145">-Tag</span></span>
<span data-ttu-id="68df3-146">Tagi zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="68df3-146">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68df3-147">-Confirm</span></span>
<span data-ttu-id="68df3-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="68df3-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68df3-149">-WhatIf</span></span>
<span data-ttu-id="68df3-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68df3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68df3-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="68df3-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68df3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68df3-152">CommonParameters</span></span>
<span data-ttu-id="68df3-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68df3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68df3-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68df3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68df3-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68df3-155">INPUTS</span></span>

### <span data-ttu-id="68df3-156">System.String</span><span class="sxs-lookup"><span data-stu-id="68df3-156">System.String</span></span>

### <span data-ttu-id="68df3-157">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="68df3-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="68df3-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="68df3-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="68df3-159">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="68df3-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="68df3-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68df3-160">OUTPUTS</span></span>

### <span data-ttu-id="68df3-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="68df3-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="68df3-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68df3-162">NOTES</span></span>

<span data-ttu-id="68df3-163">Opublikowano nowy model cen.</span><span class="sxs-lookup"><span data-stu-id="68df3-163">A new pricing model has been released.</span></span> <span data-ttu-id="68df3-164">Jeśli jesteś programem CSP, oznacza to, że musisz używać "autonomicznej" jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="68df3-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="68df3-165">W tle wersja SKU zostanie zmieniona na pergb2018.</span><span class="sxs-lookup"><span data-stu-id="68df3-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="68df3-166">Aby uzyskać więcej informacji, zobacz następujące informacje: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="68df3-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="68df3-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68df3-167">RELATED LINKS</span></span>

[<span data-ttu-id="68df3-168">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="68df3-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



