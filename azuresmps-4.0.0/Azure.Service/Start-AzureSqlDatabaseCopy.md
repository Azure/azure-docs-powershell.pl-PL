---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413068"
---
# <span data-ttu-id="83414-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="83414-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="83414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83414-102">SYNOPSIS</span></span>
<span data-ttu-id="83414-103">Rozpoczyna operację kopiowania bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="83414-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="83414-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83414-104">SYNTAX</span></span>

### <span data-ttu-id="83414-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83414-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83414-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="83414-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83414-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="83414-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83414-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="83414-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83414-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="83414-109">DESCRIPTION</span></span>
<span data-ttu-id="83414-110">Polecenie **cmdlet Start-AzureSqlDatabaseCopy** uruchamia operację kopiowania jednej lub ciągłej kopii określonej usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="83414-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="83414-111">To polecenie cmdlet nie jest transactional.</span><span class="sxs-lookup"><span data-stu-id="83414-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="83414-112">Oryginalna baza danych jest źródłową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="83414-112">The original database is the source database.</span></span>
<span data-ttu-id="83414-113">Kopia jest pomocniczą lub docelową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="83414-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="83414-114">W przypadku kopii ciągłej źródłowe i docelowe bazy danych nie mogą znajdować się na tym samym serwerze, a serwery hostujące źródłowe i docelowe bazy danych muszą być częścią tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83414-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="83414-115">Jeśli parametr *ContinuousCopy* nie zostanie określony, to polecenie cmdlet utworzy kopię źródłową bazy danych w czasie rzeczywistym.</span><span class="sxs-lookup"><span data-stu-id="83414-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="83414-116">Po otrzymaniu odpowiedzi operacja może być nadal w toku.</span><span class="sxs-lookup"><span data-stu-id="83414-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="83414-117">Operację można monitorować za pomocą polecenia cmdlet Get-AzureSqlDatabaseCopy lub Get-AzureSqlDatabaseOperation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83414-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="83414-118">Jeśli określisz *kopię ContinuousCopy,* to polecenie cmdlet utworzy kopię ciągłą źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="83414-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="83414-119">Po otrzymaniu odpowiedzi operacja będzie w toku.</span><span class="sxs-lookup"><span data-stu-id="83414-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="83414-120">Operację można monitorować przy użyciu narzędzia **Get-AzureSqlDatabaseCopy** lub **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="83414-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="83414-121">Kopię ciągłą można utworzyć jako bazę danych w trybie online lub offline.</span><span class="sxs-lookup"><span data-stu-id="83414-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="83414-122">Kopia ciągła w trybie online służy do konfigurowania usługi Active Geo-Replication dla usługi Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ Database.</span><span class="sxs-lookup"><span data-stu-id="83414-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="83414-123">Kopia ciągła w trybie offline służy do konfigurowania standardowego Geo-Replication dla usługi Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ Database.</span><span class="sxs-lookup"><span data-stu-id="83414-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="83414-124">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83414-124">EXAMPLES</span></span>

### <span data-ttu-id="83414-125">Przykład 1. Planowanie ciągłej kopii bazy danych</span><span class="sxs-lookup"><span data-stu-id="83414-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="83414-126">To polecenie pozwala zaplanować ciągłą kopię bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="83414-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="83414-127">To polecenie tworzy docelową bazę danych na serwerze o nazwie bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="83414-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="83414-128">Przykład 2. Tworzenie kopii raz na tym samym serwerze</span><span class="sxs-lookup"><span data-stu-id="83414-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="83414-129">To polecenie tworzy kopię bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="83414-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="83414-130">Polecenie tworzy kopię o nazwie OrdersCopy na tym samym serwerze.</span><span class="sxs-lookup"><span data-stu-id="83414-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="83414-131">Przykład 3. Planowanie ciągłej kopii bazy danych w trybie offline</span><span class="sxs-lookup"><span data-stu-id="83414-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="83414-132">To polecenie pozwala zaplanować ciągłą kopię bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="83414-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="83414-133">To polecenie tworzy docelową bazę danych w trybie offline na serwerze o nazwie bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="83414-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="83414-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83414-134">PARAMETERS</span></span>

### <span data-ttu-id="83414-135">- ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="83414-135">-ContinuousCopy</span></span>
<span data-ttu-id="83414-136">Wskazuje, że kopia bazy danych będzie kopią ciągłą (repliką bazy danych).</span><span class="sxs-lookup"><span data-stu-id="83414-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="83414-137">Kopia ciągła nie jest obsługiwana na tym samym serwerze.</span><span class="sxs-lookup"><span data-stu-id="83414-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="83414-138">Jeśli ten parametr nie zostanie określony, wykonywana jest kopia raz.</span><span class="sxs-lookup"><span data-stu-id="83414-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="83414-139">W przypadku kopii razowej źródło i bazy danych partnerów muszą znajdować się na tym samym serwerze.</span><span class="sxs-lookup"><span data-stu-id="83414-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="83414-140">— Baza danych</span><span class="sxs-lookup"><span data-stu-id="83414-140">-Database</span></span>
<span data-ttu-id="83414-141">Określa obiekt reprezentujący źródłową bazę danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="83414-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="83414-142">Ten parametr akceptuje dane wejściowe potoku.</span><span class="sxs-lookup"><span data-stu-id="83414-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="83414-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83414-143">-DatabaseName</span></span>
<span data-ttu-id="83414-144">Określa nazwę źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="83414-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="83414-145">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="83414-145">-Force</span></span>
<span data-ttu-id="83414-146">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="83414-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83414-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="83414-147">-OfflineSecondary</span></span>
<span data-ttu-id="83414-148">Określa, że kopia ciągła jest kopią pasywną, a nie aktywną.</span><span class="sxs-lookup"><span data-stu-id="83414-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="83414-149">Jeśli źródłową bazą danych jest baza danych w wersji Standard, ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="83414-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="83414-150">Jeśli ten parametr jest określony, należy również określić *kopię ciągłą.*</span><span class="sxs-lookup"><span data-stu-id="83414-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="83414-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="83414-151">-PartnerDatabase</span></span>
<span data-ttu-id="83414-152">Określa nazwę docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="83414-152">Specifies name of the target database.</span></span>
<span data-ttu-id="83414-153">W przypadku określenia *parametru ContinuousCopy* wartość *parametru PartnerDatabase* musi być dopasowana do nazwy źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="83414-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="83414-154">Jeśli nie określisz *wartości ContinuousCopy,* musisz określić nazwę docelowej bazy danych, która może różnić się od nazwy źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="83414-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="83414-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="83414-155">-PartnerServer</span></span>
<span data-ttu-id="83414-156">Określa nazwę serwera hostowego docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="83414-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="83414-157">Ten serwer musi mieć tę samą subskrypcję platformy Azure, co serwer źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="83414-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="83414-158">— Profil</span><span class="sxs-lookup"><span data-stu-id="83414-158">-Profile</span></span>
<span data-ttu-id="83414-159">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83414-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83414-160">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="83414-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83414-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83414-161">-ServerName</span></span>
<span data-ttu-id="83414-162">Określa nazwę serwera, na którym znajduje się źródłowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="83414-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="83414-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83414-163">-Confirm</span></span>
<span data-ttu-id="83414-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="83414-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83414-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83414-165">-WhatIf</span></span>
<span data-ttu-id="83414-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83414-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83414-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="83414-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83414-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83414-168">CommonParameters</span></span>
<span data-ttu-id="83414-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83414-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83414-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83414-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83414-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83414-171">INPUTS</span></span>

### <span data-ttu-id="83414-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="83414-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="83414-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83414-173">OUTPUTS</span></span>

### <span data-ttu-id="83414-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="83414-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="83414-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83414-175">NOTES</span></span>
* <span data-ttu-id="83414-176">Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="83414-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="83414-177">Aby uzyskać przykład sposobu używania uwierzytelniania opartego na certyfikatach w celu skonfigurowania bieżącej subskrypcji, zobacz New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83414-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="83414-178">Monitorowanie: Aby sprawdzić stan co najmniej jednej ciągłej relacji kopiowania, które są aktywne na serwerze, użyj polecenia cmdlet **Get-AzureSqlDatabaseCopy.**</span><span class="sxs-lookup"><span data-stu-id="83414-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="83414-179">Aby sprawdzić stan operacji na poziomie źródłowym i docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="83414-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="83414-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83414-180">RELATED LINKS</span></span>

[<span data-ttu-id="83414-181">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="83414-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="83414-182">Operacje na platformie Azure SQL Databases</span><span class="sxs-lookup"><span data-stu-id="83414-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="83414-183">Uruchamianie kopiowania bazy danych</span><span class="sxs-lookup"><span data-stu-id="83414-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="83414-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="83414-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="83414-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="83414-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


