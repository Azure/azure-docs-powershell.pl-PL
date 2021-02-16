---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180098"
---
# <span data-ttu-id="eaffc-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="eaffc-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="eaffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaffc-102">SYNOPSIS</span></span>
<span data-ttu-id="eaffc-103">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="eaffc-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="eaffc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eaffc-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eaffc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="eaffc-105">DESCRIPTION</span></span>
<span data-ttu-id="eaffc-106">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="eaffc-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="eaffc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eaffc-107">EXAMPLES</span></span>

### <span data-ttu-id="eaffc-108">Przykład 1. Uzyskiwanie repliki serwera MySql według nazwy grupy zasobów i serwera</span><span class="sxs-lookup"><span data-stu-id="eaffc-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="eaffc-109">To polecenie cmdlet pobiera replikę serwera MySql według nazwy grupy zasobów i serwera.</span><span class="sxs-lookup"><span data-stu-id="eaffc-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="eaffc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaffc-110">PARAMETERS</span></span>

### <span data-ttu-id="eaffc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaffc-111">-DefaultProfile</span></span>
<span data-ttu-id="eaffc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaffc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaffc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaffc-113">-ResourceGroupName</span></span>
<span data-ttu-id="eaffc-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eaffc-114">The name of the resource group.</span></span>
<span data-ttu-id="eaffc-115">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="eaffc-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="eaffc-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eaffc-116">-ServerName</span></span>
<span data-ttu-id="eaffc-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="eaffc-117">The name of the server.</span></span>

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

### <span data-ttu-id="eaffc-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eaffc-118">-SubscriptionId</span></span>
<span data-ttu-id="eaffc-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="eaffc-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="eaffc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaffc-120">CommonParameters</span></span>
<span data-ttu-id="eaffc-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaffc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaffc-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaffc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaffc-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaffc-123">INPUTS</span></span>

## <span data-ttu-id="eaffc-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eaffc-124">OUTPUTS</span></span>

### <span data-ttu-id="eaffc-125">Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer</span><span class="sxs-lookup"><span data-stu-id="eaffc-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="eaffc-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eaffc-126">NOTES</span></span>

<span data-ttu-id="eaffc-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="eaffc-127">ALIASES</span></span>

## <span data-ttu-id="eaffc-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaffc-128">RELATED LINKS</span></span>

