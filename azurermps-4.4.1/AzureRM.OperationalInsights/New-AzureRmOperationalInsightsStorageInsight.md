---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 2f27a2aef23e008294a932d57538d0acec0d249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546143"
---
# <span data-ttu-id="e8a6d-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e8a6d-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="e8a6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a6d-103">Tworzy miejsce do magazynowania w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8a6d-104">SYNTAX</span></span>

### <span data-ttu-id="e8a6d-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8a6d-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8a6d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e8a6d-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8a6d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8a6d-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a6d-108">Polecenie cmdlet **New-AzureRmOperationalInsightsStorageInsight** tworzy nowe miejsce do magazynowania w istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="e8a6d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8a6d-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a6d-110">Przykład 1. Tworzenie miejsca do magazynowania po nazwie</span><span class="sxs-lookup"><span data-stu-id="e8a6d-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="e8a6d-111">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmStorageAccount, aby uzyskać konto magazynu o nazwie ContosoStorage, a następnie przechowywać je w zmiennej $Storage.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="e8a6d-112">Drugie polecenie przekazuje konto magazynu w $Storage polecenia cmdlet Get-AzureRmStorageAccountKey za pomocą operatora potoku w celu uzyskania określonego klucza konta magazynu, a następnie zapisuje go w zmiennej $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="e8a6d-113">Ostatnie polecenie tworzy miejsce do magazynowania o nazwie MyStorageInsight w obszarze roboczym o nazwie Mój obszar.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="e8a6d-114">Ta usługa gromadzenia danych wykorzystuje dane z tabeli WADWindowsEventLogsTable w określonym zasobie kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="e8a6d-115">Przykład 2: tworzenie szczegółowego miejsca do magazynowania przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="e8a6d-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="e8a6d-116">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="e8a6d-117">Drugie polecenie używa polecenia cmdlet Get-AzureRmStorageAccount w celu uzyskania określonego konta magazynu, a następnie zapisuje je w zmiennej $Storage.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="e8a6d-118">Trzecie polecenie przekazuje konto magazynu w $Storage polecenia cmdlet Get-AzureRmStorageAccountKey za pomocą operatora potoku w celu uzyskania określonego klucza, a następnie zapisanie go w zmiennej $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="e8a6d-119">Ostatnie polecenie tworzy miejsce do magazynowania o nazwie MyStorageInsight w obszarze roboczym zdefiniowanym w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="e8a6d-120">Usługa gromadzenia danych pobiera dane z tabeli WADWindowsEventLogsTable w określonym zasobie kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="e8a6d-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8a6d-121">PARAMETERS</span></span>

### <span data-ttu-id="e8a6d-122">-Kontenery</span><span class="sxs-lookup"><span data-stu-id="e8a6d-122">-Containers</span></span>
<span data-ttu-id="e8a6d-123">Określa listę kontenerów zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="e8a6d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e8a6d-124">-Force</span></span>
<span data-ttu-id="e8a6d-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e8a6d-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8a6d-126">-Name</span></span>
<span data-ttu-id="e8a6d-127">Określa nazwę szczegółowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-127">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="e8a6d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a6d-128">-ResourceGroupName</span></span>
<span data-ttu-id="e8a6d-129">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-129">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e8a6d-130">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e8a6d-130">-StorageAccountKey</span></span>
<span data-ttu-id="e8a6d-131">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-131">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="e8a6d-132">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e8a6d-132">-StorageAccountResourceId</span></span>
<span data-ttu-id="e8a6d-133">Określa zasób platformy Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-133">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="e8a6d-134">Można go pobrać, wykonując polecenie cmdlet Get-AzureRmStorageAccount i uzyskując dostęp do parametru *ID* wyniku.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-134">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="e8a6d-135">-Tabele</span><span class="sxs-lookup"><span data-stu-id="e8a6d-135">-Tables</span></span>
<span data-ttu-id="e8a6d-136">Określa listę tabel, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-136">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="e8a6d-137">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="e8a6d-137">-Workspace</span></span>
<span data-ttu-id="e8a6d-138">Określa obszar roboczy nowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-138">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="e8a6d-139">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e8a6d-139">-WorkspaceName</span></span>
<span data-ttu-id="e8a6d-140">Określa nazwę istniejącego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-140">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="e8a6d-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8a6d-141">-Confirm</span></span>
<span data-ttu-id="e8a6d-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8a6d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a6d-143">-WhatIf</span></span>
<span data-ttu-id="e8a6d-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8a6d-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8a6d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a6d-146">-DefaultProfile</span></span>
<span data-ttu-id="e8a6d-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a6d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a6d-148">CommonParameters</span></span>
<span data-ttu-id="e8a6d-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a6d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a6d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8a6d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a6d-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8a6d-151">INPUTS</span></span>

### <span data-ttu-id="e8a6d-152">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8a6d-152">PSWorkspace</span></span>
<span data-ttu-id="e8a6d-153">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="e8a6d-153">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e8a6d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8a6d-154">OUTPUTS</span></span>

### <span data-ttu-id="e8a6d-155">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e8a6d-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="e8a6d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8a6d-156">NOTES</span></span>

## <span data-ttu-id="e8a6d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8a6d-157">RELATED LINKS</span></span>

[<span data-ttu-id="e8a6d-158">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="e8a6d-158">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="e8a6d-159">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8a6d-159">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


