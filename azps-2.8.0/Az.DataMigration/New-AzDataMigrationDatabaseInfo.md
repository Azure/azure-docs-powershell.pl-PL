---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: f1feead56c25b76890edd0fe183e65211294cf87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705744"
---
# <span data-ttu-id="049e0-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="049e0-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="049e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="049e0-102">SYNOPSIS</span></span>
<span data-ttu-id="049e0-103">Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych platformy Azure, która określa źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="049e0-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="049e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="049e0-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="049e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="049e0-105">DESCRIPTION</span></span>
<span data-ttu-id="049e0-106">Polecenie cmdlet New-AzDataMigrationDatabaseInfo tworzy obiekt DatabaseInfo, który określa wystąpienie źródłowej bazy danych, do której należy przeprowadzić migrację.</span><span class="sxs-lookup"><span data-stu-id="049e0-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="049e0-107">Nazwa bazy danych jest pobierana jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="049e0-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="049e0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="049e0-108">EXAMPLES</span></span>

### <span data-ttu-id="049e0-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="049e0-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="049e0-110">W powyższym przykładzie tworzony jest nowy obiekt DatabaseInfo dla źródłowej **AdventureWorks2016** bazy danych.</span><span class="sxs-lookup"><span data-stu-id="049e0-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="049e0-111">Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="049e0-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="049e0-112">Możesz potwierdzić stan logowania, korzystając z polecenia cmdlet Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="049e0-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="049e0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="049e0-113">PARAMETERS</span></span>

### <span data-ttu-id="049e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049e0-114">-DefaultProfile</span></span>
<span data-ttu-id="049e0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="049e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="049e0-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="049e0-116">-SourceDatabaseName</span></span>
<span data-ttu-id="049e0-117">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="049e0-117">Source Database Name.</span></span>

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

### <span data-ttu-id="049e0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049e0-118">CommonParameters</span></span>
<span data-ttu-id="049e0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049e0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049e0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="049e0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049e0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="049e0-121">INPUTS</span></span>

### <span data-ttu-id="049e0-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="049e0-122">None</span></span>

## <span data-ttu-id="049e0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="049e0-123">OUTPUTS</span></span>

### <span data-ttu-id="049e0-124">Microsoft. Azure. Management. datamigration. MODELES. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="049e0-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="049e0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="049e0-125">NOTES</span></span>

## <span data-ttu-id="049e0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="049e0-126">RELATED LINKS</span></span>
