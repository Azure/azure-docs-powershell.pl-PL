---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184098"
---
# <span data-ttu-id="a96e7-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a96e7-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="a96e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a96e7-103">Tworzy szczegółowe informacje o przestrzeni dyskowej wewnątrz obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a96e7-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="a96e7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a96e7-104">SYNTAX</span></span>

### <span data-ttu-id="a96e7-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a96e7-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a96e7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a96e7-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a96e7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a96e7-107">DESCRIPTION</span></span>
<span data-ttu-id="a96e7-108">Polecenie **cmdlet New-AzOperationalInsightsStorageInsight** tworzy nową analizę przestrzeni dyskowej w istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a96e7-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="a96e7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a96e7-109">EXAMPLES</span></span>

### <span data-ttu-id="a96e7-110">Przykład 1. Tworzenie szczegółowych informacji o przestrzeni dyskowej według nazwy</span><span class="sxs-lookup"><span data-stu-id="a96e7-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a96e7-111">Pierwsze polecenie używa Get-AzStorageAccount cmdlet w celu uzyskania konta magazynu o nazwie ContosoStorage, a następnie zapisuje je w $Storage danych.</span><span class="sxs-lookup"><span data-stu-id="a96e7-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="a96e7-112">Drugie polecenie przekazuje konto magazynu w programie $Storage do polecenia cmdlet Get-AzStorageAccountKey przy użyciu operatora potoku w celu uzyskania określonego klucza konta magazynu, $StorageKey następnie zapisuje je w zmiennej $StorageKey magazynu.</span><span class="sxs-lookup"><span data-stu-id="a96e7-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="a96e7-113">W tym przykładzie jest pobierany pierwszy klucz.</span><span class="sxs-lookup"><span data-stu-id="a96e7-113">This example retrieves the first key.</span></span> <span data-ttu-id="a96e7-114">Aby pobrać drugi z nich, użyj wartości[1] zamiast Wartość[0].</span><span class="sxs-lookup"><span data-stu-id="a96e7-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="a96e7-115">Końcowe polecenie tworzy szczegółowe informacje o przestrzeni dyskowej o nazwie MyStorageInsight w obszarze roboczym o nazwie MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a96e7-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="a96e7-116">Ta analiza miejsca do magazynowania pobiera dane z tabeli WADWindowsEventLogsTable w określonym zasobie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a96e7-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="a96e7-117">Przykład 2. Tworzenie szczegółowych informacji o magazynie przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a96e7-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a96e7-118">Pierwsze polecenie używa Get-AzOperationalInsightsWorkspace cmdlet w celu uzyskania obszaru roboczego o nazwie MyWorkspace, a następnie zapisuje go w $Workspace danych.</span><span class="sxs-lookup"><span data-stu-id="a96e7-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="a96e7-119">Drugie polecenie używa Get-AzStorageAccount cmdlet w celu uzyskania określonego konta magazynu, a następnie zapisuje je w $Storage magazynu.</span><span class="sxs-lookup"><span data-stu-id="a96e7-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="a96e7-120">Trzecie polecenie przekazuje konto magazynu w programie $Storage do polecenia cmdlet Get-AzStorageAccountKey przy użyciu operatora potoku w celu uzyskania określonego klucza, a następnie zapisuje je w $StorageKey danych.</span><span class="sxs-lookup"><span data-stu-id="a96e7-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="a96e7-121">W tym przykładzie jest pobierany pierwszy klucz.</span><span class="sxs-lookup"><span data-stu-id="a96e7-121">This example retrieves the first key.</span></span> <span data-ttu-id="a96e7-122">Aby pobrać drugi z nich, użyj wartości[1] zamiast Wartość[0].</span><span class="sxs-lookup"><span data-stu-id="a96e7-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="a96e7-123">Końcowe polecenie tworzy szczegółowe informacje o magazynie o nazwie MyStorageInsight w obszarze roboczym zdefiniowanym w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="a96e7-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="a96e7-124">Szczegółowe informacje o magazynie zużywają dane z tabeli WADWindowsEventLogsTable w określonym zasobie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a96e7-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="a96e7-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a96e7-125">PARAMETERS</span></span>

### <span data-ttu-id="a96e7-126">— Containers</span><span class="sxs-lookup"><span data-stu-id="a96e7-126">-Containers</span></span>
<span data-ttu-id="a96e7-127">Określa listę kontenerów zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="a96e7-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96e7-128">-DefaultProfile</span></span>
<span data-ttu-id="a96e7-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a96e7-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a96e7-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a96e7-130">-Force</span></span>
<span data-ttu-id="a96e7-131">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a96e7-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a96e7-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a96e7-132">-Name</span></span>
<span data-ttu-id="a96e7-133">Określa nazwę szczegółowych informacji o magazynie.</span><span class="sxs-lookup"><span data-stu-id="a96e7-133">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96e7-134">-ResourceGroupName</span></span>
<span data-ttu-id="a96e7-135">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="a96e7-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a96e7-136">-StorageAccountKey</span></span>
<span data-ttu-id="a96e7-137">Określa klucz dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a96e7-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a96e7-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="a96e7-139">Określa zasób Azure konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a96e7-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="a96e7-140">Można to pobrać, wykonując polecenie cmdlet Get-AzStorageAccount uzyskanie dostępu do *parametru Id* wyniku.</span><span class="sxs-lookup"><span data-stu-id="a96e7-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-141">— Tabele</span><span class="sxs-lookup"><span data-stu-id="a96e7-141">-Tables</span></span>
<span data-ttu-id="a96e7-142">Określa listę tabel, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="a96e7-142">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-143">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="a96e7-143">-Workspace</span></span>
<span data-ttu-id="a96e7-144">Określa obszar roboczy dla nowej szczegółowych informacji o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="a96e7-144">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a96e7-145">-WorkspaceName</span></span>
<span data-ttu-id="a96e7-146">Określa nazwę istniejącego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a96e7-146">Specifies the name of an existing workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e7-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a96e7-147">-Confirm</span></span>
<span data-ttu-id="a96e7-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a96e7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96e7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96e7-149">-WhatIf</span></span>
<span data-ttu-id="a96e7-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a96e7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96e7-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a96e7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96e7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96e7-152">CommonParameters</span></span>
<span data-ttu-id="a96e7-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96e7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96e7-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a96e7-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96e7-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a96e7-155">INPUTS</span></span>

### <span data-ttu-id="a96e7-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a96e7-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a96e7-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a96e7-157">System.String</span></span>

### <span data-ttu-id="a96e7-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a96e7-158">System.String[]</span></span>

## <span data-ttu-id="a96e7-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a96e7-159">OUTPUTS</span></span>

### <span data-ttu-id="a96e7-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a96e7-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="a96e7-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a96e7-161">NOTES</span></span>

## <span data-ttu-id="a96e7-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a96e7-162">RELATED LINKS</span></span>

[<span data-ttu-id="a96e7-163">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="a96e7-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="a96e7-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a96e7-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


