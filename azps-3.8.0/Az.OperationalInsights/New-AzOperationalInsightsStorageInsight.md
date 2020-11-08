---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 7b1f3b097c45424f9c2c9fda8e516808b2f67d94
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061766"
---
# <span data-ttu-id="53890-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="53890-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="53890-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53890-102">SYNOPSIS</span></span>
<span data-ttu-id="53890-103">Tworzy miejsce do magazynowania w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="53890-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="53890-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53890-104">SYNTAX</span></span>

### <span data-ttu-id="53890-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53890-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53890-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53890-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53890-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53890-107">DESCRIPTION</span></span>
<span data-ttu-id="53890-108">Polecenie cmdlet **New-AzOperationalInsightsStorageInsight** tworzy nowe miejsce do magazynowania w istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="53890-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="53890-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53890-109">EXAMPLES</span></span>

### <span data-ttu-id="53890-110">Przykład 1. Tworzenie miejsca do magazynowania po nazwie</span><span class="sxs-lookup"><span data-stu-id="53890-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="53890-111">Pierwsze polecenie używa polecenia cmdlet Get-AzStorageAccount, aby uzyskać konto magazynu o nazwie ContosoStorage, a następnie przechowywać je w zmiennej $Storage.</span><span class="sxs-lookup"><span data-stu-id="53890-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="53890-112">Drugie polecenie przekazuje konto magazynu w $Storage polecenia cmdlet Get-AzStorageAccountKey za pomocą operatora potoku w celu uzyskania określonego klucza konta magazynu, a następnie zapisuje go w zmiennej $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="53890-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="53890-113">Ten przykład pobiera pierwszy klawisz.</span><span class="sxs-lookup"><span data-stu-id="53890-113">This example retrieves the first key.</span></span> <span data-ttu-id="53890-114">Aby pobrać inną, użyj wartości [1] zamiast wartości [0].</span><span class="sxs-lookup"><span data-stu-id="53890-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="53890-115">Ostatnie polecenie tworzy miejsce do magazynowania o nazwie MyStorageInsight w obszarze roboczym o nazwie Mój obszar.</span><span class="sxs-lookup"><span data-stu-id="53890-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="53890-116">Ta usługa gromadzenia danych wykorzystuje dane z tabeli WADWindowsEventLogsTable w określonym zasobie kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="53890-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="53890-117">Przykład 2: tworzenie szczegółowego miejsca do magazynowania przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="53890-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="53890-118">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="53890-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="53890-119">Drugie polecenie używa polecenia cmdlet Get-AzStorageAccount w celu uzyskania określonego konta magazynu, a następnie zapisuje je w zmiennej $Storage.</span><span class="sxs-lookup"><span data-stu-id="53890-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="53890-120">Trzecie polecenie przekazuje konto magazynu w $Storage polecenia cmdlet Get-AzStorageAccountKey za pomocą operatora potoku w celu uzyskania określonego klucza, a następnie zapisanie go w zmiennej $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="53890-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="53890-121">Ten przykład pobiera pierwszy klawisz.</span><span class="sxs-lookup"><span data-stu-id="53890-121">This example retrieves the first key.</span></span> <span data-ttu-id="53890-122">Aby pobrać inną, użyj wartości [1] zamiast wartości [0].</span><span class="sxs-lookup"><span data-stu-id="53890-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="53890-123">Ostatnie polecenie tworzy miejsce do magazynowania o nazwie MyStorageInsight w obszarze roboczym zdefiniowanym w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="53890-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="53890-124">Usługa gromadzenia danych pobiera dane z tabeli WADWindowsEventLogsTable w określonym zasobie kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="53890-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="53890-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53890-125">PARAMETERS</span></span>

### <span data-ttu-id="53890-126">-Kontenery</span><span class="sxs-lookup"><span data-stu-id="53890-126">-Containers</span></span>
<span data-ttu-id="53890-127">Określa listę kontenerów zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="53890-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="53890-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53890-128">-DefaultProfile</span></span>
<span data-ttu-id="53890-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="53890-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53890-130">-Force</span><span class="sxs-lookup"><span data-stu-id="53890-130">-Force</span></span>
<span data-ttu-id="53890-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="53890-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53890-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53890-132">-Name</span></span>
<span data-ttu-id="53890-133">Określa nazwę szczegółowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="53890-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="53890-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53890-134">-ResourceGroupName</span></span>
<span data-ttu-id="53890-135">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="53890-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="53890-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="53890-136">-StorageAccountKey</span></span>
<span data-ttu-id="53890-137">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="53890-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="53890-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="53890-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="53890-139">Określa zasób platformy Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="53890-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="53890-140">Można go pobrać, wykonując polecenie cmdlet Get-AzStorageAccount i uzyskując dostęp do parametru *ID* wyniku.</span><span class="sxs-lookup"><span data-stu-id="53890-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="53890-141">-Tabele</span><span class="sxs-lookup"><span data-stu-id="53890-141">-Tables</span></span>
<span data-ttu-id="53890-142">Określa listę tabel, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="53890-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="53890-143">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="53890-143">-Workspace</span></span>
<span data-ttu-id="53890-144">Określa obszar roboczy nowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="53890-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="53890-145">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="53890-145">-WorkspaceName</span></span>
<span data-ttu-id="53890-146">Określa nazwę istniejącego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="53890-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="53890-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53890-147">-Confirm</span></span>
<span data-ttu-id="53890-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53890-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53890-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53890-149">-WhatIf</span></span>
<span data-ttu-id="53890-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53890-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53890-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53890-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53890-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53890-152">CommonParameters</span></span>
<span data-ttu-id="53890-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53890-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53890-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53890-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53890-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53890-155">INPUTS</span></span>

### <span data-ttu-id="53890-156">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="53890-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="53890-157">System. String</span><span class="sxs-lookup"><span data-stu-id="53890-157">System.String</span></span>

### <span data-ttu-id="53890-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="53890-158">System.String[]</span></span>

## <span data-ttu-id="53890-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53890-159">OUTPUTS</span></span>

### <span data-ttu-id="53890-160">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="53890-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="53890-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53890-161">NOTES</span></span>

## <span data-ttu-id="53890-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53890-162">RELATED LINKS</span></span>

[<span data-ttu-id="53890-163">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="53890-163">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="53890-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="53890-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


