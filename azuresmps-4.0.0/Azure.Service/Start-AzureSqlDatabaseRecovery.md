---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054389"
---
# <span data-ttu-id="60974-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="60974-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="60974-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60974-102">SYNOPSIS</span></span>
<span data-ttu-id="60974-103">Inicjuje żądanie przywrócenia bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="60974-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60974-104">SYNTAX</span></span>

### <span data-ttu-id="60974-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="60974-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="60974-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="60974-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="60974-107">Opis</span><span class="sxs-lookup"><span data-stu-id="60974-107">DESCRIPTION</span></span>
<span data-ttu-id="60974-108">Polecenie cmdlet **Start-AzureSqlDatabaseRecovery** inicjuje żądanie przywrócenia bazy danych na żywo lub porzuconej.</span><span class="sxs-lookup"><span data-stu-id="60974-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="60974-109">To polecenie cmdlet obsługuje odzyskiwanie podstawowe, które wykorzystuje ostatnią znaną dostępną kopię zapasową bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="60974-110">Operacja odzyskiwania powoduje utworzenie nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="60974-111">Jeśli odzyskasz bazę danych na tym samym serwerze, musisz określić inną nazwę dla nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="60974-112">Aby wykonać przywracanie w czasie dla bazy danych, zamiast tego użyj polecenia cmdlet **Start-AzureSqlDatabaseRestore** .</span><span class="sxs-lookup"><span data-stu-id="60974-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="60974-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60974-113">EXAMPLES</span></span>

### <span data-ttu-id="60974-114">Przykład 1: odzyskiwanie bazy danych określonej jako obiekt</span><span class="sxs-lookup"><span data-stu-id="60974-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="60974-115">Pierwsze polecenie pobiera obiekt bazy danych przy użyciu polecenia cmdlet **Get-AzureSqlRecoverableDatabase** .</span><span class="sxs-lookup"><span data-stu-id="60974-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="60974-116">Polecenie zapisuje ten obiekt w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="60974-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="60974-117">Drugie polecenie odkryje bazę danych przechowywaną w $Database.</span><span class="sxs-lookup"><span data-stu-id="60974-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="60974-118">Przykład 2: odzyskiwanie bazy danych określonej według nazwy</span><span class="sxs-lookup"><span data-stu-id="60974-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="60974-119">To polecenie umożliwia odkrycie bazy danych przy użyciu nazwy bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="60974-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60974-120">PARAMETERS</span></span>

### <span data-ttu-id="60974-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="60974-121">-Profile</span></span>
<span data-ttu-id="60974-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60974-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60974-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="60974-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60974-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="60974-124">-SourceDatabase</span></span>
<span data-ttu-id="60974-125">Określa obiekt bazy danych reprezentujący bazę danych, której dotyczy ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="60974-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60974-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="60974-126">-SourceDatabaseName</span></span>
<span data-ttu-id="60974-127">Określa nazwę bazy danych, która ma być odzyskana przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="60974-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60974-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="60974-128">-SourceServerName</span></span>
<span data-ttu-id="60974-129">Określa nazwę serwera, na którym jest uruchomiona źródłowa baza danych, lub w której uruchomiono źródłową bazę danych przed jej usunięciem.</span><span class="sxs-lookup"><span data-stu-id="60974-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60974-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="60974-130">-TargetDatabaseName</span></span>
<span data-ttu-id="60974-131">Określa nazwę odzyskanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="60974-132">Jeśli źródłowa baza danych jest wciąż na żywo, w celu odzyskania jej na tym samym serwerze musisz określić nazwę, która różni się od nazwy źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="60974-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60974-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="60974-133">-TargetServerName</span></span>
<span data-ttu-id="60974-134">Określa nazwę serwera, na którym ma zostać przywrócona baza danych.</span><span class="sxs-lookup"><span data-stu-id="60974-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="60974-135">Bazę danych można przywrócić na tym samym serwerze lub na innym serwerze.</span><span class="sxs-lookup"><span data-stu-id="60974-135">You can restore a database to the same server or to a different server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60974-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60974-136">CommonParameters</span></span>
<span data-ttu-id="60974-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60974-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60974-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60974-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60974-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60974-139">INPUTS</span></span>

### <span data-ttu-id="60974-140">Microsoft. platformy windowsazure. Management. SQL. MODELES. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="60974-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="60974-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60974-141">OUTPUTS</span></span>

### <span data-ttu-id="60974-142">Microsoft. platformy windowsazure. Management. SQL. MODELES. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="60974-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="60974-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60974-143">NOTES</span></span>
* <span data-ttu-id="60974-144">Aby uruchomić to polecenie cmdlet, należy użyć uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="60974-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="60974-145">Uruchom następujące polecenia na komputerze, na którym jest uruchamiane to polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60974-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="60974-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60974-146">RELATED LINKS</span></span>

[<span data-ttu-id="60974-147">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="60974-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="60974-148">Utwórz żądanie odzyskania bazy danych</span><span class="sxs-lookup"><span data-stu-id="60974-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="60974-149">Replikowanie Geo w bazie danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="60974-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="60974-150">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="60974-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="60974-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="60974-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="60974-152">Start — AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="60974-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


