---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: 2152835d997532b490a6be16bf329831071f2f87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966625"
---
# <span data-ttu-id="36429-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="36429-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="36429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36429-102">SYNOPSIS</span></span>
<span data-ttu-id="36429-103">Tworzy obiekt DatabaseInfo dla usługi Azure Database Migration Service, określającą źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="36429-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="36429-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36429-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36429-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36429-105">DESCRIPTION</span></span>
<span data-ttu-id="36429-106">Polecenie New-AzDataMigrationDatabaseInfo cmdlet tworzy obiekt DatabaseInfo określający źródłowe wystąpienie bazy danych do zmigrowania.</span><span class="sxs-lookup"><span data-stu-id="36429-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="36429-107">Nazwa bazy danych jest przyjmowana jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="36429-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="36429-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36429-108">EXAMPLES</span></span>

### <span data-ttu-id="36429-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36429-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="36429-110">Poprzedni przykład tworzy nowy obiekt DatabaseInfo dla źródłowej bazy danych **AdventureWorks2016.**</span><span class="sxs-lookup"><span data-stu-id="36429-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="36429-111">Ten skrypt zakłada, że zalogowano się już do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36429-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="36429-112">Możesz potwierdzić swój stan logowania, używając Get-AzSubscription cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36429-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="36429-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36429-113">PARAMETERS</span></span>

### <span data-ttu-id="36429-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36429-114">-DefaultProfile</span></span>
<span data-ttu-id="36429-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36429-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36429-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="36429-116">-SourceDatabaseName</span></span>
<span data-ttu-id="36429-117">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="36429-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36429-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36429-118">CommonParameters</span></span>
<span data-ttu-id="36429-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36429-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36429-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36429-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36429-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36429-121">INPUTS</span></span>

### <span data-ttu-id="36429-122">Brak</span><span class="sxs-lookup"><span data-stu-id="36429-122">None</span></span>

## <span data-ttu-id="36429-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36429-123">OUTPUTS</span></span>

### <span data-ttu-id="36429-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="36429-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="36429-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36429-125">NOTES</span></span>

## <span data-ttu-id="36429-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36429-126">RELATED LINKS</span></span>
