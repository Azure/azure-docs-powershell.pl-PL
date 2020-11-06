---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 0ba43a38763252275d7461f11cc4db574720ba5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548056"
---
# <span data-ttu-id="92026-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="92026-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="92026-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92026-102">SYNOPSIS</span></span>
<span data-ttu-id="92026-103">Umożliwia utworzenie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="92026-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92026-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92026-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92026-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92026-105">DESCRIPTION</span></span>
<span data-ttu-id="92026-106">Polecenie cmdlet **New-AzureRmOperationalInsightsWorkspace** umożliwia utworzenie obszaru roboczego w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="92026-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="92026-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92026-107">EXAMPLES</span></span>

### <span data-ttu-id="92026-108">Przykład 1. Tworzenie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="92026-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="92026-109">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="92026-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="92026-110">Przykład 2: Tworzenie obszaru roboczego i łączenie go z istniejącym kontem</span><span class="sxs-lookup"><span data-stu-id="92026-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="92026-111">W pierwszym poleceniu użyto polecenia cmdlet Get-AzureRmOperationalInsightsLinkTargets, aby uzyskać wartości docelowe linku do konta usługi Insights, a następnie przechowywać je w zmiennej $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="92026-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="92026-112">Drugie polecenie przekazuje pierwszemu elementowi docelowe łącze konta w $OILinkTargets do polecenia cmdlet **New-AzureRmOperationalInsightsWorkspace** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="92026-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92026-113">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Mój obszar roboczy, która jest połączona z pierwszym kontem usługi Insights w programie $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="92026-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="92026-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92026-114">PARAMETERS</span></span>

### <span data-ttu-id="92026-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="92026-115">-CustomerId</span></span>
<span data-ttu-id="92026-116">Określa konto, z którym dany obszar roboczy będzie połączony.</span><span class="sxs-lookup"><span data-stu-id="92026-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="92026-117">Możesz również użyć polecenia cmdlet Get-AzureRmOperationalInsightsLinkTargets, aby wyświetlić listę potencjalnych kont.</span><span class="sxs-lookup"><span data-stu-id="92026-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92026-118">-DefaultProfile</span></span>
<span data-ttu-id="92026-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92026-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92026-120">-Force</span><span class="sxs-lookup"><span data-stu-id="92026-120">-Force</span></span>
<span data-ttu-id="92026-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92026-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92026-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="92026-122">-Location</span></span>
<span data-ttu-id="92026-123">Określa lokalizację, w której ma zostać utworzony obszar roboczy, na przykład Wschodnie USA lub Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="92026-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92026-124">-Name</span></span>
<span data-ttu-id="92026-125">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="92026-125">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92026-126">-ResourceGroupName</span></span>
<span data-ttu-id="92026-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92026-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="92026-128">Obszar roboczy zostanie utworzony w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="92026-128">The workspace is created in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="92026-129">-RetentionInDays</span></span>
<span data-ttu-id="92026-130">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="92026-130">The workspace data retention in days.</span></span> <span data-ttu-id="92026-131">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU</span><span class="sxs-lookup"><span data-stu-id="92026-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="92026-132">-Sku</span></span>
<span data-ttu-id="92026-133">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="92026-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="92026-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="92026-134">Valid values are:</span></span> 

- <span data-ttu-id="92026-135">niezależnych</span><span class="sxs-lookup"><span data-stu-id="92026-135">free</span></span>
- <span data-ttu-id="92026-136">Standard</span><span class="sxs-lookup"><span data-stu-id="92026-136">standard</span></span>
- <span data-ttu-id="92026-137">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="92026-137">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="92026-138">-Tag</span></span>
<span data-ttu-id="92026-139">Znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="92026-139">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92026-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92026-140">-Confirm</span></span>
<span data-ttu-id="92026-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92026-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92026-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92026-142">-WhatIf</span></span>
<span data-ttu-id="92026-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92026-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92026-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92026-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92026-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92026-145">CommonParameters</span></span>
<span data-ttu-id="92026-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92026-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92026-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92026-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92026-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92026-148">INPUTS</span></span>

### <span data-ttu-id="92026-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="92026-149">None</span></span>
<span data-ttu-id="92026-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="92026-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92026-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92026-151">OUTPUTS</span></span>

### <span data-ttu-id="92026-152">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="92026-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="92026-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92026-153">NOTES</span></span>

## <span data-ttu-id="92026-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92026-154">RELATED LINKS</span></span>

[<span data-ttu-id="92026-155">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="92026-155">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="92026-156">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="92026-156">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


