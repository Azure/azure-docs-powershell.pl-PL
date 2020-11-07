---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 97373d35cee4efb80ca2953c0085fe6b153ea138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707997"
---
# <span data-ttu-id="4028f-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4028f-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="4028f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4028f-102">SYNOPSIS</span></span>
<span data-ttu-id="4028f-103">Pobiera zasady geograficznej kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4028f-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="4028f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4028f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4028f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4028f-105">DESCRIPTION</span></span>
<span data-ttu-id="4028f-106">Polecenie cmdlet **Get-AzSqlDatabaseGeoBackupPolicy** pobiera zasady kopii zapasowej Geo zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="4028f-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="4028f-107">To jest zasób kopii zapasowej Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4028f-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="4028f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4028f-108">EXAMPLES</span></span>

## <span data-ttu-id="4028f-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4028f-109">PARAMETERS</span></span>

### <span data-ttu-id="4028f-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4028f-110">-DatabaseName</span></span>
<span data-ttu-id="4028f-111">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje zasady tworzenia kopii zapasowych geograficznej.</span><span class="sxs-lookup"><span data-stu-id="4028f-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="4028f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4028f-112">-DefaultProfile</span></span>
<span data-ttu-id="4028f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4028f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4028f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4028f-114">-ResourceGroupName</span></span>
<span data-ttu-id="4028f-115">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="4028f-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="4028f-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4028f-116">-ServerName</span></span>
<span data-ttu-id="4028f-117">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4028f-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4028f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4028f-118">CommonParameters</span></span>
<span data-ttu-id="4028f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4028f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4028f-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4028f-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4028f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4028f-121">INPUTS</span></span>

### <span data-ttu-id="4028f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4028f-122">System.String</span></span>

## <span data-ttu-id="4028f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4028f-123">OUTPUTS</span></span>

### <span data-ttu-id="4028f-124">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4028f-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="4028f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4028f-125">NOTES</span></span>

## <span data-ttu-id="4028f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4028f-126">RELATED LINKS</span></span>

[<span data-ttu-id="4028f-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4028f-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="4028f-128">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4028f-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
