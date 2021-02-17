---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240395"
---
# <span data-ttu-id="8b283-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b283-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="8b283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b283-102">SYNOPSIS</span></span>
<span data-ttu-id="8b283-103">Aktualizuje obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="8b283-103">Updates a workspace.</span></span>

## <span data-ttu-id="8b283-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b283-104">SYNTAX</span></span>

### <span data-ttu-id="8b283-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="8b283-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="8b283-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8b283-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="8b283-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b283-107">DESCRIPTION</span></span>
<span data-ttu-id="8b283-108">Polecenie **cmdlet Set-AzOperationalInsightsWorkspace** zmienia konfigurację obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b283-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="8b283-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b283-109">EXAMPLES</span></span>

### <span data-ttu-id="8b283-110">Przykład 1. Modyfikowanie obszaru roboczego według nazwy</span><span class="sxs-lookup"><span data-stu-id="8b283-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="8b283-111">To polecenie modyfikuje sku i tagi obszaru roboczego o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8b283-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8b283-112">Przykład 2. Aktualizowanie obszaru roboczego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="8b283-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="8b283-113">To polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace w celu uzyskania obszaru roboczego o nazwie MyWorkSpace, Get-AzOperationalInsightsWorkspace następnie przekazuje go do polecenia cmdlet **Set-AzOperationalInsightsWorkspace** przy użyciu operatora potoku w celu ustawienia wersji Premium tej wersji.</span><span class="sxs-lookup"><span data-stu-id="8b283-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="8b283-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b283-114">PARAMETERS</span></span>

### <span data-ttu-id="8b283-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b283-115">-DefaultProfile</span></span>
<span data-ttu-id="8b283-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8b283-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b283-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b283-117">-Name</span></span>
<span data-ttu-id="8b283-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b283-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="8b283-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="8b283-120">Typ dostępu sieciowego do uzyskiwania dostępu do obszaru roboczego ingestion.</span><span class="sxs-lookup"><span data-stu-id="8b283-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="8b283-121">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="8b283-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="8b283-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="8b283-123">Typ dostępu sieciowego do uzyskiwania dostępu do zapytania obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b283-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="8b283-124">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="8b283-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b283-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b283-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b283-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8b283-127">-RetentionInDays</span></span>
<span data-ttu-id="8b283-128">Przechowywanie danych obszaru roboczego w dniach.</span><span class="sxs-lookup"><span data-stu-id="8b283-128">The workspace data retention in days.</span></span> <span data-ttu-id="8b283-129">730 dni to maksimum dozwolone dla wszystkich pozostałych jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="8b283-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="8b283-130">- SKU</span><span class="sxs-lookup"><span data-stu-id="8b283-130">-Sku</span></span>
<span data-ttu-id="8b283-131">Określa warstwę usługi obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b283-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="8b283-132">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="8b283-132">Valid values are:</span></span> 
- <span data-ttu-id="8b283-133">bezpłatnie</span><span class="sxs-lookup"><span data-stu-id="8b283-133">free</span></span>
- <span data-ttu-id="8b283-134">standardowy</span><span class="sxs-lookup"><span data-stu-id="8b283-134">standard</span></span>
- <span data-ttu-id="8b283-135">premium</span><span class="sxs-lookup"><span data-stu-id="8b283-135">premium</span></span>
- <span data-ttu-id="8b283-136">pernode</span><span class="sxs-lookup"><span data-stu-id="8b283-136">pernode</span></span>
- <span data-ttu-id="8b283-137">autonomiczny</span><span class="sxs-lookup"><span data-stu-id="8b283-137">standalone</span></span>
- <span data-ttu-id="8b283-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="8b283-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="8b283-139">-Tag</span></span>
<span data-ttu-id="8b283-140">Tagi zasobów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b283-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-141">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="8b283-141">-Workspace</span></span>
<span data-ttu-id="8b283-142">Określa obszar roboczy do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8b283-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b283-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b283-143">CommonParameters</span></span>
<span data-ttu-id="8b283-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b283-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b283-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b283-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b283-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b283-146">INPUTS</span></span>

### <span data-ttu-id="8b283-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b283-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8b283-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8b283-148">System.String</span></span>

### <span data-ttu-id="8b283-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b283-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8b283-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b283-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8b283-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b283-151">OUTPUTS</span></span>

### <span data-ttu-id="8b283-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b283-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8b283-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b283-153">NOTES</span></span>

## <span data-ttu-id="8b283-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b283-154">RELATED LINKS</span></span>

[<span data-ttu-id="8b283-155">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="8b283-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="8b283-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b283-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


