---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719231"
---
# <span data-ttu-id="3f8c0-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3f8c0-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="3f8c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8c0-103">Pobiera zasady geograficznej kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f8c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f8c0-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f8c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f8c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3f8c0-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseGeoBackupPolicy** pobiera zasady kopii zapasowej Geo zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="3f8c0-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="3f8c0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f8c0-108">EXAMPLES</span></span>

## <span data-ttu-id="3f8c0-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f8c0-109">PARAMETERS</span></span>

### <span data-ttu-id="3f8c0-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f8c0-110">-DatabaseName</span></span>
<span data-ttu-id="3f8c0-111">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="3f8c0-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8c0-112">-ResourceGroupName</span></span>
<span data-ttu-id="3f8c0-113">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="3f8c0-114">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3f8c0-114">-ServerName</span></span>
<span data-ttu-id="3f8c0-115">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3f8c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8c0-116">-DefaultProfile</span></span>
<span data-ttu-id="3f8c0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f8c0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8c0-118">CommonParameters</span></span>
<span data-ttu-id="3f8c0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8c0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8c0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8c0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8c0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f8c0-121">INPUTS</span></span>

## <span data-ttu-id="3f8c0-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f8c0-122">OUTPUTS</span></span>

## <span data-ttu-id="3f8c0-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f8c0-123">NOTES</span></span>

## <span data-ttu-id="3f8c0-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f8c0-124">RELATED LINKS</span></span>

[<span data-ttu-id="3f8c0-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3f8c0-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="3f8c0-126">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3f8c0-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
