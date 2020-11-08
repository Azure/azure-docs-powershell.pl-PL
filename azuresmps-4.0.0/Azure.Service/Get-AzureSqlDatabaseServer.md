---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054537"
---
# <span data-ttu-id="89f08-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="89f08-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="89f08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89f08-102">SYNOPSIS</span></span>
<span data-ttu-id="89f08-103">Pobiera informacje o serwerach bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="89f08-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="89f08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89f08-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89f08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89f08-105">DESCRIPTION</span></span>
<span data-ttu-id="89f08-106">Polecenie cmdlet **Get-AzureSqlDatabaseServer** pobiera informacje o wystąpieniach serwera bazy danych SQL Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="89f08-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="89f08-107">Jeśli określisz serwer według nazwy, to polecenie cmdlet zwróci obiekt zawierający informacje na temat tego serwera.</span><span class="sxs-lookup"><span data-stu-id="89f08-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="89f08-108">W przeciwnym razie polecenie cmdlet zwraca informacje o wszystkich serwerach.</span><span class="sxs-lookup"><span data-stu-id="89f08-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="89f08-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89f08-109">EXAMPLES</span></span>

### <span data-ttu-id="89f08-110">Przykład 1: uzyskiwanie informacji o wszystkich serwerach</span><span class="sxs-lookup"><span data-stu-id="89f08-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="89f08-111">To polecenie zwraca informacje o wszystkich wystąpieniach serwera bazy danych SQL Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="89f08-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="89f08-112">Przykład 2: uzyskiwanie informacji o konkretnym serwerze</span><span class="sxs-lookup"><span data-stu-id="89f08-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="89f08-113">To polecenie zwraca informacje o serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="89f08-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="89f08-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89f08-114">PARAMETERS</span></span>

### <span data-ttu-id="89f08-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="89f08-115">-Profile</span></span>
<span data-ttu-id="89f08-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f08-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89f08-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="89f08-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89f08-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="89f08-118">-ServerName</span></span>
<span data-ttu-id="89f08-119">Określa nazwę serwera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f08-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="89f08-120">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="89f08-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="89f08-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f08-121">CommonParameters</span></span>
<span data-ttu-id="89f08-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f08-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f08-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f08-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f08-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89f08-124">INPUTS</span></span>

### <span data-ttu-id="89f08-125">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="89f08-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="89f08-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89f08-126">OUTPUTS</span></span>

### <span data-ttu-id="89f08-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="89f08-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="89f08-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89f08-128">NOTES</span></span>

## <span data-ttu-id="89f08-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89f08-129">RELATED LINKS</span></span>

[<span data-ttu-id="89f08-130">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="89f08-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="89f08-131">Lista serwerów</span><span class="sxs-lookup"><span data-stu-id="89f08-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="89f08-132">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="89f08-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="89f08-133">Nowe — AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="89f08-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="89f08-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="89f08-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="89f08-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="89f08-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


