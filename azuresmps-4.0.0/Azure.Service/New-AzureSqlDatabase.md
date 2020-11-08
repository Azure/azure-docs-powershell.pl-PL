---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054939"
---
# <span data-ttu-id="03858-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03858-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="03858-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03858-102">SYNOPSIS</span></span>
<span data-ttu-id="03858-103">Tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="03858-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="03858-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03858-104">SYNTAX</span></span>

### <span data-ttu-id="03858-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="03858-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03858-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="03858-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03858-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03858-107">DESCRIPTION</span></span>
<span data-ttu-id="03858-108">Polecenie cmdlet **New-AzureSqlDatabase** tworzy bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="03858-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="03858-109">Serwer można określić za pomocą kontekstu połączenia serwera bazy danych Azure SQL Server tworzonego przy użyciu polecenia cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="03858-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="03858-110">Jeśli określisz nazwę serwera, polecenie cmdlet użyje bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="03858-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="03858-111">Podczas tworzenia nowej bazy danych przez określenie serwera bazy danych SQL Azure polecenie cmdlet **New-AzureSqlDatabase** tworzy tymczasowy kontekst połączenia przy użyciu określonej nazwy serwera i bieżących informacji o subskrypcji platformy Azure do wykonania tej operacji.</span><span class="sxs-lookup"><span data-stu-id="03858-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="03858-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03858-112">EXAMPLES</span></span>

### <span data-ttu-id="03858-113">Przykład 1. Tworzenie bazy danych</span><span class="sxs-lookup"><span data-stu-id="03858-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="03858-114">To polecenie tworzy bazę danych SQL Azure o nazwie database1 dla kontekstu połączenia serwera bazy danych Azure SQL Server $Context.</span><span class="sxs-lookup"><span data-stu-id="03858-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="03858-115">Przykład 2: Tworzenie bazy danych w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03858-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="03858-116">W tym przykładzie jest tworzona baza danych o nazwie database1 w określonym serwerze bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="03858-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="03858-117">Polecenie cmdlet używa bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="03858-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="03858-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03858-118">PARAMETERS</span></span>

### <span data-ttu-id="03858-119">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="03858-119">-Collation</span></span>
<span data-ttu-id="03858-120">Określa sortowanie dla nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="03858-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="03858-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="03858-121">-ConnectionContext</span></span>
<span data-ttu-id="03858-122">Określa kontekst połączenia serwera, na którym to polecenie cmdlet tworzy bazę danych.</span><span class="sxs-lookup"><span data-stu-id="03858-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03858-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03858-123">-DatabaseName</span></span>
<span data-ttu-id="03858-124">Określa nazwę nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="03858-124">Specifies the name of the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03858-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="03858-125">-Edition</span></span>
<span data-ttu-id="03858-126">Określa wydanie nowej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="03858-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="03858-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="03858-127">Valid values are:</span></span> 

- <span data-ttu-id="03858-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="03858-128">None</span></span>
- <span data-ttu-id="03858-129">Siecią</span><span class="sxs-lookup"><span data-stu-id="03858-129">Web</span></span>
- <span data-ttu-id="03858-130">Biznesu</span><span class="sxs-lookup"><span data-stu-id="03858-130">Business</span></span>
- <span data-ttu-id="03858-131">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="03858-131">Basic</span></span>
- <span data-ttu-id="03858-132">Standard</span><span class="sxs-lookup"><span data-stu-id="03858-132">Standard</span></span>
-  <span data-ttu-id="03858-133">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="03858-133">Premium</span></span>

<span data-ttu-id="03858-134">Wartość domyślna to Web.</span><span class="sxs-lookup"><span data-stu-id="03858-134">The default value is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03858-135">-Force</span><span class="sxs-lookup"><span data-stu-id="03858-135">-Force</span></span>
<span data-ttu-id="03858-136">Umożliwia wykonanie akcji bez monitowania użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03858-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="03858-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="03858-137">-MaxSizeBytes</span></span>
<span data-ttu-id="03858-138">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="03858-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="03858-139">Możesz określić albo ten parametr, albo parametr *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="03858-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="03858-140">Zobacz opis parametru *MaxSizeGB* , aby uzyskać dopuszczalne wartości na podstawie wersji.</span><span class="sxs-lookup"><span data-stu-id="03858-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03858-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="03858-141">-MaxSizeGB</span></span>
<span data-ttu-id="03858-142">Określa maksymalny rozmiar bazy danych w gigabajtach.</span><span class="sxs-lookup"><span data-stu-id="03858-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="03858-143">Możesz określić albo ten parametr, albo parametr *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="03858-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="03858-144">Dopuszczalne wartości różnią się w zależności od wersji.</span><span class="sxs-lookup"><span data-stu-id="03858-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="03858-145">Wartości podstawowego wydania: 1 lub 2</span><span class="sxs-lookup"><span data-stu-id="03858-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="03858-146">Wartości w standardzie Edition: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 lub 250</span><span class="sxs-lookup"><span data-stu-id="03858-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="03858-147">Wartości Premium Edition: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 lub 500</span><span class="sxs-lookup"><span data-stu-id="03858-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="03858-148">Wartości w sieci Web: 1 lub 5</span><span class="sxs-lookup"><span data-stu-id="03858-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="03858-149">Wartości w wersji dla firm: 10, 20, 30, 40, 50, 100 lub 150</span><span class="sxs-lookup"><span data-stu-id="03858-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03858-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="03858-150">-Profile</span></span>
<span data-ttu-id="03858-151">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03858-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03858-152">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="03858-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03858-153">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="03858-153">-ServerName</span></span>
<span data-ttu-id="03858-154">Określa nazwę serwera bazy danych SQL Azure, który ma zawierać nową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="03858-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

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

### <span data-ttu-id="03858-155">-Servicesprzeciw</span><span class="sxs-lookup"><span data-stu-id="03858-155">-ServiceObjective</span></span>
<span data-ttu-id="03858-156">Określa obiekt reprezentujący nowy cel usługi (poziom wydajności) dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="03858-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="03858-157">Ta wartość reprezentuje poziom zasobów przypisanych do tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="03858-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="03858-158">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="03858-158">Valid values are:</span></span> 

<span data-ttu-id="03858-159">Podstawowe: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* Standard (S3): 789681b8-Ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="03858-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="03858-160">\* Standard (S3) jest częścią najnowszej aktualizacji bazy danych SQL V12 (wersja Preview).</span><span class="sxs-lookup"><span data-stu-id="03858-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="03858-161">Aby uzyskać więcej informacji, zobacz co nowego w usłudze Azure SQL Database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="03858-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03858-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03858-162">-Confirm</span></span>
<span data-ttu-id="03858-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03858-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03858-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03858-164">-WhatIf</span></span>
<span data-ttu-id="03858-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03858-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03858-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03858-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03858-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03858-167">CommonParameters</span></span>
<span data-ttu-id="03858-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03858-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03858-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03858-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03858-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03858-170">INPUTS</span></span>

## <span data-ttu-id="03858-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03858-171">OUTPUTS</span></span>

### <span data-ttu-id="03858-172">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="03858-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="03858-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03858-173">NOTES</span></span>
* <span data-ttu-id="03858-174">Aby usunąć bazę danych utworzoną za pomocą polecenia **New-AzureSqlDatabase** , użyj polecenia cmdlet Remove-AzureSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="03858-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="03858-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03858-175">RELATED LINKS</span></span>

[<span data-ttu-id="03858-176">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="03858-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="03858-177">Tworzenie bazy danych</span><span class="sxs-lookup"><span data-stu-id="03858-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="03858-178">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="03858-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="03858-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03858-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="03858-180">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="03858-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="03858-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03858-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="03858-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03858-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


