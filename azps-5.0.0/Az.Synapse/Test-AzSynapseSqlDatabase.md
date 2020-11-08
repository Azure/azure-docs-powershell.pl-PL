---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224111"
---
# <span data-ttu-id="3cb69-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3cb69-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="3cb69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cb69-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb69-103">Sprawdza, czy istnieje baza danych SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cb69-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="3cb69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cb69-104">SYNTAX</span></span>

### <span data-ttu-id="3cb69-105">TestByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3cb69-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb69-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cb69-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cb69-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3cb69-107">DESCRIPTION</span></span>
<span data-ttu-id="3cb69-108">Polecenie cmdlet **test-AzSynapseSqlDatabase** sprawdza, czy istnieje baza danych SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3cb69-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="3cb69-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cb69-109">EXAMPLES</span></span>

### <span data-ttu-id="3cb69-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3cb69-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="3cb69-111">To polecenie sprawdza istnienie określonej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="3cb69-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="3cb69-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cb69-112">PARAMETERS</span></span>

### <span data-ttu-id="3cb69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb69-113">-DefaultProfile</span></span>
<span data-ttu-id="3cb69-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb69-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb69-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cb69-115">-Name</span></span>
<span data-ttu-id="3cb69-116">Nazwa bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cb69-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="3cb69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb69-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cb69-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cb69-118">Resource group name.</span></span>

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

### <span data-ttu-id="3cb69-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3cb69-119">-WorkspaceName</span></span>
<span data-ttu-id="3cb69-120">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cb69-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3cb69-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3cb69-121">-WorkspaceObject</span></span>
<span data-ttu-id="3cb69-122">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3cb69-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3cb69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb69-123">CommonParameters</span></span>
<span data-ttu-id="3cb69-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb69-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cb69-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb69-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cb69-126">INPUTS</span></span>

### <span data-ttu-id="3cb69-127">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3cb69-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3cb69-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cb69-128">OUTPUTS</span></span>

### <span data-ttu-id="3cb69-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cb69-129">System.Boolean</span></span>

## <span data-ttu-id="3cb69-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cb69-130">NOTES</span></span>

## <span data-ttu-id="3cb69-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cb69-131">RELATED LINKS</span></span>
