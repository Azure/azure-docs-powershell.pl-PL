---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719438"
---
# <span data-ttu-id="4dc95-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="4dc95-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="4dc95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dc95-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc95-103">Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych platformy Azure, która określa źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="4dc95-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dc95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dc95-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4dc95-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc95-106">Polecenie cmdlet New-AzureRmDataMigrationDatabaseInfo tworzy obiekt DatabaseInfo, który określa wystąpienie źródłowej bazy danych, do której należy przeprowadzić migrację.</span><span class="sxs-lookup"><span data-stu-id="4dc95-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="4dc95-107">Nazwa bazy danych jest pobierana jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="4dc95-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="4dc95-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dc95-108">EXAMPLES</span></span>

### <span data-ttu-id="4dc95-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4dc95-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="4dc95-110">W powyższym przykładzie tworzony jest nowy obiekt DatabaseInfo dla źródłowej **AdventureWorks2016** bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4dc95-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="4dc95-111">Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc95-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="4dc95-112">Możesz potwierdzić stan logowania, korzystając z polecenia cmdlet Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="4dc95-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="4dc95-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dc95-113">PARAMETERS</span></span>

### <span data-ttu-id="4dc95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc95-114">-DefaultProfile</span></span>
<span data-ttu-id="4dc95-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dc95-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4dc95-116">-SourceDatabaseName</span></span>
<span data-ttu-id="4dc95-117">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4dc95-117">Source Database Name.</span></span>

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

### <span data-ttu-id="4dc95-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc95-118">CommonParameters</span></span>
<span data-ttu-id="4dc95-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc95-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc95-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc95-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc95-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dc95-121">INPUTS</span></span>

### <span data-ttu-id="4dc95-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4dc95-122">None</span></span>

## <span data-ttu-id="4dc95-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dc95-123">OUTPUTS</span></span>

### <span data-ttu-id="4dc95-124">Microsoft. Azure. Management. datamigration. MODELES. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="4dc95-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="4dc95-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dc95-125">NOTES</span></span>

## <span data-ttu-id="4dc95-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dc95-126">RELATED LINKS</span></span>
