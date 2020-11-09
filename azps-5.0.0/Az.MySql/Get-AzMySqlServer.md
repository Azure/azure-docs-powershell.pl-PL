---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317208"
---
# <span data-ttu-id="a9f43-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="a9f43-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="a9f43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9f43-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f43-103">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="a9f43-103">Gets information about a server.</span></span>

## <span data-ttu-id="a9f43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9f43-104">SYNTAX</span></span>

### <span data-ttu-id="a9f43-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9f43-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9f43-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a9f43-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9f43-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9f43-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9f43-108">Lista</span><span class="sxs-lookup"><span data-stu-id="a9f43-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9f43-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a9f43-109">DESCRIPTION</span></span>
<span data-ttu-id="a9f43-110">Pobiera informacje o serwerze.</span><span class="sxs-lookup"><span data-stu-id="a9f43-110">Gets information about a server.</span></span>

## <span data-ttu-id="a9f43-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9f43-111">EXAMPLES</span></span>

### <span data-ttu-id="a9f43-112">Przykład 1: pobieranie serwera MySql z kontekstem domyślnym</span><span class="sxs-lookup"><span data-stu-id="a9f43-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a9f43-113">To polecenie cmdlet umożliwia pobieranie serwera MySql z domyślnym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="a9f43-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="a9f43-114">Przykład 2: pobieranie serwera MySql według grupy zasobów i nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="a9f43-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a9f43-115">To polecenie cmdlet umożliwia pobieranie serwera MySql według grupy zasobów i nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="a9f43-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="a9f43-116">Przykład 3: Lista wszystkich serwerów MySql w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a9f43-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a9f43-117">To polecenie cmdlet wyświetla listę wszystkich serwerów MySql w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9f43-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="a9f43-118">Przykład 4: uzyskiwanie serwera MySql za pomocą tożsamości</span><span class="sxs-lookup"><span data-stu-id="a9f43-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a9f43-119">Te listy poleceń cmdlet otrzymują tożsamość serwera MySql.</span><span class="sxs-lookup"><span data-stu-id="a9f43-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="a9f43-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9f43-120">PARAMETERS</span></span>

### <span data-ttu-id="a9f43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f43-121">-DefaultProfile</span></span>
<span data-ttu-id="a9f43-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9f43-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f43-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9f43-123">-InputObject</span></span>
<span data-ttu-id="a9f43-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a9f43-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f43-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9f43-125">-Name</span></span>
<span data-ttu-id="a9f43-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a9f43-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f43-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f43-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9f43-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9f43-128">The name of the resource group.</span></span>
<span data-ttu-id="a9f43-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a9f43-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f43-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a9f43-130">-SubscriptionId</span></span>
<span data-ttu-id="a9f43-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a9f43-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f43-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f43-132">CommonParameters</span></span>
<span data-ttu-id="a9f43-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f43-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f43-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9f43-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f43-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9f43-135">INPUTS</span></span>

### <span data-ttu-id="a9f43-136">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a9f43-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a9f43-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9f43-137">OUTPUTS</span></span>

### <span data-ttu-id="a9f43-138">Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="a9f43-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a9f43-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9f43-139">NOTES</span></span>

<span data-ttu-id="a9f43-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a9f43-140">ALIASES</span></span>

<span data-ttu-id="a9f43-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9f43-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9f43-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a9f43-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9f43-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9f43-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9f43-144">INPUTobject <IMySqlIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a9f43-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9f43-145">`[ConfigurationName <String>]`: Nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="a9f43-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a9f43-146">`[DatabaseName <String>]`: Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a9f43-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a9f43-147">`[FirewallRuleName <String>]`: Nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="a9f43-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a9f43-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a9f43-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9f43-149">`[LocationName <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9f43-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a9f43-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9f43-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a9f43-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a9f43-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a9f43-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a9f43-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a9f43-153">`[ServerName <String>]`: Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="a9f43-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a9f43-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a9f43-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a9f43-155">`[VirtualNetworkRuleName <String>]`: Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9f43-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a9f43-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9f43-156">RELATED LINKS</span></span>

