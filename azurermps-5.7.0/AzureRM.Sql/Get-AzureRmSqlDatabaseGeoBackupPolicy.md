---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2e5e313fe35770e6841909e1f0718cfe3d9c8664
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717680"
---
# <span data-ttu-id="24fa2-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24fa2-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="24fa2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="24fa2-103">Pobiera zasady geograficznej kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="24fa2-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24fa2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24fa2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24fa2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="24fa2-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseGeoBackupPolicy** pobiera zasady kopii zapasowej Geo zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="24fa2-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="24fa2-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="24fa2-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="24fa2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24fa2-108">EXAMPLES</span></span>

## <span data-ttu-id="24fa2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24fa2-109">PARAMETERS</span></span>

### <span data-ttu-id="24fa2-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24fa2-110">-DatabaseName</span></span>
<span data-ttu-id="24fa2-111">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="24fa2-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fa2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fa2-112">-DefaultProfile</span></span>
<span data-ttu-id="24fa2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="24fa2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fa2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24fa2-114">-ResourceGroupName</span></span>
<span data-ttu-id="24fa2-115">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="24fa2-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fa2-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="24fa2-116">-ServerName</span></span>
<span data-ttu-id="24fa2-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="24fa2-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fa2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fa2-118">CommonParameters</span></span>
<span data-ttu-id="24fa2-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24fa2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fa2-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24fa2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fa2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24fa2-121">INPUTS</span></span>

### <span data-ttu-id="24fa2-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="24fa2-122">None</span></span>
<span data-ttu-id="24fa2-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="24fa2-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24fa2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24fa2-124">OUTPUTS</span></span>

## <span data-ttu-id="24fa2-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24fa2-125">NOTES</span></span>

## <span data-ttu-id="24fa2-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24fa2-126">RELATED LINKS</span></span>

[<span data-ttu-id="24fa2-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24fa2-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="24fa2-128">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="24fa2-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
