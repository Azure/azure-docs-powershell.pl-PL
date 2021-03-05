---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: c2a622b110bdc17fe325934b50c59ac7e9b8f3ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989647"
---
# <span data-ttu-id="cba6e-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="cba6e-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="cba6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba6e-102">SYNOPSIS</span></span>
<span data-ttu-id="cba6e-103">Aktualizuje szczegółowe informacje o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="cba6e-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="cba6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cba6e-104">SYNTAX</span></span>

### <span data-ttu-id="cba6e-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cba6e-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cba6e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cba6e-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba6e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cba6e-107">DESCRIPTION</span></span>
<span data-ttu-id="cba6e-108">Polecenie **cmdlet Set-AzOperationalInsightsStorageInsight** zmienia konfigurację szczegółowych informacji o magazynie.</span><span class="sxs-lookup"><span data-stu-id="cba6e-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="cba6e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cba6e-109">EXAMPLES</span></span>

### <span data-ttu-id="cba6e-110">Przykład 1. Modyfikowanie informacji o magazynie według nazwy</span><span class="sxs-lookup"><span data-stu-id="cba6e-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="cba6e-111">To polecenie modyfikuje tabele, z których odczytuje szczegółowe informacje o magazynie o nazwie MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="cba6e-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="cba6e-112">Przykład 2. Modyfikowanie szczegółowych informacji o magazynie przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cba6e-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="cba6e-113">Pierwsze polecenie używa Get-AzOperationalInsightsWorkspace cmdlet w celu uzyskania obszaru roboczego o nazwie MyWorkspace, a następnie zapisuje go w $Workspace danych.</span><span class="sxs-lookup"><span data-stu-id="cba6e-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="cba6e-114">Drugie polecenie modyfikuje kontenery, z których odczytuje szczegółowe informacje o magazynie o nazwie MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="cba6e-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="cba6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cba6e-115">PARAMETERS</span></span>

### <span data-ttu-id="cba6e-116">— Containers</span><span class="sxs-lookup"><span data-stu-id="cba6e-116">-Containers</span></span>
<span data-ttu-id="cba6e-117">Określa listę kontenerów, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="cba6e-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="cba6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba6e-118">-DefaultProfile</span></span>
<span data-ttu-id="cba6e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cba6e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cba6e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cba6e-120">-Name</span></span>
<span data-ttu-id="cba6e-121">Określa nazwę szczegółowych informacji o magazynie.</span><span class="sxs-lookup"><span data-stu-id="cba6e-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="cba6e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba6e-122">-ResourceGroupName</span></span>
<span data-ttu-id="cba6e-123">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="cba6e-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="cba6e-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cba6e-124">-StorageAccountKey</span></span>
<span data-ttu-id="cba6e-125">Określa klucz dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="cba6e-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="cba6e-126">— Tabele</span><span class="sxs-lookup"><span data-stu-id="cba6e-126">-Tables</span></span>
<span data-ttu-id="cba6e-127">Określa listę tabel zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="cba6e-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="cba6e-128">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cba6e-128">-Workspace</span></span>
<span data-ttu-id="cba6e-129">Określa obszar roboczy zawierający szczegółowe informacje o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="cba6e-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="cba6e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cba6e-130">-WorkspaceName</span></span>
<span data-ttu-id="cba6e-131">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="cba6e-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="cba6e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba6e-132">CommonParameters</span></span>
<span data-ttu-id="cba6e-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba6e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba6e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba6e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba6e-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cba6e-135">INPUTS</span></span>

### <span data-ttu-id="cba6e-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cba6e-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cba6e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cba6e-137">System.String</span></span>

### <span data-ttu-id="cba6e-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cba6e-138">System.String[]</span></span>

## <span data-ttu-id="cba6e-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cba6e-139">OUTPUTS</span></span>

### <span data-ttu-id="cba6e-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="cba6e-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="cba6e-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cba6e-141">NOTES</span></span>

## <span data-ttu-id="cba6e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cba6e-142">RELATED LINKS</span></span>

[<span data-ttu-id="cba6e-143">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="cba6e-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="cba6e-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="cba6e-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


