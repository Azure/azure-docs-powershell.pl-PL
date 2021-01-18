---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503291"
---
# <span data-ttu-id="c7fa1-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="c7fa1-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="c7fa1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fa1-103">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c7fa1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7fa1-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c7fa1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="c7fa1-106">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c7fa1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7fa1-107">EXAMPLES</span></span>

### <span data-ttu-id="c7fa1-108">Przykład 1: pobieranie repliki serwera MySql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="c7fa1-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="c7fa1-109">To polecenie cmdlet umożliwia pobieranie repliki serwera MySql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="c7fa1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7fa1-110">PARAMETERS</span></span>

### <span data-ttu-id="c7fa1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fa1-111">-DefaultProfile</span></span>
<span data-ttu-id="c7fa1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7fa1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7fa1-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7fa1-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-114">The name of the resource group.</span></span>
<span data-ttu-id="c7fa1-115">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c7fa1-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c7fa1-116">-ServerName</span></span>
<span data-ttu-id="c7fa1-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-117">The name of the server.</span></span>

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

### <span data-ttu-id="c7fa1-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c7fa1-118">-SubscriptionId</span></span>
<span data-ttu-id="c7fa1-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c7fa1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fa1-120">CommonParameters</span></span>
<span data-ttu-id="c7fa1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fa1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fa1-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7fa1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fa1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7fa1-123">INPUTS</span></span>

## <span data-ttu-id="c7fa1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7fa1-124">OUTPUTS</span></span>

### <span data-ttu-id="c7fa1-125">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c7fa1-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="c7fa1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7fa1-126">NOTES</span></span>

<span data-ttu-id="c7fa1-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c7fa1-127">ALIASES</span></span>

## <span data-ttu-id="c7fa1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7fa1-128">RELATED LINKS</span></span>

