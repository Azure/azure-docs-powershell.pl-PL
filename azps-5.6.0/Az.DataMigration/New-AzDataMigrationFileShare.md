---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: b30f9fd4b29a1be064a9e0925e39faa71485b58f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966577"
---
# <span data-ttu-id="b0d96-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="b0d96-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="b0d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d96-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d96-103">Tworzy obiekt FileShare dla usługi Azure Database Migration Service, określającą lokalny udział sieciowy do wykonywania kopii zapasowych źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b0d96-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="b0d96-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0d96-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d96-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0d96-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d96-106">Polecenie New-AzDataMigrationFileShare cmdlet tworzy obiekt FileShare określający lokalny udział sieciowy, do których usługa migracji bazy danych Azure może używać źródłowych kopii zapasowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="b0d96-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="b0d96-107">Konto usługi z uruchomionym źródłowym wystąpieniem programu SQL Server musi mieć uprawnienia do zapisu w tym udziału sieciowym.</span><span class="sxs-lookup"><span data-stu-id="b0d96-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="b0d96-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0d96-108">EXAMPLES</span></span>

### <span data-ttu-id="b0d96-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0d96-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="b0d96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0d96-110">PARAMETERS</span></span>

### <span data-ttu-id="b0d96-111">- Credential</span><span class="sxs-lookup"><span data-stu-id="b0d96-111">-Credential</span></span>
<span data-ttu-id="b0d96-112">Poświadczenia dostępu do udziału plików.</span><span class="sxs-lookup"><span data-stu-id="b0d96-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d96-113">-DefaultProfile</span></span>
<span data-ttu-id="b0d96-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d96-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="b0d96-115">-Path</span></span>
<span data-ttu-id="b0d96-116">Ścieżka udziału plików.</span><span class="sxs-lookup"><span data-stu-id="b0d96-116">File share path.</span></span>

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

### <span data-ttu-id="b0d96-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d96-117">CommonParameters</span></span>
<span data-ttu-id="b0d96-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d96-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d96-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d96-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d96-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0d96-120">INPUTS</span></span>

### <span data-ttu-id="b0d96-121">Brak</span><span class="sxs-lookup"><span data-stu-id="b0d96-121">None</span></span>

## <span data-ttu-id="b0d96-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0d96-122">OUTPUTS</span></span>

### <span data-ttu-id="b0d96-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="b0d96-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="b0d96-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0d96-124">NOTES</span></span>

## <span data-ttu-id="b0d96-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0d96-125">RELATED LINKS</span></span>
