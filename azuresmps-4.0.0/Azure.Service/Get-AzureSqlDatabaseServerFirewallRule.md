---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054538"
---
# <span data-ttu-id="67741-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67741-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="67741-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67741-102">SYNOPSIS</span></span>
<span data-ttu-id="67741-103">Pobiera reguły zapory dla serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="67741-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="67741-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67741-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="67741-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67741-105">DESCRIPTION</span></span>
<span data-ttu-id="67741-106">Polecenie cmdlet **Get-AzureSqlDatabaseServerFirewallRule** pobiera reguły zapory dla wystąpienia serwera bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="67741-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="67741-107">Jeśli określisz regułę zapory według nazwy, to polecenie cmdlet zwróci informacje o regule zapory.</span><span class="sxs-lookup"><span data-stu-id="67741-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="67741-108">W przeciwnym razie polecenie cmdlet zwróci informacje o wszystkich regułach zapory dotyczących określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="67741-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="67741-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67741-109">EXAMPLES</span></span>

### <span data-ttu-id="67741-110">Przykład 1: pobieranie wszystkich reguł zapory na serwerze</span><span class="sxs-lookup"><span data-stu-id="67741-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="67741-111">To polecenie pobiera wszystkie reguły zapory na serwerze bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="67741-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="67741-112">Przykład 2: uzyskiwanie reguły zapory przy użyciu jej nazwy</span><span class="sxs-lookup"><span data-stu-id="67741-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="67741-113">To polecenie pobiera regułę zapory o nazwie FirewallRule24 na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="67741-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="67741-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67741-114">PARAMETERS</span></span>

### <span data-ttu-id="67741-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="67741-115">-Profile</span></span>
<span data-ttu-id="67741-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67741-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67741-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="67741-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67741-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="67741-118">-RuleName</span></span>
<span data-ttu-id="67741-119">Określa nazwę reguły zapory, którą to polecenie cmdlet pobiera.</span><span class="sxs-lookup"><span data-stu-id="67741-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67741-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="67741-120">-ServerName</span></span>
<span data-ttu-id="67741-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="67741-121">Specifies the name of a server.</span></span>
<span data-ttu-id="67741-122">To polecenie cmdlet pobiera reguły zapory z serwera, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="67741-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="67741-123">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="67741-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67741-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67741-124">CommonParameters</span></span>
<span data-ttu-id="67741-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67741-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67741-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67741-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67741-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67741-127">INPUTS</span></span>

### <span data-ttu-id="67741-128">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="67741-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="67741-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67741-129">OUTPUTS</span></span>

### <span data-ttu-id="67741-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="67741-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="67741-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67741-131">NOTES</span></span>

## <span data-ttu-id="67741-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67741-132">RELATED LINKS</span></span>

[<span data-ttu-id="67741-133">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="67741-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="67741-134">Lista reguł zapory</span><span class="sxs-lookup"><span data-stu-id="67741-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="67741-135">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="67741-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="67741-136">Nowe — AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67741-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="67741-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67741-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="67741-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67741-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


