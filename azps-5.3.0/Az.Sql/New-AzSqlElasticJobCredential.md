---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498354"
---
# <span data-ttu-id="1cc23-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="1cc23-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="1cc23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1cc23-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc23-103">Tworzy nowe poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="1cc23-103">Creates a new job credential</span></span>

## <span data-ttu-id="1cc23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1cc23-104">SYNTAX</span></span>

### <span data-ttu-id="1cc23-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1cc23-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cc23-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="1cc23-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cc23-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1cc23-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc23-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1cc23-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc23-109">Polecenie cmdlet New-AzSqlElasticJobCredential tworzy nowe poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="1cc23-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="1cc23-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1cc23-110">EXAMPLES</span></span>

### <span data-ttu-id="1cc23-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1cc23-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="1cc23-112">Tworzy nowe poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="1cc23-112">Creates a new job credential</span></span>

## <span data-ttu-id="1cc23-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1cc23-113">PARAMETERS</span></span>

### <span data-ttu-id="1cc23-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1cc23-114">-AgentName</span></span>
<span data-ttu-id="1cc23-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="1cc23-115">The agent name</span></span>

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

### <span data-ttu-id="1cc23-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="1cc23-116">-Credential</span></span>
<span data-ttu-id="1cc23-117">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="1cc23-117">The credential</span></span>

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

### <span data-ttu-id="1cc23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc23-118">-DefaultProfile</span></span>
<span data-ttu-id="1cc23-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc23-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1cc23-120">-Name</span></span>
<span data-ttu-id="1cc23-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="1cc23-121">The job credential name</span></span>

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

### <span data-ttu-id="1cc23-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="1cc23-122">-ParentObject</span></span>
<span data-ttu-id="1cc23-123">Obiekt Agent</span><span class="sxs-lookup"><span data-stu-id="1cc23-123">The agent object</span></span>

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

### <span data-ttu-id="1cc23-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1cc23-124">-ParentResourceId</span></span>
<span data-ttu-id="1cc23-125">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="1cc23-125">The agent resource id</span></span>

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

### <span data-ttu-id="1cc23-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc23-126">-ResourceGroupName</span></span>
<span data-ttu-id="1cc23-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1cc23-127">The resource group name</span></span>

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

### <span data-ttu-id="1cc23-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1cc23-128">-ServerName</span></span>
<span data-ttu-id="1cc23-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="1cc23-129">The server name</span></span>

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

### <span data-ttu-id="1cc23-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1cc23-130">-Confirm</span></span>
<span data-ttu-id="1cc23-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc23-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc23-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc23-132">-WhatIf</span></span>
<span data-ttu-id="1cc23-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc23-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc23-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1cc23-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc23-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc23-135">CommonParameters</span></span>
<span data-ttu-id="1cc23-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc23-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc23-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cc23-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc23-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cc23-138">INPUTS</span></span>

### <span data-ttu-id="1cc23-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1cc23-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="1cc23-140">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="1cc23-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="1cc23-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1cc23-141">OUTPUTS</span></span>

### <span data-ttu-id="1cc23-142">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="1cc23-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="1cc23-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1cc23-143">NOTES</span></span>

## <span data-ttu-id="1cc23-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cc23-144">RELATED LINKS</span></span>
