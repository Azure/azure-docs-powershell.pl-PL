---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: d5ee112af595ba88672a26d0f8f64590ea670706
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961338"
---
# <span data-ttu-id="9218d-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="9218d-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="9218d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9218d-102">SYNOPSIS</span></span>
<span data-ttu-id="9218d-103">Usuwa elastyczne poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="9218d-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="9218d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9218d-104">SYNTAX</span></span>

### <span data-ttu-id="9218d-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="9218d-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9218d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9218d-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9218d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9218d-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9218d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9218d-108">DESCRIPTION</span></span>
<span data-ttu-id="9218d-109">Polecenie Remove-AzSqlElasticJobCredential cmdlet usuwa poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="9218d-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="9218d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9218d-110">EXAMPLES</span></span>

### <span data-ttu-id="9218d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9218d-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="9218d-112">Usuwa poświadczenia zadania.</span><span class="sxs-lookup"><span data-stu-id="9218d-112">Removes a job credential</span></span>

## <span data-ttu-id="9218d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9218d-113">PARAMETERS</span></span>

### <span data-ttu-id="9218d-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9218d-114">-AgentName</span></span>
<span data-ttu-id="9218d-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="9218d-115">The agent name</span></span>

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

### <span data-ttu-id="9218d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9218d-116">-DefaultProfile</span></span>
<span data-ttu-id="9218d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9218d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9218d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9218d-118">-InputObject</span></span>
<span data-ttu-id="9218d-119">Obiekt poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="9218d-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9218d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9218d-120">-Name</span></span>
<span data-ttu-id="9218d-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="9218d-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9218d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9218d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9218d-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9218d-123">The resource group name</span></span>

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

### <span data-ttu-id="9218d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9218d-124">-ResourceId</span></span>
<span data-ttu-id="9218d-125">Identyfikator zasobu poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="9218d-125">The job credential resource id</span></span>

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

### <span data-ttu-id="9218d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9218d-126">-ServerName</span></span>
<span data-ttu-id="9218d-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="9218d-127">The server name</span></span>

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

### <span data-ttu-id="9218d-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9218d-128">-Confirm</span></span>
<span data-ttu-id="9218d-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9218d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9218d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9218d-130">-WhatIf</span></span>
<span data-ttu-id="9218d-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9218d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9218d-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9218d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9218d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9218d-133">CommonParameters</span></span>
<span data-ttu-id="9218d-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9218d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9218d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9218d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9218d-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9218d-136">INPUTS</span></span>

### <span data-ttu-id="9218d-137">Microsoft.Azure.Commands.Sql.Jego elastycznaobs.model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9218d-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9218d-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9218d-138">OUTPUTS</span></span>

### <span data-ttu-id="9218d-139">Microsoft.Azure.Commands.Sql.Jego elastycznaobs.model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9218d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9218d-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9218d-140">NOTES</span></span>

## <span data-ttu-id="9218d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9218d-141">RELATED LINKS</span></span>
