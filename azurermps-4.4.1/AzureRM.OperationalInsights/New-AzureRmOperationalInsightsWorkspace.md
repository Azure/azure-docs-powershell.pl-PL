---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 83f9ec56f5d33b65810da96364ab11dd4eb7c52a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543112"
---
# <span data-ttu-id="95680-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="95680-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="95680-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95680-102">SYNOPSIS</span></span>
<span data-ttu-id="95680-103">Umożliwia utworzenie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="95680-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95680-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95680-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95680-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95680-105">DESCRIPTION</span></span>
<span data-ttu-id="95680-106">Polecenie cmdlet **New-AzureRmOperationalInsightsWorkspace** umożliwia utworzenie obszaru roboczego w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="95680-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="95680-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95680-107">EXAMPLES</span></span>

### <span data-ttu-id="95680-108">Przykład 1. Tworzenie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="95680-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="95680-109">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="95680-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="95680-110">Przykład 2: Tworzenie obszaru roboczego i łączenie go z istniejącym kontem</span><span class="sxs-lookup"><span data-stu-id="95680-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="95680-111">W pierwszym poleceniu użyto polecenia cmdlet Get-AzureRmOperationalInsightsLinkTargets, aby uzyskać wartości docelowe linku do konta usługi Insights, a następnie przechowywać je w zmiennej $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="95680-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="95680-112">Drugie polecenie przekazuje pierwszemu elementowi docelowe łącze konta w $OILinkTargets do polecenia cmdlet **New-AzureRmOperationalInsightsWorkspace** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="95680-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95680-113">To polecenie tworzy standardową przestrzeń roboczą SKU o nazwie Mój obszar roboczy, która jest połączona z pierwszym kontem usługi Insights w programie $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="95680-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="95680-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95680-114">PARAMETERS</span></span>

### <span data-ttu-id="95680-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="95680-115">-CustomerId</span></span>
<span data-ttu-id="95680-116">Określa konto, z którym dany obszar roboczy będzie połączony.</span><span class="sxs-lookup"><span data-stu-id="95680-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="95680-117">Możesz również użyć polecenia cmdlet Get-AzureRmOperationalInsightsLinkTargets, aby wyświetlić listę potencjalnych kont.</span><span class="sxs-lookup"><span data-stu-id="95680-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="95680-118">-Force</span><span class="sxs-lookup"><span data-stu-id="95680-118">-Force</span></span>
<span data-ttu-id="95680-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="95680-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95680-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="95680-120">-Location</span></span>
<span data-ttu-id="95680-121">Określa lokalizację, w której ma zostać utworzony obszar roboczy, na przykład Wschodnie USA lub Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="95680-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="95680-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95680-122">-Name</span></span>
<span data-ttu-id="95680-123">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="95680-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="95680-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95680-124">-ResourceGroupName</span></span>
<span data-ttu-id="95680-125">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95680-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="95680-126">Obszar roboczy zostanie utworzony w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="95680-126">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="95680-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="95680-127">-Sku</span></span>
<span data-ttu-id="95680-128">Określa poziom usług obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="95680-128">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="95680-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="95680-129">Valid values are:</span></span> 

- <span data-ttu-id="95680-130">niezależnych</span><span class="sxs-lookup"><span data-stu-id="95680-130">free</span></span>
- <span data-ttu-id="95680-131">Standard</span><span class="sxs-lookup"><span data-stu-id="95680-131">standard</span></span>
- <span data-ttu-id="95680-132">ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="95680-132">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95680-133">-Tagi</span><span class="sxs-lookup"><span data-stu-id="95680-133">-Tags</span></span>
<span data-ttu-id="95680-134">Określa znaczniki zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="95680-134">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="95680-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95680-135">-Confirm</span></span>
<span data-ttu-id="95680-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95680-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95680-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95680-137">-WhatIf</span></span>
<span data-ttu-id="95680-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95680-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95680-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95680-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95680-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95680-140">-DefaultProfile</span></span>
<span data-ttu-id="95680-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95680-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95680-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="95680-142">-RetentionInDays</span></span>
<span data-ttu-id="95680-143">Dane obszaru roboczego zachowywane w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="95680-143">The workspace data retention in days.</span></span> <span data-ttu-id="95680-144">730 dni to maksimum dozwolone dla wszystkich pozostałych wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="95680-144">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="95680-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95680-145">CommonParameters</span></span>
<span data-ttu-id="95680-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95680-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95680-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95680-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95680-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95680-148">INPUTS</span></span>

## <span data-ttu-id="95680-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95680-149">OUTPUTS</span></span>

### <span data-ttu-id="95680-150">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="95680-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="95680-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95680-151">NOTES</span></span>

## <span data-ttu-id="95680-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95680-152">RELATED LINKS</span></span>

[<span data-ttu-id="95680-153">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="95680-153">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="95680-154">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="95680-154">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


