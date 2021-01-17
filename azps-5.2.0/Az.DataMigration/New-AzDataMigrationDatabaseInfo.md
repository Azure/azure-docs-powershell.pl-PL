---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327656"
---
# <span data-ttu-id="eb907-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="eb907-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="eb907-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb907-102">SYNOPSIS</span></span>
<span data-ttu-id="eb907-103">Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych platformy Azure, która określa źródło bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="eb907-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="eb907-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb907-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb907-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb907-105">DESCRIPTION</span></span>
<span data-ttu-id="eb907-106">Polecenie cmdlet New-AzDataMigrationDatabaseInfo tworzy obiekt DatabaseInfo, który określa wystąpienie źródłowej bazy danych, do której należy przeprowadzić migrację.</span><span class="sxs-lookup"><span data-stu-id="eb907-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="eb907-107">Nazwa bazy danych jest pobierana jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="eb907-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="eb907-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb907-108">EXAMPLES</span></span>

### <span data-ttu-id="eb907-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb907-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="eb907-110">W powyższym przykładzie tworzony jest nowy obiekt DatabaseInfo dla źródłowej **AdventureWorks2016** bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eb907-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="eb907-111">Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb907-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="eb907-112">Możesz potwierdzić stan logowania, korzystając z polecenia cmdlet Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="eb907-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="eb907-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb907-113">PARAMETERS</span></span>

### <span data-ttu-id="eb907-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb907-114">-DefaultProfile</span></span>
<span data-ttu-id="eb907-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb907-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb907-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb907-116">-SourceDatabaseName</span></span>
<span data-ttu-id="eb907-117">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eb907-117">Source Database Name.</span></span>

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

### <span data-ttu-id="eb907-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb907-118">CommonParameters</span></span>
<span data-ttu-id="eb907-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb907-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb907-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb907-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb907-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb907-121">INPUTS</span></span>

### <span data-ttu-id="eb907-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eb907-122">None</span></span>

## <span data-ttu-id="eb907-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb907-123">OUTPUTS</span></span>

### <span data-ttu-id="eb907-124">Microsoft. Azure. Management. datamigration. MODELES. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="eb907-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="eb907-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb907-125">NOTES</span></span>

## <span data-ttu-id="eb907-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb907-126">RELATED LINKS</span></span>
