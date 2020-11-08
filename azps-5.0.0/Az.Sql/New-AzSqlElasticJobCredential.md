---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225641"
---
# <span data-ttu-id="c125a-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="c125a-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="c125a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c125a-102">SYNOPSIS</span></span>
<span data-ttu-id="c125a-103">Tworzy nowe poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="c125a-103">Creates a new job credential</span></span>

## <span data-ttu-id="c125a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c125a-104">SYNTAX</span></span>

### <span data-ttu-id="c125a-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c125a-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c125a-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="c125a-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c125a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c125a-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c125a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c125a-108">DESCRIPTION</span></span>
<span data-ttu-id="c125a-109">Polecenie cmdlet New-AzSqlElasticJobCredential tworzy nowe poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="c125a-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="c125a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c125a-110">EXAMPLES</span></span>

### <span data-ttu-id="c125a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c125a-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="c125a-112">Tworzy nowe poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="c125a-112">Creates a new job credential</span></span>

## <span data-ttu-id="c125a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c125a-113">PARAMETERS</span></span>

### <span data-ttu-id="c125a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c125a-114">-AgentName</span></span>
<span data-ttu-id="c125a-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="c125a-115">The agent name</span></span>

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

### <span data-ttu-id="c125a-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="c125a-116">-Credential</span></span>
<span data-ttu-id="c125a-117">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="c125a-117">The credential</span></span>

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

### <span data-ttu-id="c125a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c125a-118">-DefaultProfile</span></span>
<span data-ttu-id="c125a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c125a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c125a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c125a-120">-Name</span></span>
<span data-ttu-id="c125a-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="c125a-121">The job credential name</span></span>

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

### <span data-ttu-id="c125a-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="c125a-122">-ParentObject</span></span>
<span data-ttu-id="c125a-123">Obiekt Agent</span><span class="sxs-lookup"><span data-stu-id="c125a-123">The agent object</span></span>

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

### <span data-ttu-id="c125a-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c125a-124">-ParentResourceId</span></span>
<span data-ttu-id="c125a-125">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="c125a-125">The agent resource id</span></span>

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

### <span data-ttu-id="c125a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c125a-126">-ResourceGroupName</span></span>
<span data-ttu-id="c125a-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c125a-127">The resource group name</span></span>

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

### <span data-ttu-id="c125a-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c125a-128">-ServerName</span></span>
<span data-ttu-id="c125a-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="c125a-129">The server name</span></span>

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

### <span data-ttu-id="c125a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c125a-130">-Confirm</span></span>
<span data-ttu-id="c125a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c125a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c125a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c125a-132">-WhatIf</span></span>
<span data-ttu-id="c125a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c125a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c125a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c125a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c125a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c125a-135">CommonParameters</span></span>
<span data-ttu-id="c125a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c125a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c125a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c125a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c125a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c125a-138">INPUTS</span></span>

### <span data-ttu-id="c125a-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c125a-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="c125a-140">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="c125a-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c125a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c125a-141">OUTPUTS</span></span>

### <span data-ttu-id="c125a-142">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="c125a-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="c125a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c125a-143">NOTES</span></span>

## <span data-ttu-id="c125a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c125a-144">RELATED LINKS</span></span>
