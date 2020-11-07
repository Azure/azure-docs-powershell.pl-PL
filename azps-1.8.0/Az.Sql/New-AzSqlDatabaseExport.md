---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 85f74609fe4075ef42e2b417b2d8ac2099df721b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707866"
---
# <span data-ttu-id="8565c-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="8565c-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="8565c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8565c-102">SYNOPSIS</span></span>
<span data-ttu-id="8565c-103">Eksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8565c-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="8565c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8565c-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8565c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8565c-105">DESCRIPTION</span></span>
<span data-ttu-id="8565c-106">Polecenie cmdlet **New-AzSqlDatabaseExport** wyeksportuje bazę danych SQL Azure jako plik BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8565c-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="8565c-107">W celu pobrania informacji o stanie dla tego żądania można wysłać żądanie uzyskania stanu bazy danych — eksport.</span><span class="sxs-lookup"><span data-stu-id="8565c-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="8565c-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8565c-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8565c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8565c-109">EXAMPLES</span></span>

### <span data-ttu-id="8565c-110">Przykład 1. Tworzenie żądania eksportu bazy danych</span><span class="sxs-lookup"><span data-stu-id="8565c-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="8565c-111">To polecenie tworzy żądanie eksportu dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8565c-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="8565c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8565c-112">PARAMETERS</span></span>

### <span data-ttu-id="8565c-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="8565c-113">-AdministratorLogin</span></span>
<span data-ttu-id="8565c-114">Określa nazwę administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="8565c-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8565c-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8565c-116">Określa hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="8565c-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8565c-117">-AuthenticationType</span></span>
<span data-ttu-id="8565c-118">Określa typ uwierzytelniania służący do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="8565c-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="8565c-119">Wartość domyślna to SQL, jeśli nie jest ustawiony typ uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="8565c-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="8565c-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8565c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8565c-121">Instrukcji.</span><span class="sxs-lookup"><span data-stu-id="8565c-121">Sql.</span></span>
<span data-ttu-id="8565c-122">Uwierzytelnianie SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-122">SQL authentication.</span></span>
<span data-ttu-id="8565c-123">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="8565c-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="8565c-124">ADPassword.</span></span>
<span data-ttu-id="8565c-125">Uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8565c-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="8565c-126">Ustaw *AdministratorLogin* i *AdministratorLoginPassword* na nazwę użytkownika i hasło administratora usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8565c-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="8565c-127">Ten parametr jest dostępny tylko na serwerach V12 bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="8565c-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8565c-128">-DatabaseName</span></span>
<span data-ttu-id="8565c-129">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="8565c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8565c-130">-DefaultProfile</span></span>
<span data-ttu-id="8565c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8565c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8565c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8565c-132">-ResourceGroupName</span></span>
<span data-ttu-id="8565c-133">Określa nazwę grupy zasobów dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="8565c-134">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8565c-134">-ServerName</span></span>
<span data-ttu-id="8565c-135">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8565c-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="8565c-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="8565c-136">-StorageKey</span></span>
<span data-ttu-id="8565c-137">Określa klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8565c-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="8565c-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8565c-138">-StorageKeyType</span></span>
<span data-ttu-id="8565c-139">Określa typ klucza dostępu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8565c-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="8565c-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8565c-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8565c-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="8565c-141">StorageAccessKey.</span></span>
<span data-ttu-id="8565c-142">Ta wartość korzysta z klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8565c-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="8565c-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="8565c-143">SharedAccessKey.</span></span>
<span data-ttu-id="8565c-144">Ta wartość używa klucza (SAS) (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="8565c-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="8565c-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="8565c-145">-StorageUri</span></span>
<span data-ttu-id="8565c-146">Określa łącze obiektu BLOB jako adres URL pliku BACPAC.</span><span class="sxs-lookup"><span data-stu-id="8565c-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="8565c-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8565c-147">-Confirm</span></span>
<span data-ttu-id="8565c-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8565c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8565c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8565c-149">-WhatIf</span></span>
<span data-ttu-id="8565c-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8565c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8565c-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8565c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8565c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8565c-152">CommonParameters</span></span>
<span data-ttu-id="8565c-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8565c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8565c-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8565c-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8565c-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8565c-155">INPUTS</span></span>

### <span data-ttu-id="8565c-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8565c-156">System.String</span></span>

## <span data-ttu-id="8565c-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8565c-157">OUTPUTS</span></span>

### <span data-ttu-id="8565c-158">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="8565c-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="8565c-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8565c-159">NOTES</span></span>
* <span data-ttu-id="8565c-160">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="8565c-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="8565c-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8565c-161">RELATED LINKS</span></span>

[<span data-ttu-id="8565c-162">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="8565c-162">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="8565c-163">Nowe — AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="8565c-163">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="8565c-164">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8565c-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
