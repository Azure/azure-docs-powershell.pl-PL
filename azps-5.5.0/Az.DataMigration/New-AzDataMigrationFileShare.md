---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198099"
---
# <span data-ttu-id="76a63-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="76a63-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="76a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a63-102">SYNOPSIS</span></span>
<span data-ttu-id="76a63-103">Tworzy obiekt FileShare dla usługi Azure Database Migration Service, określającą lokalny udział sieciowy do wykonywania kopii zapasowych źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="76a63-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="76a63-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76a63-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a63-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76a63-105">DESCRIPTION</span></span>
<span data-ttu-id="76a63-106">Polecenie New-AzDataMigrationFileShare cmdlet tworzy obiekt FileShare określający lokalny udział sieciowy, do których usługa migracji bazy danych Azure może używać źródłowych kopii zapasowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="76a63-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="76a63-107">Konto usługi, na którym działa źródłowe wystąpienie programu SQL Server, musi mieć uprawnienia do zapisu w tym udziału sieciowym.</span><span class="sxs-lookup"><span data-stu-id="76a63-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="76a63-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76a63-108">EXAMPLES</span></span>

### <span data-ttu-id="76a63-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76a63-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="76a63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a63-110">PARAMETERS</span></span>

### <span data-ttu-id="76a63-111">- Credential</span><span class="sxs-lookup"><span data-stu-id="76a63-111">-Credential</span></span>
<span data-ttu-id="76a63-112">Poświadczenia dostępu do udziału plików.</span><span class="sxs-lookup"><span data-stu-id="76a63-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="76a63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a63-113">-DefaultProfile</span></span>
<span data-ttu-id="76a63-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76a63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a63-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="76a63-115">-Path</span></span>
<span data-ttu-id="76a63-116">Ścieżka udziału plików.</span><span class="sxs-lookup"><span data-stu-id="76a63-116">File share path.</span></span>

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

### <span data-ttu-id="76a63-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a63-117">CommonParameters</span></span>
<span data-ttu-id="76a63-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a63-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a63-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a63-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a63-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76a63-120">INPUTS</span></span>

### <span data-ttu-id="76a63-121">Brak</span><span class="sxs-lookup"><span data-stu-id="76a63-121">None</span></span>

## <span data-ttu-id="76a63-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76a63-122">OUTPUTS</span></span>

### <span data-ttu-id="76a63-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="76a63-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="76a63-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76a63-124">NOTES</span></span>

## <span data-ttu-id="76a63-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76a63-125">RELATED LINKS</span></span>
