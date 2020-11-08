---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220282"
---
# <span data-ttu-id="fc2c9-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="fc2c9-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="fc2c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2c9-103">Usuwa elastyczne poświadczenie zadania.</span><span class="sxs-lookup"><span data-stu-id="fc2c9-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="fc2c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc2c9-104">SYNTAX</span></span>

### <span data-ttu-id="fc2c9-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc2c9-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc2c9-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="fc2c9-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc2c9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc2c9-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc2c9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc2c9-108">DESCRIPTION</span></span>
<span data-ttu-id="fc2c9-109">Polecenie cmdlet Remove-AzSqlElasticJobCredential usuwa poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="fc2c9-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="fc2c9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc2c9-110">EXAMPLES</span></span>

### <span data-ttu-id="fc2c9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc2c9-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="fc2c9-112">Usuwa poświadczenie zadania</span><span class="sxs-lookup"><span data-stu-id="fc2c9-112">Removes a job credential</span></span>

## <span data-ttu-id="fc2c9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc2c9-113">PARAMETERS</span></span>

### <span data-ttu-id="fc2c9-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fc2c9-114">-AgentName</span></span>
<span data-ttu-id="fc2c9-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="fc2c9-115">The agent name</span></span>

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

### <span data-ttu-id="fc2c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2c9-116">-DefaultProfile</span></span>
<span data-ttu-id="fc2c9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc2c9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc2c9-118">-InputObject</span></span>
<span data-ttu-id="fc2c9-119">Obiekt poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="fc2c9-119">The job credential object</span></span>

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

### <span data-ttu-id="fc2c9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc2c9-120">-Name</span></span>
<span data-ttu-id="fc2c9-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="fc2c9-121">The job credential name</span></span>

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

### <span data-ttu-id="fc2c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc2c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc2c9-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fc2c9-123">The resource group name</span></span>

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

### <span data-ttu-id="fc2c9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc2c9-124">-ResourceId</span></span>
<span data-ttu-id="fc2c9-125">Identyfikator zasobu poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="fc2c9-125">The job credential resource id</span></span>

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

### <span data-ttu-id="fc2c9-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fc2c9-126">-ServerName</span></span>
<span data-ttu-id="fc2c9-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="fc2c9-127">The server name</span></span>

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

### <span data-ttu-id="fc2c9-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc2c9-128">-Confirm</span></span>
<span data-ttu-id="fc2c9-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc2c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc2c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc2c9-130">-WhatIf</span></span>
<span data-ttu-id="fc2c9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc2c9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc2c9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc2c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc2c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2c9-133">CommonParameters</span></span>
<span data-ttu-id="fc2c9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc2c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2c9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc2c9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2c9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc2c9-136">INPUTS</span></span>

### <span data-ttu-id="fc2c9-137">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="fc2c9-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="fc2c9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc2c9-138">OUTPUTS</span></span>

### <span data-ttu-id="fc2c9-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="fc2c9-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="fc2c9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc2c9-140">NOTES</span></span>

## <span data-ttu-id="fc2c9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc2c9-141">RELATED LINKS</span></span>
