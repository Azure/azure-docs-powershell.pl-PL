---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195970"
---
# <span data-ttu-id="702a3-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="702a3-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="702a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="702a3-102">SYNOPSIS</span></span>
<span data-ttu-id="702a3-103">Aktualizuje poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="702a3-103">Updates a job credential</span></span>

## <span data-ttu-id="702a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="702a3-104">SYNTAX</span></span>

### <span data-ttu-id="702a3-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="702a3-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="702a3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="702a3-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="702a3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="702a3-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="702a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="702a3-108">DESCRIPTION</span></span>
<span data-ttu-id="702a3-109">Polecenie cmdlet Set-AzSqlElasticJobCredential aktualizuje poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="702a3-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="702a3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="702a3-110">EXAMPLES</span></span>

### <span data-ttu-id="702a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="702a3-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="702a3-112">Aktualizuje poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="702a3-112">Updates a job credential</span></span>

## <span data-ttu-id="702a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="702a3-113">PARAMETERS</span></span>

### <span data-ttu-id="702a3-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="702a3-114">-AgentName</span></span>
<span data-ttu-id="702a3-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="702a3-115">The agent name</span></span>

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

### <span data-ttu-id="702a3-116">- Credential</span><span class="sxs-lookup"><span data-stu-id="702a3-116">-Credential</span></span>
<span data-ttu-id="702a3-117">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="702a3-117">The credential</span></span>

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

### <span data-ttu-id="702a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702a3-118">-DefaultProfile</span></span>
<span data-ttu-id="702a3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="702a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="702a3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="702a3-120">-InputObject</span></span>
<span data-ttu-id="702a3-121">Obiekt poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="702a3-121">The job credential object</span></span>

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

### <span data-ttu-id="702a3-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="702a3-122">-Name</span></span>
<span data-ttu-id="702a3-123">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="702a3-123">The job credential name</span></span>

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

### <span data-ttu-id="702a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="702a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="702a3-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="702a3-125">The resource group name</span></span>

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

### <span data-ttu-id="702a3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="702a3-126">-ResourceId</span></span>
<span data-ttu-id="702a3-127">Identyfikator zasobu poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="702a3-127">The job credential resource id</span></span>

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

### <span data-ttu-id="702a3-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="702a3-128">-ServerName</span></span>
<span data-ttu-id="702a3-129">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="702a3-129">The server name</span></span>

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

### <span data-ttu-id="702a3-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="702a3-130">-Confirm</span></span>
<span data-ttu-id="702a3-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="702a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="702a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="702a3-132">-WhatIf</span></span>
<span data-ttu-id="702a3-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="702a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="702a3-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="702a3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="702a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702a3-135">CommonParameters</span></span>
<span data-ttu-id="702a3-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="702a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702a3-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="702a3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702a3-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="702a3-138">INPUTS</span></span>

### <span data-ttu-id="702a3-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="702a3-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="702a3-140">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="702a3-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="702a3-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="702a3-141">OUTPUTS</span></span>

### <span data-ttu-id="702a3-142">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="702a3-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="702a3-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="702a3-143">NOTES</span></span>

## <span data-ttu-id="702a3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="702a3-144">RELATED LINKS</span></span>
