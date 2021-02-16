---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179147"
---
# <span data-ttu-id="a097f-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="a097f-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="a097f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a097f-102">SYNOPSIS</span></span>
<span data-ttu-id="a097f-103">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="a097f-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="a097f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a097f-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a097f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a097f-105">DESCRIPTION</span></span>
<span data-ttu-id="a097f-106">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="a097f-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="a097f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a097f-107">EXAMPLES</span></span>

### <span data-ttu-id="a097f-108">Przykład 1. Uzyskiwanie repliki serwera PostgreSql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="a097f-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a097f-109">To polecenie cmdlet pobiera replikę serwera PostgreSql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="a097f-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="a097f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a097f-110">PARAMETERS</span></span>

### <span data-ttu-id="a097f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a097f-111">-DefaultProfile</span></span>
<span data-ttu-id="a097f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a097f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a097f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a097f-113">-ResourceGroupName</span></span>
<span data-ttu-id="a097f-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a097f-114">The name of the resource group.</span></span>
<span data-ttu-id="a097f-115">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="a097f-115">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a097f-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a097f-116">-ServerName</span></span>
<span data-ttu-id="a097f-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a097f-117">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a097f-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a097f-118">-SubscriptionId</span></span>
<span data-ttu-id="a097f-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a097f-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a097f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a097f-120">CommonParameters</span></span>
<span data-ttu-id="a097f-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a097f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a097f-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a097f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a097f-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a097f-123">INPUTS</span></span>

## <span data-ttu-id="a097f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a097f-124">OUTPUTS</span></span>

### <span data-ttu-id="a097f-125">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a097f-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a097f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a097f-126">NOTES</span></span>

<span data-ttu-id="a097f-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a097f-127">ALIASES</span></span>

## <span data-ttu-id="a097f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a097f-128">RELATED LINKS</span></span>

