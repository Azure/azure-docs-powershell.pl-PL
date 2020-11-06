---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 4ea8a6aca74634e8105026e45c25b861e8c060f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544748"
---
# <span data-ttu-id="791d9-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="791d9-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="791d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="791d9-102">SYNOPSIS</span></span>
<span data-ttu-id="791d9-103">Importuje plik BACPAC i tworzy nową bazę danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="791d9-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="791d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="791d9-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="791d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="791d9-105">DESCRIPTION</span></span>
<span data-ttu-id="791d9-106">Polecenie cmdlet **New-AzureRmSqlDatabaseImport** importuje plik BACPAC z konta usługi Azure Storage do nowej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="791d9-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="791d9-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="791d9-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="791d9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="791d9-108">EXAMPLES</span></span>

### <span data-ttu-id="791d9-109">Przykład 1. Tworzenie żądania importu pliku BACPAC</span><span class="sxs-lookup"><span data-stu-id="791d9-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="791d9-110">To polecenie tworzy żądanie importu w celu zaimportowania BACPAC do nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="791d9-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="791d9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="791d9-111">PARAMETERS</span></span>

### <span data-ttu-id="791d9-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="791d9-112">-AdministratorLogin</span></span>
<span data-ttu-id="791d9-113">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="791d9-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="791d9-115">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="791d9-116">-AuthenticationType</span></span>
<span data-ttu-id="791d9-117">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="791d9-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="791d9-118">Ten parametr ma domyślnie wartość SQL, jeśli nie ustawiono typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="791d9-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="791d9-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="791d9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="791d9-120">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="791d9-120">SQL.</span></span>
<span data-ttu-id="791d9-121">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-121">SQL authentication.</span></span>
<span data-ttu-id="791d9-122">Ustaw parametry *AdministratorLogin* i *AdministratorLoginPassword* z nazwą użytkownika i hasłem administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="791d9-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="791d9-123">ADPassword.</span></span>
<span data-ttu-id="791d9-124">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="791d9-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="791d9-125">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="791d9-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="791d9-126">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="791d9-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="791d9-128">Określa maksymalny rozmiar nowo zaimportowanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="791d9-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="791d9-129">-DatabaseName</span></span>
<span data-ttu-id="791d9-130">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791d9-131">-DefaultProfile</span></span>
<span data-ttu-id="791d9-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="791d9-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="791d9-133">-Edition</span></span>
<span data-ttu-id="791d9-134">Określa wersję nowej bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="791d9-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="791d9-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="791d9-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="791d9-136">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="791d9-136">Premium</span></span>
- <span data-ttu-id="791d9-137">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="791d9-137">Basic</span></span>
- <span data-ttu-id="791d9-138">Standard</span><span class="sxs-lookup"><span data-stu-id="791d9-138">Standard</span></span>
- <span data-ttu-id="791d9-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="791d9-139">DataWarehouse</span></span>
- <span data-ttu-id="791d9-140">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="791d9-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791d9-141">-ResourceGroupName</span></span>
<span data-ttu-id="791d9-142">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-142">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-143">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="791d9-143">-ServerName</span></span>
<span data-ttu-id="791d9-144">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="791d9-144">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-145">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="791d9-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="791d9-146">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="791d9-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="791d9-147">-StorageKey</span></span>
<span data-ttu-id="791d9-148">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="791d9-148">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="791d9-149">-StorageKeyType</span></span>
<span data-ttu-id="791d9-150">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="791d9-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="791d9-151">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="791d9-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="791d9-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="791d9-152">StorageAccessKey.</span></span>
<span data-ttu-id="791d9-153">Używa klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="791d9-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="791d9-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="791d9-154">SharedAccessKey.</span></span>
<span data-ttu-id="791d9-155">Używa klucza podpisu dostępu współdzielonego (SAS).</span><span class="sxs-lookup"><span data-stu-id="791d9-155">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="791d9-156">-StorageUri</span></span>
<span data-ttu-id="791d9-157">Określa identyfikator URI obiektu blob pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="791d9-157">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="791d9-158">-Confirm</span></span>
<span data-ttu-id="791d9-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791d9-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="791d9-160">-WhatIf</span></span>
<span data-ttu-id="791d9-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791d9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="791d9-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="791d9-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791d9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791d9-163">CommonParameters</span></span>
<span data-ttu-id="791d9-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="791d9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791d9-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791d9-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791d9-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="791d9-166">INPUTS</span></span>

### <span data-ttu-id="791d9-167">System. String</span><span class="sxs-lookup"><span data-stu-id="791d9-167">System.String</span></span>

## <span data-ttu-id="791d9-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="791d9-168">OUTPUTS</span></span>

### <span data-ttu-id="791d9-169">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="791d9-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="791d9-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="791d9-170">NOTES</span></span>
* <span data-ttu-id="791d9-171">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="791d9-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="791d9-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="791d9-172">RELATED LINKS</span></span>

[<span data-ttu-id="791d9-173">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="791d9-173">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="791d9-174">Nowe — AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="791d9-174">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="791d9-175">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="791d9-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

