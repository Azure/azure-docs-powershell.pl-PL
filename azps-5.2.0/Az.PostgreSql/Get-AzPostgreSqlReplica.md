---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340582"
---
# <span data-ttu-id="3c632-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="3c632-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="3c632-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c632-102">SYNOPSIS</span></span>
<span data-ttu-id="3c632-103">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="3c632-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3c632-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c632-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3c632-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c632-105">DESCRIPTION</span></span>
<span data-ttu-id="3c632-106">Wyświetlanie wszystkich replik dla danego serwera.</span><span class="sxs-lookup"><span data-stu-id="3c632-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3c632-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c632-107">EXAMPLES</span></span>

### <span data-ttu-id="3c632-108">Przykład 1: pobieranie repliki serwera PostgreSql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="3c632-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3c632-109">To polecenie cmdlet umożliwia pobieranie repliki serwera PostgreSql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="3c632-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="3c632-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c632-110">PARAMETERS</span></span>

### <span data-ttu-id="3c632-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c632-111">-DefaultProfile</span></span>
<span data-ttu-id="3c632-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c632-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c632-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c632-113">-ResourceGroupName</span></span>
<span data-ttu-id="3c632-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c632-114">The name of the resource group.</span></span>
<span data-ttu-id="3c632-115">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="3c632-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3c632-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3c632-116">-ServerName</span></span>
<span data-ttu-id="3c632-117">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="3c632-117">The name of the server.</span></span>

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

### <span data-ttu-id="3c632-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3c632-118">-SubscriptionId</span></span>
<span data-ttu-id="3c632-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3c632-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3c632-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c632-120">CommonParameters</span></span>
<span data-ttu-id="3c632-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c632-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c632-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c632-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c632-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c632-123">INPUTS</span></span>

## <span data-ttu-id="3c632-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c632-124">OUTPUTS</span></span>

### <span data-ttu-id="3c632-125">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="3c632-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3c632-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c632-126">NOTES</span></span>

<span data-ttu-id="3c632-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3c632-127">ALIASES</span></span>

## <span data-ttu-id="3c632-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c632-128">RELATED LINKS</span></span>

