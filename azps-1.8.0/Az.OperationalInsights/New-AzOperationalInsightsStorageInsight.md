---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: e4f966d542110f96672857c2222d44ae03d331ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93897097"
---
# <span data-ttu-id="3a0bb-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="3a0bb-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="3a0bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a0bb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a0bb-103">Tworzy miejsce do magazynowania w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="3a0bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a0bb-104">SYNTAX</span></span>

### <span data-ttu-id="3a0bb-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a0bb-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a0bb-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a0bb-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a0bb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3a0bb-107">DESCRIPTION</span></span>
<span data-ttu-id="3a0bb-108">Polecenie cmdlet **New-AzOperationalInsightsStorageInsight** tworzy nowe miejsce do magazynowania w istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="3a0bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a0bb-109">EXAMPLES</span></span>

### <span data-ttu-id="3a0bb-110">Przykład 1. Tworzenie miejsca do magazynowania po nazwie</span><span class="sxs-lookup"><span data-stu-id="3a0bb-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="3a0bb-111">Pierwsze polecenie używa polecenia cmdlet Get-AzStorageAccount, aby uzyskać konto magazynu o nazwie ContosoStorage, a następnie przechowywać je w zmiennej $Storage.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="3a0bb-112">Drugie polecenie przekazuje konto magazynu w $Storage polecenia cmdlet Get-AzStorageAccountKey za pomocą operatora potoku w celu uzyskania określonego klucza konta magazynu, a następnie zapisuje go w zmiennej $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="3a0bb-113">Ostatnie polecenie tworzy miejsce do magazynowania o nazwie MyStorageInsight w obszarze roboczym o nazwie Mój obszar.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="3a0bb-114">Ta usługa gromadzenia danych wykorzystuje dane z tabeli WADWindowsEventLogsTable w określonym zasobie kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="3a0bb-115">Przykład 2: tworzenie szczegółowego miejsca do magazynowania przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="3a0bb-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="3a0bb-116">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-116">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="3a0bb-117">Drugie polecenie używa polecenia cmdlet Get-AzStorageAccount w celu uzyskania określonego konta magazynu, a następnie zapisuje je w zmiennej $Storage.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-117">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="3a0bb-118">Trzecie polecenie przekazuje konto magazynu w $Storage polecenia cmdlet Get-AzStorageAccountKey za pomocą operatora potoku w celu uzyskania określonego klucza, a następnie zapisanie go w zmiennej $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-118">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="3a0bb-119">Ostatnie polecenie tworzy miejsce do magazynowania o nazwie MyStorageInsight w obszarze roboczym zdefiniowanym w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="3a0bb-120">Usługa gromadzenia danych pobiera dane z tabeli WADWindowsEventLogsTable w określonym zasobie kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="3a0bb-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a0bb-121">PARAMETERS</span></span>

### <span data-ttu-id="3a0bb-122">-Kontenery</span><span class="sxs-lookup"><span data-stu-id="3a0bb-122">-Containers</span></span>
<span data-ttu-id="3a0bb-123">Określa listę kontenerów zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="3a0bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a0bb-124">-DefaultProfile</span></span>
<span data-ttu-id="3a0bb-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3a0bb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a0bb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3a0bb-126">-Force</span></span>
<span data-ttu-id="3a0bb-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a0bb-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a0bb-128">-Name</span></span>
<span data-ttu-id="3a0bb-129">Określa nazwę szczegółowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="3a0bb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a0bb-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a0bb-131">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3a0bb-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3a0bb-132">-StorageAccountKey</span></span>
<span data-ttu-id="3a0bb-133">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3a0bb-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3a0bb-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="3a0bb-135">Określa zasób platformy Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="3a0bb-136">Można go pobrać, wykonując polecenie cmdlet Get-AzStorageAccount i uzyskując dostęp do parametru *ID* wyniku.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-136">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="3a0bb-137">-Tabele</span><span class="sxs-lookup"><span data-stu-id="3a0bb-137">-Tables</span></span>
<span data-ttu-id="3a0bb-138">Określa listę tabel, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="3a0bb-139">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="3a0bb-139">-Workspace</span></span>
<span data-ttu-id="3a0bb-140">Określa obszar roboczy nowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="3a0bb-141">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3a0bb-141">-WorkspaceName</span></span>
<span data-ttu-id="3a0bb-142">Określa nazwę istniejącego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="3a0bb-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a0bb-143">-Confirm</span></span>
<span data-ttu-id="3a0bb-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a0bb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a0bb-145">-WhatIf</span></span>
<span data-ttu-id="3a0bb-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a0bb-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a0bb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a0bb-148">CommonParameters</span></span>
<span data-ttu-id="3a0bb-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a0bb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a0bb-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a0bb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a0bb-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a0bb-151">INPUTS</span></span>

### <span data-ttu-id="3a0bb-152">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a0bb-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3a0bb-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3a0bb-153">System.String</span></span>

### <span data-ttu-id="3a0bb-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="3a0bb-154">System.String[]</span></span>

## <span data-ttu-id="3a0bb-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a0bb-155">OUTPUTS</span></span>

### <span data-ttu-id="3a0bb-156">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="3a0bb-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="3a0bb-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a0bb-157">NOTES</span></span>

## <span data-ttu-id="3a0bb-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a0bb-158">RELATED LINKS</span></span>

[<span data-ttu-id="3a0bb-159">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="3a0bb-159">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="3a0bb-160">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a0bb-160">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


