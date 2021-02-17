---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176827"
---
# <span data-ttu-id="54645-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="54645-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="54645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54645-102">SYNOPSIS</span></span>
<span data-ttu-id="54645-103">Usuwa elastyczne poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="54645-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="54645-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54645-104">SYNTAX</span></span>

### <span data-ttu-id="54645-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="54645-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54645-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="54645-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54645-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54645-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54645-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="54645-108">DESCRIPTION</span></span>
<span data-ttu-id="54645-109">Polecenie Remove-AzSqlElasticJobCredential cmdlet usuwa poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="54645-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="54645-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54645-110">EXAMPLES</span></span>

### <span data-ttu-id="54645-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54645-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="54645-112">Usuwa poświadczenia zadania.</span><span class="sxs-lookup"><span data-stu-id="54645-112">Removes a job credential</span></span>

## <span data-ttu-id="54645-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54645-113">PARAMETERS</span></span>

### <span data-ttu-id="54645-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="54645-114">-AgentName</span></span>
<span data-ttu-id="54645-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="54645-115">The agent name</span></span>

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

### <span data-ttu-id="54645-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54645-116">-DefaultProfile</span></span>
<span data-ttu-id="54645-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54645-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54645-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54645-118">-InputObject</span></span>
<span data-ttu-id="54645-119">Obiekt poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="54645-119">The job credential object</span></span>

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

### <span data-ttu-id="54645-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="54645-120">-Name</span></span>
<span data-ttu-id="54645-121">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="54645-121">The job credential name</span></span>

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

### <span data-ttu-id="54645-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54645-122">-ResourceGroupName</span></span>
<span data-ttu-id="54645-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="54645-123">The resource group name</span></span>

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

### <span data-ttu-id="54645-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54645-124">-ResourceId</span></span>
<span data-ttu-id="54645-125">Identyfikator zasobu poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="54645-125">The job credential resource id</span></span>

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

### <span data-ttu-id="54645-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54645-126">-ServerName</span></span>
<span data-ttu-id="54645-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="54645-127">The server name</span></span>

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

### <span data-ttu-id="54645-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54645-128">-Confirm</span></span>
<span data-ttu-id="54645-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="54645-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54645-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54645-130">-WhatIf</span></span>
<span data-ttu-id="54645-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54645-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54645-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="54645-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54645-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54645-133">CommonParameters</span></span>
<span data-ttu-id="54645-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54645-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54645-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54645-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54645-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54645-136">INPUTS</span></span>

### <span data-ttu-id="54645-137">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="54645-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="54645-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54645-138">OUTPUTS</span></span>

### <span data-ttu-id="54645-139">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="54645-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="54645-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54645-140">NOTES</span></span>

## <span data-ttu-id="54645-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54645-141">RELATED LINKS</span></span>
