---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374563"
---
# <span data-ttu-id="29967-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="29967-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="29967-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29967-102">SYNOPSIS</span></span>
<span data-ttu-id="29967-103">Usuwa elastyczne poświadczenie zadania.</span><span class="sxs-lookup"><span data-stu-id="29967-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="29967-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29967-104">SYNTAX</span></span>

### <span data-ttu-id="29967-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29967-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29967-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="29967-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29967-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29967-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29967-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29967-108">DESCRIPTION</span></span>
<span data-ttu-id="29967-109">Polecenie cmdlet Remove-AzSqlElasticJobCredential usuwa poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="29967-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="29967-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29967-110">EXAMPLES</span></span>

### <span data-ttu-id="29967-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29967-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="29967-112">Usuwa poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="29967-112">Removes a job credential</span></span>

## <span data-ttu-id="29967-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29967-113">PARAMETERS</span></span>

### <span data-ttu-id="29967-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="29967-114">-AgentName</span></span>
<span data-ttu-id="29967-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="29967-115">The agent name</span></span>

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

### <span data-ttu-id="29967-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29967-116">-DefaultProfile</span></span>
<span data-ttu-id="29967-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29967-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29967-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29967-118">-InputObject</span></span>
<span data-ttu-id="29967-119">Obiekt poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="29967-119">The job credential object</span></span>

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

### <span data-ttu-id="29967-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29967-120">-Name</span></span>
<span data-ttu-id="29967-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="29967-121">The job credential name</span></span>

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

### <span data-ttu-id="29967-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29967-122">-ResourceGroupName</span></span>
<span data-ttu-id="29967-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="29967-123">The resource group name</span></span>

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

### <span data-ttu-id="29967-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29967-124">-ResourceId</span></span>
<span data-ttu-id="29967-125">Identyfikator zasobu poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="29967-125">The job credential resource id</span></span>

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

### <span data-ttu-id="29967-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="29967-126">-ServerName</span></span>
<span data-ttu-id="29967-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="29967-127">The server name</span></span>

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

### <span data-ttu-id="29967-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29967-128">-Confirm</span></span>
<span data-ttu-id="29967-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29967-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29967-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29967-130">-WhatIf</span></span>
<span data-ttu-id="29967-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29967-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29967-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29967-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29967-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29967-133">CommonParameters</span></span>
<span data-ttu-id="29967-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29967-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29967-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29967-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29967-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29967-136">INPUTS</span></span>

### <span data-ttu-id="29967-137">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="29967-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="29967-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29967-138">OUTPUTS</span></span>

### <span data-ttu-id="29967-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="29967-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="29967-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29967-140">NOTES</span></span>

## <span data-ttu-id="29967-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29967-141">RELATED LINKS</span></span>
