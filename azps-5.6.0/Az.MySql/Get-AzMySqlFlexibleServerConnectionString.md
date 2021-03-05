---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011953"
---
# <span data-ttu-id="f49ec-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="f49ec-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="f49ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f49ec-103">Pobierz parametrów połączenia według dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="f49ec-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="f49ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f49ec-104">SYNTAX</span></span>

### <span data-ttu-id="f49ec-105">Pobierz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f49ec-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f49ec-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f49ec-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f49ec-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f49ec-107">DESCRIPTION</span></span>
<span data-ttu-id="f49ec-108">Pobierz parametrów połączenia według dostawcy połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="f49ec-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="f49ec-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f49ec-109">EXAMPLES</span></span>

### <span data-ttu-id="f49ec-110">Przykład 1. Uzyskiwanie parametrów połączenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="f49ec-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="f49ec-111">To polecenie cmdlet wyświetla ciąg połączenia klienta według nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="f49ec-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="f49ec-112">Przykład 2. Uzyskiwanie parametrów połączenia serwera MySql według tożsamości</span><span class="sxs-lookup"><span data-stu-id="f49ec-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="f49ec-113">To polecenie cmdlet pobiera ciąg połączenia serwera MySql według tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f49ec-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="f49ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f49ec-114">PARAMETERS</span></span>

### <span data-ttu-id="f49ec-115">—Klient</span><span class="sxs-lookup"><span data-stu-id="f49ec-115">-Client</span></span>
<span data-ttu-id="f49ec-116">Dostawca połączenia klienta.</span><span class="sxs-lookup"><span data-stu-id="f49ec-116">Client connection provider.</span></span>

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

### <span data-ttu-id="f49ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49ec-117">-DefaultProfile</span></span>
<span data-ttu-id="f49ec-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f49ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f49ec-119">-InputObject</span></span>
<span data-ttu-id="f49ec-120">Serwer parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="f49ec-120">The server for the connection string.</span></span>
<span data-ttu-id="f49ec-121">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="f49ec-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f49ec-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f49ec-122">-Name</span></span>
<span data-ttu-id="f49ec-123">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f49ec-123">The name of the server.</span></span>

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

### <span data-ttu-id="f49ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="f49ec-125">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="f49ec-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49ec-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f49ec-126">-SubscriptionId</span></span>
<span data-ttu-id="f49ec-127">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f49ec-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49ec-128">CommonParameters</span></span>
<span data-ttu-id="f49ec-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49ec-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f49ec-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49ec-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f49ec-131">INPUTS</span></span>

### <span data-ttu-id="f49ec-132">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f49ec-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f49ec-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f49ec-133">OUTPUTS</span></span>

### <span data-ttu-id="f49ec-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f49ec-134">System.String</span></span>

## <span data-ttu-id="f49ec-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f49ec-135">NOTES</span></span>

<span data-ttu-id="f49ec-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f49ec-136">ALIASES</span></span>

<span data-ttu-id="f49ec-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f49ec-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f49ec-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f49ec-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f49ec-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f49ec-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f49ec-140">INPUTOBJECT: <IMySqlIdentity> Serwer parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="f49ec-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="f49ec-141">`[ConfigurationName <String>]`: nazwa konfiguracji serwera.</span><span class="sxs-lookup"><span data-stu-id="f49ec-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f49ec-142">`[DatabaseName <String>]`: nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f49ec-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f49ec-143">`[FirewallRuleName <String>]`: nazwa reguły zapory serwera.</span><span class="sxs-lookup"><span data-stu-id="f49ec-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f49ec-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f49ec-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f49ec-145">`[KeyName <String>]`: nazwa klucza serwera.</span><span class="sxs-lookup"><span data-stu-id="f49ec-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f49ec-146">`[LocationName <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f49ec-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f49ec-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f49ec-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f49ec-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="f49ec-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="f49ec-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f49ec-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f49ec-150">`[ServerName <String>]`: nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f49ec-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f49ec-151">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="f49ec-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f49ec-152">`[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f49ec-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f49ec-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f49ec-153">RELATED LINKS</span></span>

