---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055074"
---
# <span data-ttu-id="6662b-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6662b-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="6662b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6662b-102">SYNOPSIS</span></span>
<span data-ttu-id="6662b-103">Usuwa bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6662b-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="6662b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6662b-104">SYNTAX</span></span>

### <span data-ttu-id="6662b-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="6662b-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6662b-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="6662b-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6662b-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="6662b-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6662b-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="6662b-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6662b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6662b-109">DESCRIPTION</span></span>
<span data-ttu-id="6662b-110">Polecenie cmdlet **Remove-AzureSqlDatabase** usuwa bazę danych SQL Azure według kontekstu połączenia serwera lub nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="6662b-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="6662b-111">Kontekst połączenia serwera bazy danych Azure SQL Server można utworzyć przy użyciu polecenia cmdlet **New-AzureSqlDatabaseServerContext** , a następnie używać go za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662b-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="6662b-112">Po usunięciu bazy danych przez określenie nazwy serwera bazy danych Azure SQL Server polecenie cmdlet **Remove-AzureSqlDatabase** używa nazwy i bieżących informacji o subskrypcji platformy Azure do wykonania tej operacji.</span><span class="sxs-lookup"><span data-stu-id="6662b-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="6662b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6662b-113">EXAMPLES</span></span>

### <span data-ttu-id="6662b-114">Przykład 1: Usuwanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="6662b-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="6662b-115">To polecenie usuwa bazę danych o nazwie Database01 z kontekstu połączenia serwera bazy danych Azure SQL Server $Context.</span><span class="sxs-lookup"><span data-stu-id="6662b-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="6662b-116">Przykład 2: Usuwanie bazy danych przy użyciu nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="6662b-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="6662b-117">To polecenie usuwa bazę danych o nazwie Database01 z serwera bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="6662b-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="6662b-118">Przykład 3: Usuwanie bazy danych przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="6662b-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="6662b-119">W tym przykładzie pokazano alternatywną metodę przechodzenia obiektu bazy danych za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="6662b-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="6662b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6662b-120">PARAMETERS</span></span>

### <span data-ttu-id="6662b-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="6662b-121">-ConnectionContext</span></span>
<span data-ttu-id="6662b-122">Określa kontekst połączenia serwera, z którego jest usuwana baza danych.</span><span class="sxs-lookup"><span data-stu-id="6662b-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-123">-Database</span><span class="sxs-lookup"><span data-stu-id="6662b-123">-Database</span></span>
<span data-ttu-id="6662b-124">Określa obiekt reprezentujący bazę danych, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662b-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6662b-125">-DatabaseName</span></span>
<span data-ttu-id="6662b-126">Określa nazwę bazy danych, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662b-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6662b-127">-Force</span></span>
<span data-ttu-id="6662b-128">Umożliwia wykonanie akcji bez monitowania użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6662b-128">Allows the action to complete without prompting the user for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="6662b-129">-Profile</span></span>
<span data-ttu-id="6662b-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662b-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6662b-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6662b-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6662b-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6662b-132">-ServerName</span></span>
<span data-ttu-id="6662b-133">Określa nazwę serwera, na którym ten aplet polecenia usunie bazę danych.</span><span class="sxs-lookup"><span data-stu-id="6662b-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6662b-134">-Confirm</span></span>
<span data-ttu-id="6662b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6662b-136">-WhatIf</span></span>
<span data-ttu-id="6662b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6662b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6662b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6662b-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6662b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6662b-139">CommonParameters</span></span>
<span data-ttu-id="6662b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6662b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6662b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6662b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6662b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6662b-142">INPUTS</span></span>

### <span data-ttu-id="6662b-143">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="6662b-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="6662b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6662b-144">OUTPUTS</span></span>

## <span data-ttu-id="6662b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6662b-145">NOTES</span></span>
* <span data-ttu-id="6662b-146">Ze względu na dotkliwość operacji to polecenie cmdlet domyślnie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6662b-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="6662b-147">Aby pominąć potwierdzenie, określ parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="6662b-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="6662b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6662b-148">RELATED LINKS</span></span>

[<span data-ttu-id="6662b-149">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="6662b-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6662b-150">Usuwanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="6662b-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="6662b-151">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="6662b-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6662b-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6662b-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="6662b-153">Nowe — AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6662b-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="6662b-154">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="6662b-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="6662b-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6662b-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


