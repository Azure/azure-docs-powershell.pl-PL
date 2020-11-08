---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054536"
---
# <span data-ttu-id="55c9a-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="55c9a-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="55c9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="55c9a-103">Pobiera informacje o przydziałach dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="55c9a-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="55c9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55c9a-104">SYNTAX</span></span>

### <span data-ttu-id="55c9a-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="55c9a-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="55c9a-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="55c9a-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="55c9a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="55c9a-107">DESCRIPTION</span></span>
<span data-ttu-id="55c9a-108">Polecenie cmdlet **Get-AzureSqlDatabaseServerQuota** pobiera informacje o przydziałach dla określonego wystąpienia serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="55c9a-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="55c9a-109">Określ kontekst połączenia lub nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="55c9a-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="55c9a-110">Jeśli nie określisz nazwy przydziału, to polecenie cmdlet otrzyma wszystkie informacje o przydziałach dla serwera.</span><span class="sxs-lookup"><span data-stu-id="55c9a-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="55c9a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55c9a-111">EXAMPLES</span></span>

### <span data-ttu-id="55c9a-112">Przykład 1: uzyskiwanie informacji dotyczących określonego przydziału</span><span class="sxs-lookup"><span data-stu-id="55c9a-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="55c9a-113">To polecenie pobiera przydział o nazwie Premium_Databases z serwera bazy danych SQL Azure określonego przez połączenie przechowywane w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="55c9a-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="55c9a-114">Przykład 2: uzyskiwanie informacji o wszystkich przydziałach</span><span class="sxs-lookup"><span data-stu-id="55c9a-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="55c9a-115">To polecenie pobiera wszystkie wartości przydziałów z serwera określonego przez $Context połączenia.</span><span class="sxs-lookup"><span data-stu-id="55c9a-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="55c9a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55c9a-116">PARAMETERS</span></span>

### <span data-ttu-id="55c9a-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="55c9a-117">-ConnectionContext</span></span>
<span data-ttu-id="55c9a-118">Określa kontekst połączenia serwera.</span><span class="sxs-lookup"><span data-stu-id="55c9a-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55c9a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="55c9a-119">-Profile</span></span>
<span data-ttu-id="55c9a-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c9a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="55c9a-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="55c9a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="55c9a-122">-Przydział</span><span class="sxs-lookup"><span data-stu-id="55c9a-122">-QuotaName</span></span>
<span data-ttu-id="55c9a-123">Określa nazwę wartości przydziału pobieranej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c9a-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55c9a-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="55c9a-124">-ServerName</span></span>
<span data-ttu-id="55c9a-125">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="55c9a-125">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c9a-126">CommonParameters</span></span>
<span data-ttu-id="55c9a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c9a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c9a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c9a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55c9a-129">INPUTS</span></span>

## <span data-ttu-id="55c9a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55c9a-130">OUTPUTS</span></span>

### <span data-ttu-id="55c9a-131">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="55c9a-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="55c9a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55c9a-132">NOTES</span></span>
* <span data-ttu-id="55c9a-133">Uwierzytelnianie: to polecenie cmdlet może używać uwierzytelniania programu SQL Server lub uwierzytelniania opartego na certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="55c9a-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="55c9a-134">Aby zapoznać się z przykładami konfigurowania uwierzytelniania, zobacz polecenie cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="55c9a-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="55c9a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55c9a-135">RELATED LINKS</span></span>

[<span data-ttu-id="55c9a-136">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="55c9a-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="55c9a-137">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="55c9a-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="55c9a-138">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="55c9a-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


