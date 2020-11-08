---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233375"
---
# <span data-ttu-id="43a89-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="43a89-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="43a89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43a89-102">SYNOPSIS</span></span>
<span data-ttu-id="43a89-103">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="43a89-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="43a89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43a89-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="43a89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43a89-105">DESCRIPTION</span></span>
<span data-ttu-id="43a89-106">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="43a89-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="43a89-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43a89-107">EXAMPLES</span></span>

### <span data-ttu-id="43a89-108">Przykład 1: Wyświetlanie całej repliki bazy danych w ramach MariaDB</span><span class="sxs-lookup"><span data-stu-id="43a89-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="43a89-109">To polecenie wyświetla listę wszystkich replik DB w MariaDB.</span><span class="sxs-lookup"><span data-stu-id="43a89-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="43a89-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43a89-110">PARAMETERS</span></span>

### <span data-ttu-id="43a89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a89-111">-DefaultProfile</span></span>
<span data-ttu-id="43a89-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43a89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a89-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a89-113">-ResourceGroupName</span></span>
<span data-ttu-id="43a89-114">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="43a89-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="43a89-115">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="43a89-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="43a89-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="43a89-116">-ServerName</span></span>
<span data-ttu-id="43a89-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="43a89-117">The name of the server.</span></span>

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

### <span data-ttu-id="43a89-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="43a89-118">-SubscriptionId</span></span>
<span data-ttu-id="43a89-119">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43a89-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="43a89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a89-120">CommonParameters</span></span>
<span data-ttu-id="43a89-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a89-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43a89-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a89-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43a89-123">INPUTS</span></span>

## <span data-ttu-id="43a89-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43a89-124">OUTPUTS</span></span>

### <span data-ttu-id="43a89-125">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="43a89-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="43a89-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43a89-126">NOTES</span></span>

<span data-ttu-id="43a89-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="43a89-127">ALIASES</span></span>

## <span data-ttu-id="43a89-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43a89-128">RELATED LINKS</span></span>

