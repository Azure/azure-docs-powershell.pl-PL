---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970657"
---
# <span data-ttu-id="ca331-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="ca331-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="ca331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca331-102">SYNOPSIS</span></span>
<span data-ttu-id="ca331-103">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="ca331-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ca331-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca331-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ca331-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca331-105">DESCRIPTION</span></span>
<span data-ttu-id="ca331-106">Lista wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="ca331-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ca331-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca331-107">EXAMPLES</span></span>

### <span data-ttu-id="ca331-108">Przykład 1. Lista wszystkich replik bazy danych w obszarze bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="ca331-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ca331-109">To polecenie wyświetla listę wszystkich replik bazy danych w obszarze bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ca331-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="ca331-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca331-110">PARAMETERS</span></span>

### <span data-ttu-id="ca331-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca331-111">-DefaultProfile</span></span>
<span data-ttu-id="ca331-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca331-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca331-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca331-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca331-114">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="ca331-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ca331-115">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="ca331-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ca331-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca331-116">-ServerName</span></span>
<span data-ttu-id="ca331-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="ca331-117">The name of the server.</span></span>

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

### <span data-ttu-id="ca331-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca331-118">-SubscriptionId</span></span>
<span data-ttu-id="ca331-119">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca331-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ca331-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca331-120">CommonParameters</span></span>
<span data-ttu-id="ca331-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca331-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca331-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca331-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca331-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca331-123">INPUTS</span></span>

## <span data-ttu-id="ca331-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca331-124">OUTPUTS</span></span>

### <span data-ttu-id="ca331-125">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ca331-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ca331-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca331-126">NOTES</span></span>

<span data-ttu-id="ca331-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ca331-127">ALIASES</span></span>

## <span data-ttu-id="ca331-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca331-128">RELATED LINKS</span></span>

