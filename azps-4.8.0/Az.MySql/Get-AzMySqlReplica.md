---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222443"
---
# <span data-ttu-id="0605d-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="0605d-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="0605d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0605d-102">SYNOPSIS</span></span>
<span data-ttu-id="0605d-103">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="0605d-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0605d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0605d-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0605d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0605d-105">DESCRIPTION</span></span>
<span data-ttu-id="0605d-106">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="0605d-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0605d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0605d-107">EXAMPLES</span></span>

### <span data-ttu-id="0605d-108">Przykład 1: pobieranie repliki serwera MySql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="0605d-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0605d-109">To polecenie cmdlet umożliwia pobieranie repliki serwera MySql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="0605d-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="0605d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0605d-110">PARAMETERS</span></span>

### <span data-ttu-id="0605d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0605d-111">-DefaultProfile</span></span>
<span data-ttu-id="0605d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0605d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0605d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0605d-113">-ResourceGroupName</span></span>
<span data-ttu-id="0605d-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0605d-114">The name of the resource group.</span></span>
<span data-ttu-id="0605d-115">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0605d-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0605d-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0605d-116">-ServerName</span></span>
<span data-ttu-id="0605d-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0605d-117">The name of the server.</span></span>

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

### <span data-ttu-id="0605d-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0605d-118">-SubscriptionId</span></span>
<span data-ttu-id="0605d-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0605d-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0605d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0605d-120">CommonParameters</span></span>
<span data-ttu-id="0605d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0605d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0605d-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0605d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0605d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0605d-123">INPUTS</span></span>

## <span data-ttu-id="0605d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0605d-124">OUTPUTS</span></span>

### <span data-ttu-id="0605d-125">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0605d-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0605d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0605d-126">NOTES</span></span>

<span data-ttu-id="0605d-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0605d-127">ALIASES</span></span>

## <span data-ttu-id="0605d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0605d-128">RELATED LINKS</span></span>

