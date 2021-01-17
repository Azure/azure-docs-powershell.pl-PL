---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346174"
---
# <span data-ttu-id="d5a02-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d5a02-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="d5a02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5a02-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a02-103">Aktualizuje informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="d5a02-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="d5a02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5a02-104">SYNTAX</span></span>

### <span data-ttu-id="d5a02-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d5a02-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a02-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5a02-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a02-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d5a02-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a02-108">Polecenie cmdlet **Set-AzOperationalInsightsStorageInsight** umożliwia zmianę konfiguracji gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="d5a02-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="d5a02-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5a02-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a02-110">Przykład 1: modyfikowanie miejsca do magazynowania po nazwie</span><span class="sxs-lookup"><span data-stu-id="d5a02-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="d5a02-111">To polecenie modyfikuje tabele, z których dane składowe o nazwie MyStorageInsight odczytuje.</span><span class="sxs-lookup"><span data-stu-id="d5a02-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="d5a02-112">Przykład 2: modyfikowanie informacji o przestrzeni dyskowej przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="d5a02-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="d5a02-113">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="d5a02-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="d5a02-114">Drugie polecenie modyfikuje kontenery, na podstawie których miejsce do magazynowania o nazwie MyStorageInsight odczytuje.</span><span class="sxs-lookup"><span data-stu-id="d5a02-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="d5a02-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5a02-115">PARAMETERS</span></span>

### <span data-ttu-id="d5a02-116">-Kontenery</span><span class="sxs-lookup"><span data-stu-id="d5a02-116">-Containers</span></span>
<span data-ttu-id="d5a02-117">Określa listę kontenerów, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="d5a02-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="d5a02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a02-118">-DefaultProfile</span></span>
<span data-ttu-id="d5a02-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d5a02-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5a02-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5a02-120">-Name</span></span>
<span data-ttu-id="d5a02-121">Określa nazwę gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="d5a02-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="d5a02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a02-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5a02-123">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="d5a02-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d5a02-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d5a02-124">-StorageAccountKey</span></span>
<span data-ttu-id="d5a02-125">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5a02-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a02-126">-Tabele</span><span class="sxs-lookup"><span data-stu-id="d5a02-126">-Tables</span></span>
<span data-ttu-id="d5a02-127">Określa listę tabel zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="d5a02-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a02-128">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="d5a02-128">-Workspace</span></span>
<span data-ttu-id="d5a02-129">Określa obszar roboczy zawierający szczegółowe dane dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="d5a02-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="d5a02-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d5a02-130">-WorkspaceName</span></span>
<span data-ttu-id="d5a02-131">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d5a02-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="d5a02-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a02-132">CommonParameters</span></span>
<span data-ttu-id="d5a02-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a02-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a02-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a02-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a02-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5a02-135">INPUTS</span></span>

### <span data-ttu-id="d5a02-136">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5a02-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d5a02-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a02-137">System.String</span></span>

### <span data-ttu-id="d5a02-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="d5a02-138">System.String[]</span></span>

## <span data-ttu-id="d5a02-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5a02-139">OUTPUTS</span></span>

### <span data-ttu-id="d5a02-140">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d5a02-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="d5a02-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5a02-141">NOTES</span></span>

## <span data-ttu-id="d5a02-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5a02-142">RELATED LINKS</span></span>

[<span data-ttu-id="d5a02-143">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="d5a02-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="d5a02-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5a02-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


