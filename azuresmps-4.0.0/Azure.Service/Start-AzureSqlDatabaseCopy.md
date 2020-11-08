---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054811"
---
# <span data-ttu-id="734a0-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="734a0-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="734a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="734a0-102">SYNOPSIS</span></span>
<span data-ttu-id="734a0-103">Rozpoczyna operację kopiowania bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="734a0-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="734a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="734a0-104">SYNTAX</span></span>

### <span data-ttu-id="734a0-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="734a0-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734a0-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="734a0-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734a0-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="734a0-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734a0-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="734a0-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734a0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="734a0-109">DESCRIPTION</span></span>
<span data-ttu-id="734a0-110">Polecenie cmdlet **Start-AzureSqlDatabaseCopy** rozpoczyna jednorazową operację kopiowania lub ciągłą operację kopiowania określonej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="734a0-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="734a0-111">To polecenie cmdlet nie jest transakcyjne.</span><span class="sxs-lookup"><span data-stu-id="734a0-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="734a0-112">Pierwotna baza danych jest źródłową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-112">The original database is the source database.</span></span>
<span data-ttu-id="734a0-113">Kopia jest pomocniczą lub docelową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="734a0-114">W przypadku ciągłej kopii bazy danych źródłowych i docelowych nie mogą znajdować się na tym samym serwerze, a serwery, które obsługują źródłową i docelową bazę danych, muszą być częścią tego samego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="734a0-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="734a0-115">Jeśli nie określisz parametru *ContinuousCopy* , to polecenie cmdlet utworzy jednorazową kopię źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="734a0-116">Po odebraniu odpowiedzi operacja może być nadal w toku.</span><span class="sxs-lookup"><span data-stu-id="734a0-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="734a0-117">Operację można monitorować za pomocą polecenia cmdlet Get-AzureSqlDatabaseCopy lub Get-AzureSqlDatabaseOperation.</span><span class="sxs-lookup"><span data-stu-id="734a0-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="734a0-118">Jeśli określisz *ContinuousCopy* , to polecenie cmdlet utworzy ciągłą kopię źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="734a0-119">Po odebraniu odpowiedzi operacja będzie w toku.</span><span class="sxs-lookup"><span data-stu-id="734a0-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="734a0-120">Operację można monitorować, korzystając z polecenia **Get-AzureSqlDatabaseCopy** lub **Get-AzureSqlDatabaseOperation**.</span><span class="sxs-lookup"><span data-stu-id="734a0-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="734a0-121">Możesz utworzyć ciągłą kopię jako bazę danych w trybie online lub offline.</span><span class="sxs-lookup"><span data-stu-id="734a0-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="734a0-122">Nieprzerwana kopia online jest używana do konfigurowania aktywnego Geo-Replication bazy danych SQL Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="734a0-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="734a0-123">Ciągła Kopia offline jest używana do konfigurowania standardowego Geo-Replication bazy danych SQL Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="734a0-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="734a0-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="734a0-124">EXAMPLES</span></span>

### <span data-ttu-id="734a0-125">Przykład 1: Planowanie ciągłej kopii bazy danych</span><span class="sxs-lookup"><span data-stu-id="734a0-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="734a0-126">To polecenie planuje ciągłą kopię bazy danych o nazwanych zamówieniach na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="734a0-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="734a0-127">Polecenie utworzy docelową bazę danych na serwerze o nazwie bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="734a0-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="734a0-128">Przykład 2: Tworzenie jednorazowej kopii na tym samym serwerze</span><span class="sxs-lookup"><span data-stu-id="734a0-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="734a0-129">To polecenie umożliwia utworzenie jednorazowej kopii bazy danych o nazwanych zamówieniach na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="734a0-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="734a0-130">Polecenie utworzy kopię o nazwie OrdersCopy na tym samym serwerze.</span><span class="sxs-lookup"><span data-stu-id="734a0-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="734a0-131">Przykład 3: Planowanie ciągłej kopii bazy danych w trybie offline</span><span class="sxs-lookup"><span data-stu-id="734a0-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="734a0-132">To polecenie planuje ciągłą kopię bazy danych o nazwanych zamówieniach na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="734a0-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="734a0-133">To polecenie tworzy docelową bazę danych w trybie offline na serwerze o nazwie bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="734a0-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="734a0-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="734a0-134">PARAMETERS</span></span>

### <span data-ttu-id="734a0-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="734a0-135">-ContinuousCopy</span></span>
<span data-ttu-id="734a0-136">Oznacza, że kopia bazy danych będzie ciągła w kopii (bazy danych repliki).</span><span class="sxs-lookup"><span data-stu-id="734a0-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="734a0-137">Ciągła kopia nie jest obsługiwana na tym samym serwerze.</span><span class="sxs-lookup"><span data-stu-id="734a0-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="734a0-138">Jeśli ten parametr nie jest określony, wykonywana jest jednorazowa kopia.</span><span class="sxs-lookup"><span data-stu-id="734a0-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="734a0-139">W przypadku kopii jednorazowej bazy danych źródłowych i partnerskich muszą znajdować się na tym samym serwerze.</span><span class="sxs-lookup"><span data-stu-id="734a0-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-140">-Database</span><span class="sxs-lookup"><span data-stu-id="734a0-140">-Database</span></span>
<span data-ttu-id="734a0-141">Określa obiekt reprezentujący źródłową bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="734a0-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="734a0-142">Ten parametr akceptuje dane wejściowe potoku.</span><span class="sxs-lookup"><span data-stu-id="734a0-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="734a0-143">-DatabaseName</span></span>
<span data-ttu-id="734a0-144">Określa nazwę źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-145">-Force</span><span class="sxs-lookup"><span data-stu-id="734a0-145">-Force</span></span>
<span data-ttu-id="734a0-146">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="734a0-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="734a0-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="734a0-147">-OfflineSecondary</span></span>
<span data-ttu-id="734a0-148">Określa, że kopia ciągła jest kopią pasywną, a nie aktywną kopią.</span><span class="sxs-lookup"><span data-stu-id="734a0-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="734a0-149">Jeśli źródłowa baza danych jest standardową bazą danych wersji, ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="734a0-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="734a0-150">Jeśli ten parametr jest określony, należy również określić *ContinuousCopy* .</span><span class="sxs-lookup"><span data-stu-id="734a0-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="734a0-151">-PartnerDatabase</span></span>
<span data-ttu-id="734a0-152">Określa nazwę docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-152">Specifies name of the target database.</span></span>
<span data-ttu-id="734a0-153">Jeśli określisz parametr *ContinuousCopy* , wartość dla *PartnerDatabase* musi być zgodna z nazwą źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="734a0-154">Jeśli nie określisz *ContinuousCopy* , musisz określić nazwę docelowej bazy danych, która może różnić się od nazwy źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="734a0-155">-PartnerServer</span></span>
<span data-ttu-id="734a0-156">Określa nazwę serwera obsługującego docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="734a0-157">Ten serwer musi znajdować się w tej samej subskrypcji platformy Azure co źródłowy serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="734a0-158">-Profile</span></span>
<span data-ttu-id="734a0-159">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734a0-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="734a0-160">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="734a0-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="734a0-161">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="734a0-161">-ServerName</span></span>
<span data-ttu-id="734a0-162">Określa nazwę serwera, na którym znajduje się źródłowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="734a0-162">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="734a0-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="734a0-163">-Confirm</span></span>
<span data-ttu-id="734a0-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734a0-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734a0-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734a0-165">-WhatIf</span></span>
<span data-ttu-id="734a0-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734a0-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734a0-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="734a0-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734a0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734a0-168">CommonParameters</span></span>
<span data-ttu-id="734a0-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734a0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734a0-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734a0-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734a0-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="734a0-171">INPUTS</span></span>

### <span data-ttu-id="734a0-172">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="734a0-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="734a0-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="734a0-173">OUTPUTS</span></span>

### <span data-ttu-id="734a0-174">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="734a0-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="734a0-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="734a0-175">NOTES</span></span>
* <span data-ttu-id="734a0-176">Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="734a0-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="734a0-177">Aby zapoznać się z przykładem używania uwierzytelniania opartego na certyfikatach do ustawiania bieżącego abonamentu, zobacz New-AzureSqlDatabaseServerContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734a0-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="734a0-178">Monitorowanie: Aby sprawdzić stan jednej lub większej liczby relacji kopii ciągłej, które są aktywne na serwerze, użyj polecenia cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="734a0-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="734a0-179">Aby sprawdzić stan operacji zarówno w źródle, jak i w miejscu docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="734a0-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="734a0-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="734a0-180">RELATED LINKS</span></span>

[<span data-ttu-id="734a0-181">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="734a0-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="734a0-182">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="734a0-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="734a0-183">Uruchamianie kopii bazy danych</span><span class="sxs-lookup"><span data-stu-id="734a0-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="734a0-184">Polecenia cmdlet usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="734a0-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="734a0-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="734a0-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="734a0-186">Zatrzymaj — AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="734a0-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


