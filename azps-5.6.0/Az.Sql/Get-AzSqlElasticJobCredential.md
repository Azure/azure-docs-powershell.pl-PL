---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 466df2e5be2c9193cce49cf9b06a5f8ff0d10e94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014577"
---
# <span data-ttu-id="2320d-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="2320d-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="2320d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2320d-102">SYNOPSIS</span></span>
<span data-ttu-id="2320d-103">Pobiera co najmniej jedno poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="2320d-103">Gets one or more credentials</span></span>

## <span data-ttu-id="2320d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2320d-104">SYNTAX</span></span>

### <span data-ttu-id="2320d-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="2320d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2320d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2320d-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2320d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2320d-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2320d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2320d-108">DESCRIPTION</span></span>
<span data-ttu-id="2320d-109">Polecenie Get-AzSqlElasticJobCredential pobiera jedno lub więcej poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="2320d-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="2320d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2320d-110">EXAMPLES</span></span>

### <span data-ttu-id="2320d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2320d-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="2320d-112">Pobiera poświadczenia zadania</span><span class="sxs-lookup"><span data-stu-id="2320d-112">Gets a job credential</span></span>

## <span data-ttu-id="2320d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2320d-113">PARAMETERS</span></span>

### <span data-ttu-id="2320d-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2320d-114">-AgentName</span></span>
<span data-ttu-id="2320d-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="2320d-115">The agent name</span></span>

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

### <span data-ttu-id="2320d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2320d-116">-DefaultProfile</span></span>
<span data-ttu-id="2320d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2320d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2320d-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2320d-118">-Name</span></span>
<span data-ttu-id="2320d-119">Nazwa poświadczeń zadania</span><span class="sxs-lookup"><span data-stu-id="2320d-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2320d-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="2320d-120">-ParentObject</span></span>
<span data-ttu-id="2320d-121">Obiekt agenta</span><span class="sxs-lookup"><span data-stu-id="2320d-121">The agent object</span></span>

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

### <span data-ttu-id="2320d-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2320d-122">-ParentResourceId</span></span>
<span data-ttu-id="2320d-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="2320d-123">The agent resource id</span></span>

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

### <span data-ttu-id="2320d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2320d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2320d-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2320d-125">The resource group name</span></span>

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

### <span data-ttu-id="2320d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2320d-126">-ServerName</span></span>
<span data-ttu-id="2320d-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="2320d-127">The server name</span></span>

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

### <span data-ttu-id="2320d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2320d-128">CommonParameters</span></span>
<span data-ttu-id="2320d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2320d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2320d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2320d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2320d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2320d-131">INPUTS</span></span>

### <span data-ttu-id="2320d-132">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2320d-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2320d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2320d-133">OUTPUTS</span></span>

### <span data-ttu-id="2320d-134">Microsoft.Azure.Commands.Sql.Jego elastycznaobs.model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="2320d-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="2320d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2320d-135">NOTES</span></span>

## <span data-ttu-id="2320d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2320d-136">RELATED LINKS</span></span>
