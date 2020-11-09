---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308215"
---
# <span data-ttu-id="37c1a-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="37c1a-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="37c1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="37c1a-103">Aktualizowanie poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="37c1a-103">Updates a job credential</span></span>

## <span data-ttu-id="37c1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37c1a-104">SYNTAX</span></span>

### <span data-ttu-id="37c1a-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="37c1a-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37c1a-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="37c1a-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37c1a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37c1a-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c1a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="37c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="37c1a-109">Polecenie cmdlet Set-AzSqlElasticJobCredential aktualizuje poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="37c1a-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="37c1a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37c1a-110">EXAMPLES</span></span>

### <span data-ttu-id="37c1a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37c1a-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="37c1a-112">Aktualizowanie poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="37c1a-112">Updates a job credential</span></span>

## <span data-ttu-id="37c1a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37c1a-113">PARAMETERS</span></span>

### <span data-ttu-id="37c1a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="37c1a-114">-AgentName</span></span>
<span data-ttu-id="37c1a-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="37c1a-115">The agent name</span></span>

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

### <span data-ttu-id="37c1a-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="37c1a-116">-Credential</span></span>
<span data-ttu-id="37c1a-117">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="37c1a-117">The credential</span></span>

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

### <span data-ttu-id="37c1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c1a-118">-DefaultProfile</span></span>
<span data-ttu-id="37c1a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37c1a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c1a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37c1a-120">-InputObject</span></span>
<span data-ttu-id="37c1a-121">Obiekt poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="37c1a-121">The job credential object</span></span>

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

### <span data-ttu-id="37c1a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37c1a-122">-Name</span></span>
<span data-ttu-id="37c1a-123">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="37c1a-123">The job credential name</span></span>

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

### <span data-ttu-id="37c1a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c1a-124">-ResourceGroupName</span></span>
<span data-ttu-id="37c1a-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="37c1a-125">The resource group name</span></span>

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

### <span data-ttu-id="37c1a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37c1a-126">-ResourceId</span></span>
<span data-ttu-id="37c1a-127">Identyfikator zasobu poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="37c1a-127">The job credential resource id</span></span>

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

### <span data-ttu-id="37c1a-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="37c1a-128">-ServerName</span></span>
<span data-ttu-id="37c1a-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="37c1a-129">The server name</span></span>

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

### <span data-ttu-id="37c1a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37c1a-130">-Confirm</span></span>
<span data-ttu-id="37c1a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c1a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c1a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c1a-132">-WhatIf</span></span>
<span data-ttu-id="37c1a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c1a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c1a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37c1a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c1a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c1a-135">CommonParameters</span></span>
<span data-ttu-id="37c1a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c1a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c1a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37c1a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c1a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37c1a-138">INPUTS</span></span>

### <span data-ttu-id="37c1a-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="37c1a-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="37c1a-140">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="37c1a-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="37c1a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37c1a-141">OUTPUTS</span></span>

### <span data-ttu-id="37c1a-142">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="37c1a-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="37c1a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37c1a-143">NOTES</span></span>

## <span data-ttu-id="37c1a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37c1a-144">RELATED LINKS</span></span>
