---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: f7ede8432f8e833b3d309925daab591889836257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719224"
---
# <span data-ttu-id="b1631-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b1631-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="b1631-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1631-102">SYNOPSIS</span></span>
<span data-ttu-id="b1631-103">Eksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b1631-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1631-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1631-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1631-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1631-105">DESCRIPTION</span></span>
<span data-ttu-id="b1631-106">Polecenie cmdlet **New-AzureRmSqlDatabaseExport** wyeksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b1631-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="b1631-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych — eksport.</span><span class="sxs-lookup"><span data-stu-id="b1631-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="b1631-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b1631-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b1631-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1631-109">EXAMPLES</span></span>

### <span data-ttu-id="b1631-110">Przykład 1. Tworzenie żądania eksportu bazy danych</span><span class="sxs-lookup"><span data-stu-id="b1631-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="b1631-111">To polecenie tworzy żądanie eksportu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b1631-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="b1631-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1631-112">PARAMETERS</span></span>

### <span data-ttu-id="b1631-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="b1631-113">-AdministratorLogin</span></span>
<span data-ttu-id="b1631-114">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="b1631-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b1631-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b1631-116">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="b1631-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b1631-117">-AuthenticationType</span></span>
<span data-ttu-id="b1631-118">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="b1631-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="b1631-119">Wartość domyślna to SQL, jeśli nie jest ustawiony typ uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="b1631-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="b1631-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b1631-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1631-121">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="b1631-121">Sql.</span></span>
<span data-ttu-id="b1631-122">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-122">SQL authentication.</span></span>
<span data-ttu-id="b1631-123">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="b1631-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="b1631-124">ADPassword.</span></span>
<span data-ttu-id="b1631-125">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1631-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="b1631-126">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b1631-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="b1631-127">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="b1631-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1631-128">-DatabaseName</span></span>
<span data-ttu-id="b1631-129">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1631-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1631-130">-ResourceGroupName</span></span>
<span data-ttu-id="b1631-131">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-131">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="b1631-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b1631-132">-ServerName</span></span>
<span data-ttu-id="b1631-133">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b1631-133">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="b1631-134">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b1631-134">-StorageKey</span></span>
<span data-ttu-id="b1631-135">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b1631-135">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="b1631-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b1631-136">-StorageKeyType</span></span>
<span data-ttu-id="b1631-137">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b1631-137">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="b1631-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b1631-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1631-139">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b1631-139">StorageAccessKey.</span></span>
<span data-ttu-id="b1631-140">Ta wartość korzysta z klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b1631-140">This value uses a storage account key.</span></span> 
- <span data-ttu-id="b1631-141">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b1631-141">SharedAccessKey.</span></span>
<span data-ttu-id="b1631-142">Ta wartość używa klucza (SAS) (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="b1631-142">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="b1631-143">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b1631-143">-StorageUri</span></span>
<span data-ttu-id="b1631-144">Określa łącze obiektu BLOB jako adres URL pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="b1631-144">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="b1631-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1631-145">-Confirm</span></span>
<span data-ttu-id="b1631-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1631-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1631-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1631-147">-WhatIf</span></span>
<span data-ttu-id="b1631-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1631-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1631-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1631-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1631-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1631-150">-DefaultProfile</span></span>
<span data-ttu-id="b1631-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1631-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1631-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1631-152">CommonParameters</span></span>
<span data-ttu-id="b1631-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1631-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1631-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1631-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1631-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1631-155">INPUTS</span></span>

## <span data-ttu-id="b1631-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1631-156">OUTPUTS</span></span>

### <span data-ttu-id="b1631-157">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="b1631-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="b1631-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1631-158">NOTES</span></span>
* <span data-ttu-id="b1631-159">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="b1631-159">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b1631-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1631-160">RELATED LINKS</span></span>

[<span data-ttu-id="b1631-161">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b1631-161">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b1631-162">Nowe — AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b1631-162">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="b1631-163">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b1631-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
