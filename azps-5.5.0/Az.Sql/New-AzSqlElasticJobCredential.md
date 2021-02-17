---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191027"
---
# <span data-ttu-id="d7cef-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="d7cef-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="d7cef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7cef-102">SYNOPSIS</span></span>
<span data-ttu-id="d7cef-103">Tworzy nowe poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="d7cef-103">Creates a new job credential</span></span>

## <span data-ttu-id="d7cef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7cef-104">SYNTAX</span></span>

### <span data-ttu-id="d7cef-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="d7cef-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7cef-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7cef-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7cef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d7cef-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7cef-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7cef-108">DESCRIPTION</span></span>
<span data-ttu-id="d7cef-109">Polecenie New-AzSqlElasticJobCredential cmdlet tworzy nowe poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="d7cef-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="d7cef-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7cef-110">EXAMPLES</span></span>

### <span data-ttu-id="d7cef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7cef-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="d7cef-112">Tworzy nowe poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="d7cef-112">Creates a new job credential</span></span>

## <span data-ttu-id="d7cef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7cef-113">PARAMETERS</span></span>

### <span data-ttu-id="d7cef-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d7cef-114">-AgentName</span></span>
<span data-ttu-id="d7cef-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="d7cef-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-116">- Credential</span><span class="sxs-lookup"><span data-stu-id="d7cef-116">-Credential</span></span>
<span data-ttu-id="d7cef-117">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="d7cef-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7cef-118">-DefaultProfile</span></span>
<span data-ttu-id="d7cef-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7cef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7cef-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7cef-120">-Name</span></span>
<span data-ttu-id="d7cef-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="d7cef-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7cef-122">-ParentObject</span></span>
<span data-ttu-id="d7cef-123">Obiekt agenta</span><span class="sxs-lookup"><span data-stu-id="d7cef-123">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d7cef-124">-ParentResourceId</span></span>
<span data-ttu-id="d7cef-125">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="d7cef-125">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7cef-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7cef-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d7cef-127">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7cef-128">-ServerName</span></span>
<span data-ttu-id="d7cef-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="d7cef-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cef-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7cef-130">-Confirm</span></span>
<span data-ttu-id="d7cef-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7cef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7cef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7cef-132">-WhatIf</span></span>
<span data-ttu-id="d7cef-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7cef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7cef-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d7cef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7cef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7cef-135">CommonParameters</span></span>
<span data-ttu-id="d7cef-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7cef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7cef-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7cef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7cef-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7cef-138">INPUTS</span></span>

### <span data-ttu-id="d7cef-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="d7cef-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="d7cef-140">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d7cef-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d7cef-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7cef-141">OUTPUTS</span></span>

### <span data-ttu-id="d7cef-142">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="d7cef-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="d7cef-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7cef-143">NOTES</span></span>

## <span data-ttu-id="d7cef-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7cef-144">RELATED LINKS</span></span>
