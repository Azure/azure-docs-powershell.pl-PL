---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186722"
---
# <span data-ttu-id="f797f-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f797f-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f797f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f797f-102">SYNOPSIS</span></span>
<span data-ttu-id="f797f-103">Powoduje utworzenie obszaru roboczego lub przywrócenie obszaru roboczego "miękkiego usunięcia".</span><span class="sxs-lookup"><span data-stu-id="f797f-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="f797f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f797f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f797f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f797f-105">DESCRIPTION</span></span>
<span data-ttu-id="f797f-106">Polecenie **cmdlet New-AzOperationalInsightsWorkspace** tworzy obszar roboczy w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f797f-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="f797f-107">Lub przywróć programowo usunięty obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="f797f-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="f797f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f797f-108">EXAMPLES</span></span>

### <span data-ttu-id="f797f-109">Przykład 1. Tworzenie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="f797f-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="f797f-110">To polecenie tworzy standardowy obszar roboczy SKU o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f797f-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f797f-111">Przykład 2. Tworzenie obszaru roboczego i łączenie go z istniejącym kontem</span><span class="sxs-lookup"><span data-stu-id="f797f-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="f797f-112">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsLinkTargets w celu uzyskania celów docelowych linku do konta w szczegółowych informacjach operacyjnych, a następnie przechowuje je w $OILinkTargets danych.</span><span class="sxs-lookup"><span data-stu-id="f797f-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="f797f-113">Drugie polecenie przekazuje pierwszy element docelowy linku do konta w $OILinkTargets do polecenia cmdlet **New-AzOperationalInsightsWorkspace** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f797f-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f797f-114">Polecenie tworzy standardowy obszar roboczy SKU o nazwie MyWorkspace, który jest połączony z pierwszym kontem szczegółowych informacji operacyjnych w programie $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="f797f-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="f797f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f797f-115">PARAMETERS</span></span>

### <span data-ttu-id="f797f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f797f-116">-DefaultProfile</span></span>
<span data-ttu-id="f797f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f797f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f797f-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f797f-118">-Force</span></span>
<span data-ttu-id="f797f-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f797f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f797f-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f797f-120">-Location</span></span>
<span data-ttu-id="f797f-121">Określa lokalizację, w której ma być tworzyć obszar roboczy, na przykład Wschód Stany Zjednoczone lub Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="f797f-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="f797f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f797f-122">-Name</span></span>
<span data-ttu-id="f797f-123">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f797f-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="f797f-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="f797f-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="f797f-125">Typ dostępu sieciowego do uzyskiwania dostępu do obszaru roboczego ingestion.</span><span class="sxs-lookup"><span data-stu-id="f797f-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="f797f-126">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="f797f-126">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="f797f-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="f797f-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="f797f-128">Typ dostępu sieciowego do uzyskiwania dostępu do zapytania obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f797f-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="f797f-129">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="f797f-129">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="f797f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f797f-130">-ResourceGroupName</span></span>
<span data-ttu-id="f797f-131">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f797f-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f797f-132">Obszar roboczy zostanie utworzony w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f797f-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="f797f-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f797f-133">-RetentionInDays</span></span>
<span data-ttu-id="f797f-134">Przechowywanie danych obszaru roboczego w dniach.</span><span class="sxs-lookup"><span data-stu-id="f797f-134">The workspace data retention in days.</span></span> <span data-ttu-id="f797f-135">730 dni to maksimum dozwolone dla wszystkich pozostałych jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="f797f-135">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="f797f-136">- SKU</span><span class="sxs-lookup"><span data-stu-id="f797f-136">-Sku</span></span>
<span data-ttu-id="f797f-137">Określa warstwę usługi obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f797f-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="f797f-138">Aby uzyskać więcej informacji dotyczących wartości, której należy użyć, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers sprawdź.</span><span class="sxs-lookup"><span data-stu-id="f797f-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="f797f-139">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="f797f-139">Valid values are:</span></span>
- <span data-ttu-id="f797f-140">bezpłatnie</span><span class="sxs-lookup"><span data-stu-id="f797f-140">free</span></span>
- <span data-ttu-id="f797f-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="f797f-141">pergb2018</span></span>
- <span data-ttu-id="f797f-142">pernode</span><span class="sxs-lookup"><span data-stu-id="f797f-142">pernode</span></span>
- <span data-ttu-id="f797f-143">premium</span><span class="sxs-lookup"><span data-stu-id="f797f-143">premium</span></span>
- <span data-ttu-id="f797f-144">autonomiczny</span><span class="sxs-lookup"><span data-stu-id="f797f-144">standalone</span></span>
- <span data-ttu-id="f797f-145">standardowy</span><span class="sxs-lookup"><span data-stu-id="f797f-145">standard</span></span>

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

### <span data-ttu-id="f797f-146">— Tag</span><span class="sxs-lookup"><span data-stu-id="f797f-146">-Tag</span></span>
<span data-ttu-id="f797f-147">Tagi zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f797f-147">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="f797f-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f797f-148">-Confirm</span></span>
<span data-ttu-id="f797f-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f797f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f797f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f797f-150">-WhatIf</span></span>
<span data-ttu-id="f797f-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f797f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f797f-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f797f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f797f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f797f-153">CommonParameters</span></span>
<span data-ttu-id="f797f-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f797f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f797f-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f797f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f797f-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f797f-156">INPUTS</span></span>

### <span data-ttu-id="f797f-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f797f-157">System.String</span></span>

### <span data-ttu-id="f797f-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f797f-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f797f-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f797f-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f797f-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f797f-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f797f-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f797f-161">OUTPUTS</span></span>

### <span data-ttu-id="f797f-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f797f-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f797f-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f797f-163">NOTES</span></span>

<span data-ttu-id="f797f-164">Opublikowano nowy model cen.</span><span class="sxs-lookup"><span data-stu-id="f797f-164">A new pricing model has been released.</span></span> <span data-ttu-id="f797f-165">Jeśli jesteś programem CSP, oznacza to, że musisz używać "autonomicznej" jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="f797f-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="f797f-166">W tle wersja SKU zostanie zmieniona na pergb2018.</span><span class="sxs-lookup"><span data-stu-id="f797f-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="f797f-167">Aby uzyskać więcej informacji, zobacz następujące informacje: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="f797f-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="f797f-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f797f-168">RELATED LINKS</span></span>

[<span data-ttu-id="f797f-169">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="f797f-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="f797f-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="f797f-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


