---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222999"
---
# <span data-ttu-id="4218f-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4218f-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="4218f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4218f-102">SYNOPSIS</span></span>
<span data-ttu-id="4218f-103">Umożliwia utworzenie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4218f-103">Creates a workspace.</span></span>

## <span data-ttu-id="4218f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4218f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4218f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4218f-105">DESCRIPTION</span></span>
<span data-ttu-id="4218f-106">Polecenie cmdlet **New-AzOperationalInsightsWorkspace** umożliwia utworzenie obszaru roboczego w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4218f-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="4218f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4218f-107">EXAMPLES</span></span>

### <span data-ttu-id="4218f-108">Przykład 1. Tworzenie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="4218f-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="4218f-109">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4218f-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="4218f-110">Przykład 2: Tworzenie obszaru roboczego i łączenie go z istniejącym kontem</span><span class="sxs-lookup"><span data-stu-id="4218f-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="4218f-111">W pierwszym poleceniu użyto polecenia cmdlet Get-AzOperationalInsightsLinkTargets, aby uzyskać wartości docelowe linku do konta usługi Insights, a następnie przechowywać je w zmiennej $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="4218f-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="4218f-112">Drugie polecenie przekazuje pierwszemu elementowi docelowe łącze konta w $OILinkTargets do polecenia cmdlet **New-AzOperationalInsightsWorkspace** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4218f-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4218f-113">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Mój obszar roboczy, która jest połączona z pierwszym kontem usługi Insights w programie $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="4218f-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="4218f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4218f-114">PARAMETERS</span></span>

### <span data-ttu-id="4218f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4218f-115">-DefaultProfile</span></span>
<span data-ttu-id="4218f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4218f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4218f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4218f-117">-Force</span></span>
<span data-ttu-id="4218f-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4218f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4218f-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4218f-119">-Location</span></span>
<span data-ttu-id="4218f-120">Określa lokalizację, w której ma zostać utworzony obszar roboczy, na przykład Wschodnie USA lub Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="4218f-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="4218f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4218f-121">-Name</span></span>
<span data-ttu-id="4218f-122">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4218f-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="4218f-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="4218f-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="4218f-124">Typ dostępu do sieci umożliwiający dostęp do spożycia w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="4218f-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="4218f-125">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="4218f-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="4218f-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="4218f-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="4218f-127">Typ dostępu do sieci w celu uzyskania dostępu do zapytania dotyczącego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4218f-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="4218f-128">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="4218f-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="4218f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4218f-129">-ResourceGroupName</span></span>
<span data-ttu-id="4218f-130">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4218f-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4218f-131">Obszar roboczy zostanie utworzony w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4218f-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="4218f-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4218f-132">-RetentionInDays</span></span>
<span data-ttu-id="4218f-133">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="4218f-133">The workspace data retention in days.</span></span> <span data-ttu-id="4218f-134">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="4218f-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="4218f-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="4218f-135">-Sku</span></span>
<span data-ttu-id="4218f-136">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4218f-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="4218f-137">Aby uzyskać więcej informacji na temat wartości, którą należy użyć, sprawdź https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="4218f-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="4218f-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4218f-138">Valid values are:</span></span>
- <span data-ttu-id="4218f-139">niezależnych</span><span class="sxs-lookup"><span data-stu-id="4218f-139">free</span></span>
- <span data-ttu-id="4218f-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="4218f-140">pergb2018</span></span>
- <span data-ttu-id="4218f-141">pernode</span><span class="sxs-lookup"><span data-stu-id="4218f-141">pernode</span></span>
- <span data-ttu-id="4218f-142">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="4218f-142">premium</span></span>
- <span data-ttu-id="4218f-143">oddzielnie</span><span class="sxs-lookup"><span data-stu-id="4218f-143">standalone</span></span>
- <span data-ttu-id="4218f-144">Standard</span><span class="sxs-lookup"><span data-stu-id="4218f-144">standard</span></span>

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

### <span data-ttu-id="4218f-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="4218f-145">-Tag</span></span>
<span data-ttu-id="4218f-146">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4218f-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="4218f-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4218f-147">-Confirm</span></span>
<span data-ttu-id="4218f-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4218f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4218f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4218f-149">-WhatIf</span></span>
<span data-ttu-id="4218f-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4218f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4218f-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4218f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4218f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4218f-152">CommonParameters</span></span>
<span data-ttu-id="4218f-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4218f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4218f-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4218f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4218f-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4218f-155">INPUTS</span></span>

### <span data-ttu-id="4218f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4218f-156">System.String</span></span>

### <span data-ttu-id="4218f-157">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4218f-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4218f-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4218f-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4218f-159">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4218f-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4218f-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4218f-160">OUTPUTS</span></span>

### <span data-ttu-id="4218f-161">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4218f-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="4218f-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4218f-162">NOTES</span></span>

<span data-ttu-id="4218f-163">Nowy model cenowy został zwolniony.</span><span class="sxs-lookup"><span data-stu-id="4218f-163">A new pricing model has been released.</span></span> <span data-ttu-id="4218f-164">Jeśli jesteś dostawcą CSP, co oznacza, że musisz użyć "autonomicznej" dla jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="4218f-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="4218f-165">W tle jednostka SKU zostanie zmieniona na pergb2018.</span><span class="sxs-lookup"><span data-stu-id="4218f-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="4218f-166">Aby uzyskać więcej informacji, zobacz następujące tematy: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="4218f-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="4218f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4218f-167">RELATED LINKS</span></span>

[<span data-ttu-id="4218f-168">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="4218f-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="4218f-169">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="4218f-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


