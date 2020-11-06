---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: f17619fcdb16574a1fc755843e0084200031085d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548519"
---
# <span data-ttu-id="ab965-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ab965-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="ab965-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab965-102">SYNOPSIS</span></span>
<span data-ttu-id="ab965-103">Pobiera zasady geograficznej kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab965-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab965-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab965-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab965-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab965-105">DESCRIPTION</span></span>
<span data-ttu-id="ab965-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseGeoBackupPolicy** pobiera zasady kopii zapasowej Geo zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ab965-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="ab965-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ab965-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="ab965-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab965-108">EXAMPLES</span></span>

## <span data-ttu-id="ab965-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab965-109">PARAMETERS</span></span>

### <span data-ttu-id="ab965-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab965-110">-DatabaseName</span></span>
<span data-ttu-id="ab965-111">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="ab965-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab965-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab965-112">-DefaultProfile</span></span>
<span data-ttu-id="ab965-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ab965-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab965-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab965-114">-ResourceGroupName</span></span>
<span data-ttu-id="ab965-115">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ab965-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab965-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ab965-116">-ServerName</span></span>
<span data-ttu-id="ab965-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="ab965-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab965-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab965-118">CommonParameters</span></span>
<span data-ttu-id="ab965-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab965-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab965-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab965-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab965-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab965-121">INPUTS</span></span>

### <span data-ttu-id="ab965-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ab965-122">System.String</span></span>

## <span data-ttu-id="ab965-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab965-123">OUTPUTS</span></span>

### <span data-ttu-id="ab965-124">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ab965-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="ab965-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab965-125">NOTES</span></span>

## <span data-ttu-id="ab965-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab965-126">RELATED LINKS</span></span>

[<span data-ttu-id="ab965-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ab965-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="ab965-128">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ab965-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
