---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055525"
---
# <span data-ttu-id="4a9fb-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="4a9fb-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="4a9fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9fb-103">Pobiera odzyskiwalne bazy danych z określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="4a9fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a9fb-104">SYNTAX</span></span>

### <span data-ttu-id="4a9fb-105">AllDatabasesOnGivenServer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a9fb-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4a9fb-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="4a9fb-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a9fb-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4a9fb-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a9fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4a9fb-108">DESCRIPTION</span></span>
<span data-ttu-id="4a9fb-109">Polecenie cmdlet **Get-AzureSqlRecoverableDatabase** pobiera odzyskiwalne bazy danych z określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="4a9fb-110">To polecenie cmdlet pobiera określoną odzyskiwalną bazę danych lub wszystkie odzyskiwalne bazy danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="4a9fb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a9fb-111">EXAMPLES</span></span>

### <span data-ttu-id="4a9fb-112">Przykład 1: pobieranie wszystkich odzyskiwalnych baz danych</span><span class="sxs-lookup"><span data-stu-id="4a9fb-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="4a9fb-113">To polecenie umożliwia pobieranie wszystkich odzyskiwalnych baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="4a9fb-114">Przykład 2: uzyskiwanie określonej odzyskiwalnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="4a9fb-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="4a9fb-115">To polecenie pobiera bazę danych o nazwie Database17 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="4a9fb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a9fb-116">PARAMETERS</span></span>

### <span data-ttu-id="4a9fb-117">-Database</span><span class="sxs-lookup"><span data-stu-id="4a9fb-117">-Database</span></span>
<span data-ttu-id="4a9fb-118">Określa obiekt reprezentujący odzyskiwalną bazę danych, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9fb-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a9fb-119">-DatabaseName</span></span>
<span data-ttu-id="4a9fb-120">Określa nazwę odzyskiwalnej bazy danych, która ma być pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9fb-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="4a9fb-121">-Profile</span></span>
<span data-ttu-id="4a9fb-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a9fb-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a9fb-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4a9fb-124">-ServerName</span></span>
<span data-ttu-id="4a9fb-125">Określa nazwę serwera, za pomocą którego ten aplet polecenia pobiera odzyskiwalne bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9fb-126">CommonParameters</span></span>
<span data-ttu-id="4a9fb-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9fb-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a9fb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9fb-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a9fb-129">INPUTS</span></span>

### <span data-ttu-id="4a9fb-130">Microsoft. platformy windowsazure. Management. SQL. MODELES. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="4a9fb-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="4a9fb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a9fb-131">OUTPUTS</span></span>

### <span data-ttu-id="4a9fb-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="4a9fb-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="4a9fb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a9fb-133">NOTES</span></span>
* <span data-ttu-id="4a9fb-134">Aby uruchomić to polecenie cmdlet, należy użyć uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="4a9fb-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="4a9fb-135">Uruchom następujące polecenia na komputerze, na którym Uruchom to polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4a9fb-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="4a9fb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a9fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="4a9fb-137">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4a9fb-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4a9fb-138">Uzyskiwanie odzyskiwalnej bazy danych</span><span class="sxs-lookup"><span data-stu-id="4a9fb-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="4a9fb-139">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4a9fb-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4a9fb-140">Start — AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="4a9fb-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


