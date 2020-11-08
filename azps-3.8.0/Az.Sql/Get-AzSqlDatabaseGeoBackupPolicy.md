---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: d69d6c2976e71183fed07e2c18adc730d8ea6e61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050512"
---
# <span data-ttu-id="b5bfb-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b5bfb-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="b5bfb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bfb-103">Pobiera zasady geograficznej kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="b5bfb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5bfb-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5bfb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="b5bfb-106">Polecenie cmdlet **Get-AzSqlDatabaseGeoBackupPolicy** pobiera zasady kopii zapasowej Geo zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="b5bfb-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="b5bfb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5bfb-108">EXAMPLES</span></span>

## <span data-ttu-id="b5bfb-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5bfb-109">PARAMETERS</span></span>

### <span data-ttu-id="b5bfb-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5bfb-110">-DatabaseName</span></span>
<span data-ttu-id="b5bfb-111">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="b5bfb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bfb-112">-DefaultProfile</span></span>
<span data-ttu-id="b5bfb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b5bfb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5bfb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5bfb-114">-ResourceGroupName</span></span>
<span data-ttu-id="b5bfb-115">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b5bfb-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b5bfb-116">-ServerName</span></span>
<span data-ttu-id="b5bfb-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b5bfb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bfb-118">CommonParameters</span></span>
<span data-ttu-id="b5bfb-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bfb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bfb-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5bfb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bfb-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5bfb-121">INPUTS</span></span>

### <span data-ttu-id="b5bfb-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b5bfb-122">System.String</span></span>

## <span data-ttu-id="b5bfb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5bfb-123">OUTPUTS</span></span>

### <span data-ttu-id="b5bfb-124">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b5bfb-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="b5bfb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5bfb-125">NOTES</span></span>

## <span data-ttu-id="b5bfb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5bfb-126">RELATED LINKS</span></span>

[<span data-ttu-id="b5bfb-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b5bfb-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="b5bfb-128">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b5bfb-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
