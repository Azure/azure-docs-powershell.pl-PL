---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054831"
---
# <span data-ttu-id="754da-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="754da-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="754da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="754da-102">SYNOPSIS</span></span>
<span data-ttu-id="754da-103">Ustawia właściwości bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="754da-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="754da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="754da-104">SYNTAX</span></span>

### <span data-ttu-id="754da-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="754da-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754da-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="754da-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754da-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="754da-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754da-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="754da-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="754da-109">Opis</span><span class="sxs-lookup"><span data-stu-id="754da-109">DESCRIPTION</span></span>
<span data-ttu-id="754da-110">Polecenie cmdlet **Set-AzureSqlDatabase** ustawia właściwości dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="754da-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="754da-111">Możesz określić bazę danych według nazwy lub przekazać obiekt bazy danych SQL Azure za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="754da-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="754da-112">Możesz określić serwer według jego nazwy lub przekazać kontekst połączenia serwera bazy danych Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="754da-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="754da-113">Utwórz kontekst połączenia, uruchamiając polecenie cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="754da-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="754da-114">Jeśli określisz nazwę serwera, polecenie cmdlet użyje bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania.</span><span class="sxs-lookup"><span data-stu-id="754da-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="754da-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="754da-115">EXAMPLES</span></span>

### <span data-ttu-id="754da-116">Przykład 1. Zmienianie rozmiaru bazy danych za pomocą kontekstu połączenia</span><span class="sxs-lookup"><span data-stu-id="754da-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="754da-117">W tym przykładzie jest zmieniany rozmiar bazy danych o nazwie Database01 GB w kontekście połączenia serwera bazy danych Azure SQL Server $Context.</span><span class="sxs-lookup"><span data-stu-id="754da-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="754da-118">Przykład 2: Zmienianie rozmiaru bazy danych przy użyciu nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="754da-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="754da-119">W tym przykładzie jest zmieniany rozmiar bazy danych o nazwie Database01 na 20 GB na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="754da-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="754da-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="754da-120">PARAMETERS</span></span>

### <span data-ttu-id="754da-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="754da-121">-ConnectionContext</span></span>
<span data-ttu-id="754da-122">Określa kontekst połączenia serwera.</span><span class="sxs-lookup"><span data-stu-id="754da-122">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="754da-123">-Database</span><span class="sxs-lookup"><span data-stu-id="754da-123">-Database</span></span>
<span data-ttu-id="754da-124">Określa obiekt reprezentujący bazę danych SQL Azure, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="754da-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="754da-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="754da-125">-DatabaseName</span></span>
<span data-ttu-id="754da-126">Określa nazwę bazy danych modyfikowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754da-126">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="754da-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="754da-127">-Edition</span></span>
<span data-ttu-id="754da-128">Określa nowe wydanie bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="754da-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="754da-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="754da-129">Valid values are:</span></span> 

- <span data-ttu-id="754da-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="754da-130">None</span></span>
- <span data-ttu-id="754da-131">Siecią</span><span class="sxs-lookup"><span data-stu-id="754da-131">Web</span></span>
- <span data-ttu-id="754da-132">Biznesu</span><span class="sxs-lookup"><span data-stu-id="754da-132">Business</span></span>
- <span data-ttu-id="754da-133">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="754da-133">Basic</span></span>
- <span data-ttu-id="754da-134">Standard</span><span class="sxs-lookup"><span data-stu-id="754da-134">Standard</span></span>
-  <span data-ttu-id="754da-135">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="754da-135">Premium</span></span>

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

### <span data-ttu-id="754da-136">-Force</span><span class="sxs-lookup"><span data-stu-id="754da-136">-Force</span></span>
<span data-ttu-id="754da-137">Umożliwia wykonanie akcji bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="754da-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="754da-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="754da-138">-MaxSizeBytes</span></span>
<span data-ttu-id="754da-139">Określa nowy maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="754da-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="754da-140">Możesz określić albo ten parametr, albo parametr *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="754da-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="754da-141">Zobacz parametr *MaxSizeGB* , aby uzyskać dozwolone wartości na podstawie wersji.</span><span class="sxs-lookup"><span data-stu-id="754da-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="754da-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="754da-142">-MaxSizeGB</span></span>
<span data-ttu-id="754da-143">Określa nowy maksymalny rozmiar bazy danych w gigabajtach.</span><span class="sxs-lookup"><span data-stu-id="754da-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="754da-144">Możesz określić albo ten parametr, albo parametr *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="754da-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="754da-145">Dopuszczalne wartości różnią się w zależności od wersji.</span><span class="sxs-lookup"><span data-stu-id="754da-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="754da-146">Wartości podstawowego wydania: 1 lub 2</span><span class="sxs-lookup"><span data-stu-id="754da-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="754da-147">Wartości w standardzie Edition: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 lub 250</span><span class="sxs-lookup"><span data-stu-id="754da-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="754da-148">Wartości Premium Edition: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 lub 500</span><span class="sxs-lookup"><span data-stu-id="754da-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="754da-149">Wartości w sieci Web: 1 lub 5</span><span class="sxs-lookup"><span data-stu-id="754da-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="754da-150">Wartości w wersji dla firm: 10, 20, 30, 40, 50, 100 lub 150</span><span class="sxs-lookup"><span data-stu-id="754da-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="754da-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="754da-151">-NewDatabaseName</span></span>
<span data-ttu-id="754da-152">Określa nową nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="754da-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754da-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="754da-153">-PassThru</span></span>
<span data-ttu-id="754da-154">Zwraca zaktualizowaną bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="754da-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="754da-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="754da-155">-Profile</span></span>
<span data-ttu-id="754da-156">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754da-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="754da-157">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="754da-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="754da-158">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="754da-158">-ServerName</span></span>
<span data-ttu-id="754da-159">Określa nazwę serwera zawierającego bazę danych, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754da-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="754da-160">-Servicesprzeciw</span><span class="sxs-lookup"><span data-stu-id="754da-160">-ServiceObjective</span></span>
<span data-ttu-id="754da-161">Określa obiekt reprezentujący nowy cel usługi (poziom wydajności) dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="754da-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="754da-162">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="754da-162">Valid values are:</span></span> 

- <span data-ttu-id="754da-163">Podstawowe: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="754da-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="754da-164">Standardowo (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="754da-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="754da-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="754da-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="754da-166">Standardowo (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="754da-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="754da-167">\* Standard (S3): 789681b8-Ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="754da-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="754da-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="754da-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="754da-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="754da-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="754da-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="754da-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="754da-171">\* Standard (S3) jest częścią najnowszej aktualizacji bazy danych SQL V12 (wersja Preview).</span><span class="sxs-lookup"><span data-stu-id="754da-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="754da-172">Aby uzyskać więcej informacji, zobacz co nowego w usłudze Azure SQL Database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="754da-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="754da-173">-Sync</span><span class="sxs-lookup"><span data-stu-id="754da-173">-Sync</span></span>
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

### <span data-ttu-id="754da-174">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="754da-174">-Confirm</span></span>
<span data-ttu-id="754da-175">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754da-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="754da-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="754da-176">-WhatIf</span></span>
<span data-ttu-id="754da-177">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754da-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="754da-178">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="754da-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="754da-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754da-179">CommonParameters</span></span>
<span data-ttu-id="754da-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="754da-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754da-181">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="754da-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754da-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="754da-182">INPUTS</span></span>

### <span data-ttu-id="754da-183">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="754da-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="754da-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="754da-184">OUTPUTS</span></span>

### <span data-ttu-id="754da-185">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="754da-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="754da-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="754da-186">NOTES</span></span>

## <span data-ttu-id="754da-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="754da-187">RELATED LINKS</span></span>

[<span data-ttu-id="754da-188">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="754da-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="754da-189">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="754da-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="754da-190">Aktualizowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="754da-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="754da-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="754da-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="754da-192">Nowe — AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="754da-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="754da-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="754da-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="754da-194">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="754da-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


