---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e797cba0c05b6dbaee11d540b9efc3aca7e7efcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011258"
---
# <span data-ttu-id="5abe1-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5abe1-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="5abe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5abe1-102">SYNOPSIS</span></span>
<span data-ttu-id="5abe1-103">Sprawdza, czy istnieje baza danych Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="5abe1-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5abe1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5abe1-104">SYNTAX</span></span>

### <span data-ttu-id="5abe1-105">TestByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5abe1-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5abe1-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5abe1-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5abe1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5abe1-107">DESCRIPTION</span></span>
<span data-ttu-id="5abe1-108">Polecenie **cmdlet Test-AzSynapseSqlDatabase** sprawdza, czy istnieje baza danych SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5abe1-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5abe1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5abe1-109">EXAMPLES</span></span>

### <span data-ttu-id="5abe1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5abe1-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="5abe1-111">To polecenie sprawdza istnienie określonej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5abe1-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="5abe1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5abe1-112">PARAMETERS</span></span>

### <span data-ttu-id="5abe1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abe1-113">-DefaultProfile</span></span>
<span data-ttu-id="5abe1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5abe1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5abe1-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5abe1-115">-Name</span></span>
<span data-ttu-id="5abe1-116">Nazwa bazy danych Synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5abe1-116">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abe1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5abe1-117">-ResourceGroupName</span></span>
<span data-ttu-id="5abe1-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5abe1-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abe1-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5abe1-119">-WorkspaceName</span></span>
<span data-ttu-id="5abe1-120">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="5abe1-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abe1-121">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5abe1-121">-WorkspaceObject</span></span>
<span data-ttu-id="5abe1-122">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="5abe1-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5abe1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abe1-123">CommonParameters</span></span>
<span data-ttu-id="5abe1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5abe1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5abe1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5abe1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abe1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5abe1-126">INPUTS</span></span>

### <span data-ttu-id="5abe1-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5abe1-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5abe1-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5abe1-128">OUTPUTS</span></span>

### <span data-ttu-id="5abe1-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5abe1-129">System.Boolean</span></span>

## <span data-ttu-id="5abe1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5abe1-130">NOTES</span></span>

## <span data-ttu-id="5abe1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5abe1-131">RELATED LINKS</span></span>
