---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243843"
---
# <span data-ttu-id="f10ed-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f10ed-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="f10ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f10ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f10ed-103">Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych Azure, który określa źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="f10ed-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="f10ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f10ed-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f10ed-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f10ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f10ed-106">Polecenie New-AzDataMigrationDatabaseInfo cmdlet tworzy obiekt DatabaseInfo określający źródłowe wystąpienie bazy danych do zmigrowania.</span><span class="sxs-lookup"><span data-stu-id="f10ed-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="f10ed-107">Nazwa bazy danych jest przyjmowana jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="f10ed-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="f10ed-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f10ed-108">EXAMPLES</span></span>

### <span data-ttu-id="f10ed-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f10ed-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="f10ed-110">Poprzedni przykład tworzy nowy obiekt DatabaseInfo dla źródłowej bazy danych **AdventureWorks2016.**</span><span class="sxs-lookup"><span data-stu-id="f10ed-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="f10ed-111">Ten skrypt zakłada, że zalogowano się już do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f10ed-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="f10ed-112">Możesz potwierdzić swój stan logowania, używając Get-AzSubscription cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f10ed-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="f10ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f10ed-113">PARAMETERS</span></span>

### <span data-ttu-id="f10ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10ed-114">-DefaultProfile</span></span>
<span data-ttu-id="f10ed-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f10ed-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f10ed-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f10ed-116">-SourceDatabaseName</span></span>
<span data-ttu-id="f10ed-117">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f10ed-117">Source Database Name.</span></span>

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

### <span data-ttu-id="f10ed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10ed-118">CommonParameters</span></span>
<span data-ttu-id="f10ed-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f10ed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10ed-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10ed-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10ed-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f10ed-121">INPUTS</span></span>

### <span data-ttu-id="f10ed-122">Brak</span><span class="sxs-lookup"><span data-stu-id="f10ed-122">None</span></span>

## <span data-ttu-id="f10ed-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f10ed-123">OUTPUTS</span></span>

### <span data-ttu-id="f10ed-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f10ed-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="f10ed-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f10ed-125">NOTES</span></span>

## <span data-ttu-id="f10ed-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f10ed-126">RELATED LINKS</span></span>
