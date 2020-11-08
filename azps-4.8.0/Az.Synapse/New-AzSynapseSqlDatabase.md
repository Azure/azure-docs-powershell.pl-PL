---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063032"
---
# <span data-ttu-id="8cc5d-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc5d-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="8cc5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc5d-103">Tworzy bazę danych SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="8cc5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cc5d-104">SYNTAX</span></span>

### <span data-ttu-id="8cc5d-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cc5d-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc5d-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cc5d-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc5d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8cc5d-107">DESCRIPTION</span></span>
<span data-ttu-id="8cc5d-108">Polecenie cmdlet **Get-AzSynapseSqlDatabase** pobiera informacje o bazie danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="8cc5d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cc5d-109">EXAMPLES</span></span>

### <span data-ttu-id="8cc5d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8cc5d-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="8cc5d-111">To polecenie tworzy bazę danych SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="8cc5d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cc5d-112">PARAMETERS</span></span>

### <span data-ttu-id="8cc5d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cc5d-113">-AsJob</span></span>
<span data-ttu-id="8cc5d-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8cc5d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cc5d-115">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="8cc5d-115">-Collation</span></span>
<span data-ttu-id="8cc5d-116">Sortowanie definiuje reguły, które sortują i porównują dane, i nie można ich zmieniać po utworzeniu puli SQL.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="8cc5d-117">Domyślnym sortowaniem jest SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc5d-118">-DefaultProfile</span></span>
<span data-ttu-id="8cc5d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc5d-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="8cc5d-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="8cc5d-121">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cc5d-122">-Name</span></span>
<span data-ttu-id="8cc5d-123">Nazwa bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="8cc5d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc5d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cc5d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8cc5d-126">-Tag</span></span>
<span data-ttu-id="8cc5d-127">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-127">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8cc5d-128">-WorkspaceName</span></span>
<span data-ttu-id="8cc5d-129">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8cc5d-130">-WorkspaceObject</span></span>
<span data-ttu-id="8cc5d-131">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cc5d-132">-Confirm</span></span>
<span data-ttu-id="8cc5d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc5d-134">-WhatIf</span></span>
<span data-ttu-id="8cc5d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc5d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc5d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc5d-137">CommonParameters</span></span>
<span data-ttu-id="8cc5d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc5d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc5d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cc5d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc5d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cc5d-140">INPUTS</span></span>

### <span data-ttu-id="8cc5d-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8cc5d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8cc5d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cc5d-142">OUTPUTS</span></span>

### <span data-ttu-id="8cc5d-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc5d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="8cc5d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cc5d-144">NOTES</span></span>

## <span data-ttu-id="8cc5d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cc5d-145">RELATED LINKS</span></span>
