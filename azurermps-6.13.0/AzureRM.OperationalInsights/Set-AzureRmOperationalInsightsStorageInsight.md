---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 460a1585c8c6c556f0044b9cd0673a3be750ffe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716932"
---
# <span data-ttu-id="cd3b6-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="cd3b6-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="cd3b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd3b6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3b6-103">Aktualizuje informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd3b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd3b6-104">SYNTAX</span></span>

### <span data-ttu-id="cd3b6-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd3b6-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd3b6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cd3b6-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3b6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd3b6-107">DESCRIPTION</span></span>
<span data-ttu-id="cd3b6-108">Polecenie cmdlet **Set-AzureRmOperationalInsightsStorageInsight** umożliwia zmianę konfiguracji gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="cd3b6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd3b6-109">EXAMPLES</span></span>

### <span data-ttu-id="cd3b6-110">Przykład 1: modyfikowanie miejsca do magazynowania po nazwie</span><span class="sxs-lookup"><span data-stu-id="cd3b6-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="cd3b6-111">To polecenie modyfikuje tabele, z których dane składowe o nazwie MyStorageInsight odczytuje.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="cd3b6-112">Przykład 2: modyfikowanie informacji o przestrzeni dyskowej przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cd3b6-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="cd3b6-113">Pierwsze polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie Moja przestrzeń robocza, a następnie przechowywać go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="cd3b6-114">Drugie polecenie modyfikuje kontenery, na podstawie których miejsce do magazynowania o nazwie MyStorageInsight odczytuje.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="cd3b6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd3b6-115">PARAMETERS</span></span>

### <span data-ttu-id="cd3b6-116">-Kontenery</span><span class="sxs-lookup"><span data-stu-id="cd3b6-116">-Containers</span></span>
<span data-ttu-id="cd3b6-117">Określa listę kontenerów, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="cd3b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3b6-118">-DefaultProfile</span></span>
<span data-ttu-id="cd3b6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd3b6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd3b6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd3b6-120">-Name</span></span>
<span data-ttu-id="cd3b6-121">Określa nazwę gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="cd3b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd3b6-123">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="cd3b6-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cd3b6-124">-StorageAccountKey</span></span>
<span data-ttu-id="cd3b6-125">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="cd3b6-126">-Tabele</span><span class="sxs-lookup"><span data-stu-id="cd3b6-126">-Tables</span></span>
<span data-ttu-id="cd3b6-127">Określa listę tabel zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="cd3b6-128">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cd3b6-128">-Workspace</span></span>
<span data-ttu-id="cd3b6-129">Określa obszar roboczy zawierający szczegółowe dane dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="cd3b6-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cd3b6-130">-WorkspaceName</span></span>
<span data-ttu-id="cd3b6-131">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="cd3b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3b6-132">CommonParameters</span></span>
<span data-ttu-id="cd3b6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3b6-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3b6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd3b6-135">INPUTS</span></span>

### <span data-ttu-id="cd3b6-136">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd3b6-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="cd3b6-137">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd3b6-137">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="cd3b6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3b6-138">System.String</span></span>

### <span data-ttu-id="cd3b6-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="cd3b6-139">System.String[]</span></span>

## <span data-ttu-id="cd3b6-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd3b6-140">OUTPUTS</span></span>

### <span data-ttu-id="cd3b6-141">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="cd3b6-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="cd3b6-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd3b6-142">NOTES</span></span>

## <span data-ttu-id="cd3b6-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd3b6-143">RELATED LINKS</span></span>

[<span data-ttu-id="cd3b6-144">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="cd3b6-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="cd3b6-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd3b6-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


