---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221907"
---
# <span data-ttu-id="25b31-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="25b31-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="25b31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25b31-102">SYNOPSIS</span></span>
<span data-ttu-id="25b31-103">Aktualizuje informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="25b31-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="25b31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25b31-104">SYNTAX</span></span>

### <span data-ttu-id="25b31-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="25b31-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25b31-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="25b31-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b31-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25b31-107">DESCRIPTION</span></span>
<span data-ttu-id="25b31-108">Polecenie cmdlet **Set-AzOperationalInsightsStorageInsight** umożliwia zmianę konfiguracji gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="25b31-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="25b31-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25b31-109">EXAMPLES</span></span>

### <span data-ttu-id="25b31-110">Przykład 1: modyfikowanie miejsca do magazynowania po nazwie</span><span class="sxs-lookup"><span data-stu-id="25b31-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="25b31-111">To polecenie modyfikuje tabele, z których dane składowe o nazwie MyStorageInsight odczytuje.</span><span class="sxs-lookup"><span data-stu-id="25b31-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="25b31-112">Przykład 2: modyfikowanie informacji o przestrzeni dyskowej przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="25b31-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="25b31-113">Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="25b31-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="25b31-114">Drugie polecenie modyfikuje kontenery, na podstawie których miejsce do magazynowania o nazwie MyStorageInsight odczytuje.</span><span class="sxs-lookup"><span data-stu-id="25b31-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="25b31-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25b31-115">PARAMETERS</span></span>

### <span data-ttu-id="25b31-116">-Kontenery</span><span class="sxs-lookup"><span data-stu-id="25b31-116">-Containers</span></span>
<span data-ttu-id="25b31-117">Określa listę kontenerów, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="25b31-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="25b31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b31-118">-DefaultProfile</span></span>
<span data-ttu-id="25b31-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25b31-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25b31-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25b31-120">-Name</span></span>
<span data-ttu-id="25b31-121">Określa nazwę gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="25b31-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="25b31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b31-122">-ResourceGroupName</span></span>
<span data-ttu-id="25b31-123">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="25b31-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="25b31-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="25b31-124">-StorageAccountKey</span></span>
<span data-ttu-id="25b31-125">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="25b31-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="25b31-126">-Tabele</span><span class="sxs-lookup"><span data-stu-id="25b31-126">-Tables</span></span>
<span data-ttu-id="25b31-127">Określa listę tabel zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="25b31-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="25b31-128">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="25b31-128">-Workspace</span></span>
<span data-ttu-id="25b31-129">Określa obszar roboczy zawierający szczegółowe dane dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="25b31-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="25b31-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="25b31-130">-WorkspaceName</span></span>
<span data-ttu-id="25b31-131">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="25b31-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="25b31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b31-132">CommonParameters</span></span>
<span data-ttu-id="25b31-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b31-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b31-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b31-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25b31-135">INPUTS</span></span>

### <span data-ttu-id="25b31-136">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25b31-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="25b31-137">System. String</span><span class="sxs-lookup"><span data-stu-id="25b31-137">System.String</span></span>

### <span data-ttu-id="25b31-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="25b31-138">System.String[]</span></span>

## <span data-ttu-id="25b31-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25b31-139">OUTPUTS</span></span>

### <span data-ttu-id="25b31-140">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="25b31-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="25b31-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25b31-141">NOTES</span></span>

## <span data-ttu-id="25b31-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25b31-142">RELATED LINKS</span></span>

[<span data-ttu-id="25b31-143">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="25b31-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="25b31-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="25b31-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


