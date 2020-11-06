---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544655"
---
# <span data-ttu-id="f778e-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="f778e-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="f778e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f778e-102">SYNOPSIS</span></span>
<span data-ttu-id="f778e-103">Importuje plik BACPAC i tworzy nową bazę danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f778e-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f778e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f778e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f778e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f778e-105">DESCRIPTION</span></span>
<span data-ttu-id="f778e-106">Polecenie cmdlet **New-AzureRmSqlDatabaseImport** importuje plik BACPAC z konta usługi Azure Storage do nowej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f778e-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="f778e-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f778e-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="f778e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f778e-108">EXAMPLES</span></span>

### <span data-ttu-id="f778e-109">Przykład 1. Tworzenie żądania importu pliku BACPAC</span><span class="sxs-lookup"><span data-stu-id="f778e-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="f778e-110">To polecenie tworzy żądanie importu w celu zaimportowania BACPAC do nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f778e-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="f778e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f778e-111">PARAMETERS</span></span>

### <span data-ttu-id="f778e-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="f778e-112">-AdministratorLogin</span></span>
<span data-ttu-id="f778e-113">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="f778e-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f778e-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f778e-115">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="f778e-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f778e-116">-AuthenticationType</span></span>
<span data-ttu-id="f778e-117">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="f778e-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="f778e-118">Ten parametr ma domyślnie wartość SQL, jeśli nie ustawiono typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="f778e-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="f778e-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f778e-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f778e-120">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="f778e-120">SQL.</span></span>
<span data-ttu-id="f778e-121">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-121">SQL authentication.</span></span>
<span data-ttu-id="f778e-122">Ustaw parametry *AdministratorLogin* i *AdministratorLoginPassword* z nazwą użytkownika i hasłem administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="f778e-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="f778e-123">ADPassword.</span></span>
<span data-ttu-id="f778e-124">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f778e-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="f778e-125">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f778e-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="f778e-126">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="f778e-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f778e-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="f778e-128">Określa maksymalny rozmiar nowo zaimportowanej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f778e-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="f778e-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f778e-129">-DatabaseName</span></span>
<span data-ttu-id="f778e-130">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="f778e-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="f778e-131">-Edition</span></span>
<span data-ttu-id="f778e-132">Określa wersję nowej bazy danych do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f778e-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="f778e-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f778e-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f778e-134">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="f778e-134">Premium</span></span>
- <span data-ttu-id="f778e-135">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="f778e-135">Basic</span></span>
- <span data-ttu-id="f778e-136">Standard</span><span class="sxs-lookup"><span data-stu-id="f778e-136">Standard</span></span>
- <span data-ttu-id="f778e-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f778e-137">DataWarehouse</span></span>
- <span data-ttu-id="f778e-138">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="f778e-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f778e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f778e-139">-ResourceGroupName</span></span>
<span data-ttu-id="f778e-140">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="f778e-141">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f778e-141">-ServerName</span></span>
<span data-ttu-id="f778e-142">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f778e-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="f778e-143">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="f778e-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="f778e-144">Określa nazwę celu usługi, który ma zostać przypisany do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f778e-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f778e-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f778e-145">-StorageKey</span></span>
<span data-ttu-id="f778e-146">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f778e-146">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="f778e-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f778e-147">-StorageKeyType</span></span>
<span data-ttu-id="f778e-148">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f778e-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="f778e-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f778e-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f778e-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f778e-150">StorageAccessKey.</span></span>
<span data-ttu-id="f778e-151">Używa klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f778e-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="f778e-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f778e-152">SharedAccessKey.</span></span>
<span data-ttu-id="f778e-153">Używa klucza podpisu dostępu współdzielonego (SAS).</span><span class="sxs-lookup"><span data-stu-id="f778e-153">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="f778e-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f778e-154">-StorageUri</span></span>
<span data-ttu-id="f778e-155">Określa identyfikator URI obiektu blob pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="f778e-155">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="f778e-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f778e-156">-Confirm</span></span>
<span data-ttu-id="f778e-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f778e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f778e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f778e-158">-WhatIf</span></span>
<span data-ttu-id="f778e-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f778e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f778e-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f778e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f778e-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f778e-161">-DefaultProfile</span></span>
<span data-ttu-id="f778e-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f778e-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f778e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f778e-163">CommonParameters</span></span>
<span data-ttu-id="f778e-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f778e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f778e-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f778e-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f778e-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f778e-166">INPUTS</span></span>

## <span data-ttu-id="f778e-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f778e-167">OUTPUTS</span></span>

### <span data-ttu-id="f778e-168">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="f778e-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="f778e-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f778e-169">NOTES</span></span>
* <span data-ttu-id="f778e-170">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="f778e-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f778e-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f778e-171">RELATED LINKS</span></span>

[<span data-ttu-id="f778e-172">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="f778e-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="f778e-173">Nowe — AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="f778e-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="f778e-174">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f778e-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

