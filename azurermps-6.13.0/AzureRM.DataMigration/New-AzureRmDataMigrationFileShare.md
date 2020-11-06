---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551268"
---
# <span data-ttu-id="862db-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="862db-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="862db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="862db-102">SYNOPSIS</span></span>
<span data-ttu-id="862db-103">Tworzy obiekt udostępnionego udziału w usłudze migracji bazy danych platformy Azure, który określa lokalny udział sieciowy do wykonania kopii zapasowych źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="862db-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="862db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="862db-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="862db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="862db-105">DESCRIPTION</span></span>
<span data-ttu-id="862db-106">Polecenie cmdlet New-AzureRmDataMigrationFileShare powoduje utworzenie obiektu udostępnionego, który określa lokalny udział sieciowy, w którym usługa migracji bazy danych Azure może wykonać kopie zapasowe źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="862db-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="862db-107">Konto usługi, w którym jest uruchomione źródłowe wystąpienie programu SQL Server, musi mieć uprawnienia do zapisu w tym udziale sieciowym.</span><span class="sxs-lookup"><span data-stu-id="862db-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="862db-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="862db-108">EXAMPLES</span></span>

### <span data-ttu-id="862db-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="862db-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="862db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="862db-110">PARAMETERS</span></span>

### <span data-ttu-id="862db-111">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="862db-111">-Credential</span></span>
<span data-ttu-id="862db-112">Poświadczenia umożliwiające uzyskanie dostępu do udziału plików.</span><span class="sxs-lookup"><span data-stu-id="862db-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="862db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862db-113">-DefaultProfile</span></span>
<span data-ttu-id="862db-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="862db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="862db-115">-Path</span><span class="sxs-lookup"><span data-stu-id="862db-115">-Path</span></span>
<span data-ttu-id="862db-116">Ścieżka udziału plików.</span><span class="sxs-lookup"><span data-stu-id="862db-116">File share path.</span></span>

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

### <span data-ttu-id="862db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862db-117">CommonParameters</span></span>
<span data-ttu-id="862db-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862db-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862db-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="862db-120">INPUTS</span></span>

### <span data-ttu-id="862db-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="862db-121">None</span></span>

## <span data-ttu-id="862db-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="862db-122">OUTPUTS</span></span>

### <span data-ttu-id="862db-123">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="862db-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="862db-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="862db-124">NOTES</span></span>

## <span data-ttu-id="862db-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="862db-125">RELATED LINKS</span></span>
