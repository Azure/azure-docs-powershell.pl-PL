---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190243"
---
# <span data-ttu-id="f02a7-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="f02a7-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="f02a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f02a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f02a7-103">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="f02a7-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="f02a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f02a7-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f02a7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f02a7-105">DESCRIPTION</span></span>
<span data-ttu-id="f02a7-106">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="f02a7-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="f02a7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f02a7-107">EXAMPLES</span></span>

### <span data-ttu-id="f02a7-108">Przykład 1. Lista wszystkich replik bazy danych w obszarze bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="f02a7-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="f02a7-109">To polecenie wyświetla listę wszystkich replik bazy danych w obszarze bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f02a7-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="f02a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f02a7-110">PARAMETERS</span></span>

### <span data-ttu-id="f02a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02a7-111">-DefaultProfile</span></span>
<span data-ttu-id="f02a7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f02a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02a7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02a7-113">-ResourceGroupName</span></span>
<span data-ttu-id="f02a7-114">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="f02a7-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f02a7-115">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="f02a7-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f02a7-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f02a7-116">-ServerName</span></span>
<span data-ttu-id="f02a7-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f02a7-117">The name of the server.</span></span>

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

### <span data-ttu-id="f02a7-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f02a7-118">-SubscriptionId</span></span>
<span data-ttu-id="f02a7-119">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f02a7-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f02a7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02a7-120">CommonParameters</span></span>
<span data-ttu-id="f02a7-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02a7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02a7-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f02a7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02a7-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f02a7-123">INPUTS</span></span>

## <span data-ttu-id="f02a7-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f02a7-124">OUTPUTS</span></span>

### <span data-ttu-id="f02a7-125">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="f02a7-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="f02a7-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f02a7-126">NOTES</span></span>

<span data-ttu-id="f02a7-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f02a7-127">ALIASES</span></span>

## <span data-ttu-id="f02a7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f02a7-128">RELATED LINKS</span></span>

