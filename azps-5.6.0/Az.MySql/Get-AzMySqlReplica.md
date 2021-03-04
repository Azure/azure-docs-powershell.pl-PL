---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: d4579ec17d870c1f002ce40309aa580226ff143d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962833"
---
# <span data-ttu-id="57194-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="57194-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="57194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57194-102">SYNOPSIS</span></span>
<span data-ttu-id="57194-103">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="57194-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="57194-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57194-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57194-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="57194-105">DESCRIPTION</span></span>
<span data-ttu-id="57194-106">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="57194-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="57194-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57194-107">EXAMPLES</span></span>

### <span data-ttu-id="57194-108">Przykład 1. Uzyskiwanie repliki serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="57194-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="57194-109">To polecenie cmdlet pobiera replikę serwera MySql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="57194-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="57194-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57194-110">PARAMETERS</span></span>

### <span data-ttu-id="57194-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57194-111">-DefaultProfile</span></span>
<span data-ttu-id="57194-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57194-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57194-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57194-113">-ResourceGroupName</span></span>
<span data-ttu-id="57194-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57194-114">The name of the resource group.</span></span>
<span data-ttu-id="57194-115">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="57194-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="57194-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57194-116">-ServerName</span></span>
<span data-ttu-id="57194-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="57194-117">The name of the server.</span></span>

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

### <span data-ttu-id="57194-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57194-118">-SubscriptionId</span></span>
<span data-ttu-id="57194-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="57194-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="57194-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57194-120">CommonParameters</span></span>
<span data-ttu-id="57194-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57194-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57194-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57194-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57194-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57194-123">INPUTS</span></span>

## <span data-ttu-id="57194-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57194-124">OUTPUTS</span></span>

### <span data-ttu-id="57194-125">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="57194-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="57194-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57194-126">NOTES</span></span>

<span data-ttu-id="57194-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="57194-127">ALIASES</span></span>

## <span data-ttu-id="57194-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57194-128">RELATED LINKS</span></span>

