---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8df5d54576b62caf93a92583eb6dcc9e39802f3d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93897185"
---
# <span data-ttu-id="00b10-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="00b10-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="00b10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00b10-102">SYNOPSIS</span></span>
<span data-ttu-id="00b10-103">Umożliwia utworzenie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="00b10-103">Creates a workspace.</span></span>

## <span data-ttu-id="00b10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00b10-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00b10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00b10-105">DESCRIPTION</span></span>
<span data-ttu-id="00b10-106">Polecenie cmdlet **New-AzOperationalInsightsWorkspace** umożliwia utworzenie obszaru roboczego w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="00b10-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="00b10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00b10-107">EXAMPLES</span></span>

### <span data-ttu-id="00b10-108">Przykład 1. Tworzenie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="00b10-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="00b10-109">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="00b10-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="00b10-110">Przykład 2: Tworzenie obszaru roboczego i łączenie go z istniejącym kontem</span><span class="sxs-lookup"><span data-stu-id="00b10-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="00b10-111">W pierwszym poleceniu użyto polecenia cmdlet Get-AzOperationalInsightsLinkTargets, aby uzyskać wartości docelowe linku do konta usługi Insights, a następnie przechowywać je w zmiennej $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="00b10-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="00b10-112">Drugie polecenie przekazuje pierwszemu elementowi docelowe łącze konta w $OILinkTargets do polecenia cmdlet **New-AzOperationalInsightsWorkspace** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="00b10-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="00b10-113">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Mój obszar roboczy, która jest połączona z pierwszym kontem usługi Insights w programie $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="00b10-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="00b10-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00b10-114">PARAMETERS</span></span>

### <span data-ttu-id="00b10-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="00b10-115">-CustomerId</span></span>
<span data-ttu-id="00b10-116">Określa konto, z którym dany obszar roboczy będzie połączony.</span><span class="sxs-lookup"><span data-stu-id="00b10-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="00b10-117">Możesz również użyć polecenia cmdlet Get-AzOperationalInsightsLinkTargets, aby wyświetlić listę potencjalnych kont.</span><span class="sxs-lookup"><span data-stu-id="00b10-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b10-118">-DefaultProfile</span></span>
<span data-ttu-id="00b10-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="00b10-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00b10-120">-Force</span><span class="sxs-lookup"><span data-stu-id="00b10-120">-Force</span></span>
<span data-ttu-id="00b10-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00b10-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00b10-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="00b10-122">-Location</span></span>
<span data-ttu-id="00b10-123">Określa lokalizację, w której ma zostać utworzony obszar roboczy, na przykład Wschodnie USA lub Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="00b10-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="00b10-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00b10-124">-Name</span></span>
<span data-ttu-id="00b10-125">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="00b10-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="00b10-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b10-126">-ResourceGroupName</span></span>
<span data-ttu-id="00b10-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00b10-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="00b10-128">Obszar roboczy zostanie utworzony w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="00b10-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="00b10-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="00b10-129">-RetentionInDays</span></span>
<span data-ttu-id="00b10-130">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="00b10-130">The workspace data retention in days.</span></span> <span data-ttu-id="00b10-131">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="00b10-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="00b10-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="00b10-132">-Sku</span></span>
<span data-ttu-id="00b10-133">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="00b10-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="00b10-134">Aby uzyskać więcej informacji na temat wartości, którą należy użyć, sprawdź https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="00b10-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="00b10-135">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="00b10-135">Valid values are:</span></span>
- <span data-ttu-id="00b10-136">niezależnych</span><span class="sxs-lookup"><span data-stu-id="00b10-136">free</span></span>
- <span data-ttu-id="00b10-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="00b10-137">pergb2018</span></span>
- <span data-ttu-id="00b10-138">pernode</span><span class="sxs-lookup"><span data-stu-id="00b10-138">pernode</span></span>
- <span data-ttu-id="00b10-139">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="00b10-139">premium</span></span>
- <span data-ttu-id="00b10-140">oddzielnie</span><span class="sxs-lookup"><span data-stu-id="00b10-140">standalone</span></span>
- <span data-ttu-id="00b10-141">Standard</span><span class="sxs-lookup"><span data-stu-id="00b10-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b10-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="00b10-142">-Tag</span></span>
<span data-ttu-id="00b10-143">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="00b10-143">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="00b10-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00b10-144">-Confirm</span></span>
<span data-ttu-id="00b10-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b10-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b10-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b10-146">-WhatIf</span></span>
<span data-ttu-id="00b10-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b10-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00b10-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="00b10-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b10-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b10-149">CommonParameters</span></span>
<span data-ttu-id="00b10-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b10-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b10-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b10-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b10-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00b10-152">INPUTS</span></span>

### <span data-ttu-id="00b10-153">System. String</span><span class="sxs-lookup"><span data-stu-id="00b10-153">System.String</span></span>

### <span data-ttu-id="00b10-154">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00b10-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="00b10-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="00b10-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="00b10-156">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00b10-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="00b10-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00b10-157">OUTPUTS</span></span>

### <span data-ttu-id="00b10-158">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="00b10-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="00b10-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00b10-159">NOTES</span></span>

<span data-ttu-id="00b10-160">Nowy model cenowy został zwolniony.</span><span class="sxs-lookup"><span data-stu-id="00b10-160">A new pricing model has been released.</span></span> <span data-ttu-id="00b10-161">Jeśli jesteś dostawcą CSP, co oznacza, że musisz użyć "autonomicznej" dla jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="00b10-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="00b10-162">W tle jednostka SKU zostanie zmieniona na pergb2018.</span><span class="sxs-lookup"><span data-stu-id="00b10-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="00b10-163">Aby uzyskać więcej informacji, zobacz następujące tematy: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="00b10-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="00b10-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00b10-164">RELATED LINKS</span></span>

[<span data-ttu-id="00b10-165">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="00b10-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
