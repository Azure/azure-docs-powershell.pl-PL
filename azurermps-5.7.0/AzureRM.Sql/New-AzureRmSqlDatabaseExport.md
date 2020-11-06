---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 324686ace908235e3b48fb150249d2bad22c169b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524817"
---
# <span data-ttu-id="d8022-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="d8022-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="d8022-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8022-102">SYNOPSIS</span></span>
<span data-ttu-id="d8022-103">Eksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8022-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8022-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8022-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8022-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8022-105">DESCRIPTION</span></span>
<span data-ttu-id="d8022-106">Polecenie cmdlet **New-AzureRmSqlDatabaseExport** wyeksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8022-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="d8022-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych — eksport.</span><span class="sxs-lookup"><span data-stu-id="d8022-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="d8022-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d8022-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d8022-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8022-109">EXAMPLES</span></span>

### <span data-ttu-id="d8022-110">Przykład 1. Tworzenie żądania eksportu bazy danych</span><span class="sxs-lookup"><span data-stu-id="d8022-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="d8022-111">To polecenie tworzy żądanie eksportu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d8022-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="d8022-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8022-112">PARAMETERS</span></span>

### <span data-ttu-id="d8022-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="d8022-113">-AdministratorLogin</span></span>
<span data-ttu-id="d8022-114">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="d8022-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d8022-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d8022-116">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-116">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d8022-117">-AuthenticationType</span></span>
<span data-ttu-id="d8022-118">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="d8022-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="d8022-119">Wartość domyślna to SQL, jeśli nie jest ustawiony typ uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="d8022-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="d8022-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d8022-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8022-121">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="d8022-121">Sql.</span></span>
<span data-ttu-id="d8022-122">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-122">SQL authentication.</span></span>
<span data-ttu-id="d8022-123">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="d8022-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="d8022-124">ADPassword.</span></span>
<span data-ttu-id="d8022-125">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8022-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="d8022-126">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d8022-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="d8022-127">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-127">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8022-128">-DatabaseName</span></span>
<span data-ttu-id="d8022-129">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8022-130">-DefaultProfile</span></span>
<span data-ttu-id="d8022-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d8022-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8022-132">-ResourceGroupName</span></span>
<span data-ttu-id="d8022-133">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-133">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-134">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d8022-134">-ServerName</span></span>
<span data-ttu-id="d8022-135">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d8022-135">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d8022-136">-StorageKey</span></span>
<span data-ttu-id="d8022-137">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8022-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="d8022-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d8022-138">-StorageKeyType</span></span>
<span data-ttu-id="d8022-139">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8022-139">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="d8022-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d8022-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8022-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d8022-141">StorageAccessKey.</span></span>
<span data-ttu-id="d8022-142">Ta wartość korzysta z klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8022-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="d8022-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d8022-143">SharedAccessKey.</span></span>
<span data-ttu-id="d8022-144">Ta wartość używa klucza (SAS) (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="d8022-144">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d8022-145">-StorageUri</span></span>
<span data-ttu-id="d8022-146">Określa łącze obiektu BLOB jako adres URL pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="d8022-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8022-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8022-147">-Confirm</span></span>
<span data-ttu-id="d8022-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8022-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8022-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8022-149">-WhatIf</span></span>
<span data-ttu-id="d8022-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8022-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8022-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8022-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8022-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8022-152">CommonParameters</span></span>
<span data-ttu-id="d8022-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8022-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8022-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8022-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8022-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8022-155">INPUTS</span></span>

### <span data-ttu-id="d8022-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d8022-156">None</span></span>
<span data-ttu-id="d8022-157">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d8022-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8022-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8022-158">OUTPUTS</span></span>

### <span data-ttu-id="d8022-159">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="d8022-159">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="d8022-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8022-160">NOTES</span></span>
* <span data-ttu-id="d8022-161">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d8022-161">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d8022-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8022-162">RELATED LINKS</span></span>

[<span data-ttu-id="d8022-163">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="d8022-163">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="d8022-164">Nowe — AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="d8022-164">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="d8022-165">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d8022-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
