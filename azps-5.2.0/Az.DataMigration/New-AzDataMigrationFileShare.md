---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327661"
---
# <span data-ttu-id="64c0c-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="64c0c-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="64c0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="64c0c-103">Tworzy obiekt udostępnionego udziału w usłudze migracji bazy danych platformy Azure, który określa lokalny udział sieciowy do wykonania kopii zapasowych źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="64c0c-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="64c0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64c0c-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64c0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="64c0c-106">Polecenie cmdlet New-AzDataMigrationFileShare powoduje utworzenie obiektu udostępnionego, który określa lokalny udział sieciowy, w którym usługa migracji bazy danych Azure może wykonać kopie zapasowe źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="64c0c-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="64c0c-107">Konto usługi, w którym jest uruchomione źródłowe wystąpienie programu SQL Server, musi mieć uprawnienia do zapisu w tym udziale sieciowym.</span><span class="sxs-lookup"><span data-stu-id="64c0c-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="64c0c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64c0c-108">EXAMPLES</span></span>

### <span data-ttu-id="64c0c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64c0c-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="64c0c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64c0c-110">PARAMETERS</span></span>

### <span data-ttu-id="64c0c-111">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="64c0c-111">-Credential</span></span>
<span data-ttu-id="64c0c-112">Poświadczenia umożliwiające uzyskanie dostępu do udziału plików.</span><span class="sxs-lookup"><span data-stu-id="64c0c-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="64c0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c0c-113">-DefaultProfile</span></span>
<span data-ttu-id="64c0c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64c0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c0c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="64c0c-115">-Path</span></span>
<span data-ttu-id="64c0c-116">Ścieżka udziału plików.</span><span class="sxs-lookup"><span data-stu-id="64c0c-116">File share path.</span></span>

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

### <span data-ttu-id="64c0c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c0c-117">CommonParameters</span></span>
<span data-ttu-id="64c0c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c0c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c0c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c0c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c0c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64c0c-120">INPUTS</span></span>

### <span data-ttu-id="64c0c-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="64c0c-121">None</span></span>

## <span data-ttu-id="64c0c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64c0c-122">OUTPUTS</span></span>

### <span data-ttu-id="64c0c-123">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="64c0c-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="64c0c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64c0c-124">NOTES</span></span>

## <span data-ttu-id="64c0c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64c0c-125">RELATED LINKS</span></span>
