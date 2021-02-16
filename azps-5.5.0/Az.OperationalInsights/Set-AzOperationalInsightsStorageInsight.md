---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186698"
---
# <span data-ttu-id="474ba-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="474ba-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="474ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="474ba-102">SYNOPSIS</span></span>
<span data-ttu-id="474ba-103">Aktualizuje szczegółowe informacje o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="474ba-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="474ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="474ba-104">SYNTAX</span></span>

### <span data-ttu-id="474ba-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="474ba-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="474ba-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="474ba-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474ba-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="474ba-107">DESCRIPTION</span></span>
<span data-ttu-id="474ba-108">Polecenie **cmdlet Set-AzOperationalInsightsStorageInsight** zmienia konfigurację szczegółowych informacji o magazynie.</span><span class="sxs-lookup"><span data-stu-id="474ba-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="474ba-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="474ba-109">EXAMPLES</span></span>

### <span data-ttu-id="474ba-110">Przykład 1. Modyfikowanie szczegółowych informacji o magazynie według nazwy</span><span class="sxs-lookup"><span data-stu-id="474ba-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="474ba-111">To polecenie modyfikuje tabele, z których odczytuje szczegółowe informacje o magazynie o nazwie MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="474ba-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="474ba-112">Przykład 2. Modyfikowanie szczegółowych informacji o magazynie przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="474ba-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="474ba-113">Pierwsze polecenie używa Get-AzOperationalInsightsWorkspace cmdlet w celu uzyskania obszaru roboczego o nazwie MyWorkspace, a następnie zapisuje go w $Workspace danych.</span><span class="sxs-lookup"><span data-stu-id="474ba-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="474ba-114">Drugie polecenie modyfikuje kontenery, z których odczytuje szczegółowe informacje o magazynie o nazwie MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="474ba-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="474ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="474ba-115">PARAMETERS</span></span>

### <span data-ttu-id="474ba-116">— Containers</span><span class="sxs-lookup"><span data-stu-id="474ba-116">-Containers</span></span>
<span data-ttu-id="474ba-117">Określa listę kontenerów, które dostarczają dane.</span><span class="sxs-lookup"><span data-stu-id="474ba-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="474ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474ba-118">-DefaultProfile</span></span>
<span data-ttu-id="474ba-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="474ba-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="474ba-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="474ba-120">-Name</span></span>
<span data-ttu-id="474ba-121">Określa nazwę szczegółowych informacji o magazynie.</span><span class="sxs-lookup"><span data-stu-id="474ba-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="474ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="474ba-123">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="474ba-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="474ba-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="474ba-124">-StorageAccountKey</span></span>
<span data-ttu-id="474ba-125">Określa klucz dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="474ba-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="474ba-126">— Tabele</span><span class="sxs-lookup"><span data-stu-id="474ba-126">-Tables</span></span>
<span data-ttu-id="474ba-127">Określa listę tabel zawierających dane.</span><span class="sxs-lookup"><span data-stu-id="474ba-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="474ba-128">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="474ba-128">-Workspace</span></span>
<span data-ttu-id="474ba-129">Określa obszar roboczy zawierający szczegółowe informacje o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="474ba-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="474ba-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="474ba-130">-WorkspaceName</span></span>
<span data-ttu-id="474ba-131">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="474ba-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="474ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474ba-132">CommonParameters</span></span>
<span data-ttu-id="474ba-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474ba-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474ba-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474ba-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="474ba-135">INPUTS</span></span>

### <span data-ttu-id="474ba-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="474ba-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="474ba-137">System.String</span><span class="sxs-lookup"><span data-stu-id="474ba-137">System.String</span></span>

### <span data-ttu-id="474ba-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="474ba-138">System.String[]</span></span>

## <span data-ttu-id="474ba-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="474ba-139">OUTPUTS</span></span>

### <span data-ttu-id="474ba-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="474ba-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="474ba-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="474ba-141">NOTES</span></span>

## <span data-ttu-id="474ba-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="474ba-142">RELATED LINKS</span></span>

[<span data-ttu-id="474ba-143">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="474ba-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="474ba-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="474ba-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


